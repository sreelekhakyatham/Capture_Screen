//# Capture_Screen

package capturescreen;

import java.awt.Rectangle;
import java.awt.Robot;
import java.awt.image.BufferedImage;
import java.io.File;
import java.time.Duration;

import javax.imageio.ImageIO;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class CapturingScreen_Facebook 
{

	public static void main(String[] args) throws Exception 
	{
		WebDriver driver=new ChromeDriver();
		driver.get("https://facebook.com//");
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(300));
		
		Robot robot=new Robot();
		BufferedImage Image=robot.createScreenCapture(new Rectangle(new java.awt.Dimension(900,550)));
		ImageIO.write(Image,"PNG", new File("D:\\\\SSSSs.png"));
		

	}

}
