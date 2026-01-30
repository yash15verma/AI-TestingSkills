# Selenium Review Examples

## Bad Practice: Hard Waits & Fragile Locators
```java
public void login() {
    driver.findElement(By.xpath("/html/body/div[1]/form/input[1]")).sendKeys("user");
    driver.findElement(By.xpath("/html/body/div[1]/form/input[2]")).sendKeys("pass");
    Thread.sleep(5000); // ❌ Anti-pattern: Hard wait
    driver.findElement(By.xpath("/html/body/div[1]/form/button")).click();
}
```

## Good Practice: Explicit Waits & POM
```java
public class LoginPage {
    private WebDriver driver;
    private WebDriverWait wait;

    // ✅ IDs or CSS are more resilient than absolute XPaths
    private By usernameField = By.id("username");
    private By passwordField = By.id("password");
    private By loginButton = By.cssSelector("button[type='submit']");

    public LoginPage(WebDriver driver) {
        this.driver = driver;
        this.wait = new WebDriverWait(driver, Duration.ofSeconds(10));
    }

    public void login(String user, String pass) {
        // ✅ Explicit wait for stability
        wait.until(ExpectedConditions.visibilityOfElementLocated(usernameField)).sendKeys(user);
        driver.findElement(passwordField).sendKeys(pass);
        driver.findElement(loginButton).click();
    }
}
```
