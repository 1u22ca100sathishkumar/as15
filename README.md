# as15
Selenium Java Program – Register on HYR Tutorials
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class HYRRegistration {

    public static void main(String[] args) throws InterruptedException {

        // Set ChromeDriver path
        System.setProperty("webdriver.chrome.driver", "path/to/chromedriver");

        // Launch browser
        WebDriver driver = new ChromeDriver();
        driver.manage().window().maximize();

        // Navigate to site
        driver.get("https://www.hyrtutorials.com/p/basic-controls.html");

        // Fill registration form
        driver.findElement(By.id("firstName")).sendKeys("John");
        driver.findElement(By.id("lastName")).sendKeys("Doe");
        driver.findElement(By.id("email")).sendKeys("john.doe@gmail.com");
        driver.findElement(By.id("password")).sendKeys("Test@123");

        // Select gender
        driver.findElement(By.id("malerb")).click();

        // Select language
        driver.findElement(By.id("englishchbx")).click();

        // Select country
        driver.findElement(By.id("country")).sendKeys("India");

        // Click Register button
        driver.findElement(By.id("registerbtn")).click();

        // Print confirmation
        System.out.println("Registration completed successfully");

        // Wait and close browser
        Thread.sleep(3000);
        driver.quit();
    }
}

Explanation (For Viva / Exam)

driver.get() → Opens the website

sendKeys() → Enters text into input fields

click() → Selects radio buttons, checkboxes, and submit button

By.id() → Locator strategy used for faster execution

driver.quit() → Closes the browser

Expected Output

✔ Form is submitted
✔ Registration message displayed on page
✔ Console output:

Registration completed successfully
