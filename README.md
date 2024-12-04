# second_github
my demo session
public class Action
{
	
	public static void action() throws Throwable
	{
		System.setProperty("webdriver.chrome.driver","C:\\Users\\rkavi\\eclipse-workspace\\"
				+ "Selenium\\driver\\chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.get("https://www.amazon.in/");
		driver.manage().window().maximize();
		WebElement mobile = driver.findElement(By.xpath("//a[text()='Mobiles']"));
		Actions act = new Actions(driver);
		act.moveToElement(mobile).build().perform();
		Thread.sleep(2000);
		act.contextClick(mobile).build().perform();
		Robot r = new Robot();
		for (int i=0;i<=2;i++)
		{
			r.keyPress(KeyEvent.VK_DOWN);
			r.keyRelease(KeyEvent.VK_DOWN);
		}
		r.keyPress(KeyEvent.VK_ENTER);
		r.keyPress(KeyEvent.VK_ENTER);
		
		
	}
public static void main(String[] args) throws Throwable 
{
	action();



 
}
}
