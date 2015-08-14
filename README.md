# Selenium-login
login program 

public class Login
 {
	public static void main(String[] args)
 {
    WebDriver driver = new FirefoxDriver();
    driver.get("https://edit.europe.yahoo.com/registration");
    driver.manage().window().maximize();
    WebElement elmnt = driver.findElement(By.id("country-lang"));
    Select fnd = new Select(elmnt);
    fnd.selectByVisibleText("English (India)");
    driver.findElement(By.id("first-name")).sendKeys("Baravi");
    driver.findElement(By.id("last-name")).sendKeys("C");
    driver.findElement(By.id("user-name")).sendKeys("baravi.chinnu");
    driver.findElement(By.id("password")).sendKeys("baravi3438");
    driver.findElement(By.id("mobile")).sendKeys("9486403438");
    WebElement mnth = driver.findElement(By.id("month"));
    Select mon = new Select(mnth);
    mon.selectByIndex(9);
    WebElement dat = driver.findElement(By.id("day"));
    Select date = new Select(dat);
    date.selectByValue("19");
    WebElement yr = driver.findElement(By.id("year"));
    Select year = new Select(yr);
    year.selectByValue("1990");
    driver.findElement(By.id("male")).click();
    driver.findElement(By.id("mobile-res")).sendKeys("8939886079");
    driver.findElement(By.id("relationship")).sendKeys("Brother");
    driver.findElement(By.className("submit")).click();
}
}
