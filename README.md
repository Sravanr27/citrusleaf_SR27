# citrusleaf_SR27

package test;



import org.testng.annotations.Test;



import util.DriverUtil;



import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.ie.InternetExplorerDriver;
import org.testng.Assert;
import org.testng.annotations.AfterTest;
import org.testng.annotations.BeforeTest;



import org.testng.annotations.Test;







import util.DriverUtil;





import org.testng.annotations.BeforeTest;
import org.junit.Assert;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.support.ui.Select;
import org.testng.annotations.AfterTest;
public class launchBrowser {
WebDriver dr;
WebElement we;



@Test
public void f() {
dr.get("https://citrusleaf.in/");
Assert.assertEquals("Web and mobile application development company | Custom web and mobile application development in India | CitrusLeaf",dr.getTitle());



WebElement servicelink=dr.findElement(By.id("navbarDropdown"));
servicelink.click();
WebElement fltrapp = dr.findElement(By.xpath("//*[@id=\"navbarSupportedContent\"]/ul/li[2]/div/a[2]"));
fltrapp.click();
Assert.assertEquals("Flutter App Development | Flutter mobile app development | CitrusLeaf",dr.getTitle());



WebElement getintouch=dr.findElement(By.xpath("//*[@id=\"features-1\"]/div/div[1]/div[2]/div/div/div/button"));
getintouch.click();



WebElement name1=dr.findElement(By.id("contact-name"));
name1.sendKeys("Sravan Reddy");



WebElement email1=dr.findElement(By.name("email"));
email1.sendKeys("sravan@test.com");



WebElement phnn=dr.findElement(By.name("phone"));
phnn.sendKeys("9505548601");



WebElement details=dr.findElement(By.name("details"));
details.sendKeys("HI HOW ARE YOU");



WebElement sendbtn=dr.findElement(By.id("submit-form"));
sendbtn.click();




}
@BeforeTest
public void beforeTest() {
dr=DriverUtil.getBrowserInstance("chrome");
dr.manage().window().maximize();
}





@AfterTest
public void afterTest() {
dr.close();
}





}
