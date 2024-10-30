Install Selenium in Visual Studio :

Create Automation Framework
	- Add Selenium and other package to be used in Designing framework
	- Develop reusable libraries to be useful while writing test scripts for testing application


```

namespace Framework
{
	public static class Browser
	{
		private static IWebDriver _webdriver = new ChromeDriver();
		private static string url = "http://applicationtotest.in";
		public static ISearchContext Driver {get {return _webdriver;}}
		public static string Title { get {return _webDriver.Title; }}
	}

	public static void Inititalize()
	{
		Goto("");
	}

	public static void close()
	{
		_webdriver.Close();
	}

	public static void Goto(string relativeurl)
	{
		_webdriver.Navigate().GoToURL(url)
	}

}

using OpenQA.Selenium.Support.Pageobjects;
namespace Framework.Pages
{
	public static class pages
	{
		private static T GetPage<T>() Where T : new ()
		{
			var page = new t();
			PageFactory.InitElements(Browser.Driver, page);
			return page;	
		}

		public static LoginPage Login
		{
			get { return GetPage<LoginPage>(); }
		}
		
	}

}



using Framework;
using Microsoft.VisualStudio.TestTools.UnitTesting
namespace Test 
{
	public class TestBase
	{
	[TestInitialize]
	public static void Initialize()
	{
		Browser.Initialize();
	}

	[TestCleanup]
	public static void cleanup()
	{
		Browser.Close();
	}


}

```


Create Unit Test for developing Scripts to test Application.
	- Create 'unit test project' for Application to be tested
	- Add reference to Framework 
	 
Principle:
 - Yagni : You aren;t Gonna Need it
 - KISSL Keep it simple stupid

```
using OpenQA.Selenium;
using OpenQA.Selenium.Chrome;

private statiuc IWebDriver _webDriver = new ChromeDriver (@"full_path_to_browserdriver");


internal static IWebDriver GetDriver(Drivers driver)
{
	var outputdirectory = path.GetDirectoryName(Assembly.GetExecutingAssembly().Location);
	// outdirectory contain the path of the debug folder from where the code is running
	var relativePath = @"..\..\..\Framework\Drivers";
	var chromeDriverPath = Path.GetFullPath(Path.Combine(outputDirectory, relativePath));
	return new ChromeDriver(chromeDriverPath);
}

static IWebDriver driver = new ChromeDriver();
private IWebElement webelement;
private By Locator;

driver.Navigate().GoToUrl("http://www.qtptutorial.net/automation-practice);
var idElement = driver.FindElement(By.ID("idExample"));
idElement.click

```
#### Identifier in Csharp
- **By.ID**("idExample)
- **By.ClassName**("buttonClassExample")
- **By.Name**("NameExample")
- **By.LinkText**("Hey User Click this link")
- **By.PartialLinkText**("Click this link")- 
- **By.CssSelector** (".et_pb_promo_button")		
- By.XPath.
	Absolute XPath : ` .//*[@id='post-9189']/div/div[4]/div/div/form[7]/input   `
	Relative  Xpath  :  ` //input[@value='Xpath Button 9189'] `
- DOM 



##### Explicit Wait

```
private init PAGE_LOAD_TIMEOUT =10;

By element = By.XPath("//*[Contains(text(), 'Text to find')]");
return Browser.WaitUntilElementIsDisplayed(element, PAGE_LOAD_TIMEOUT);

namespace Framwork
{
 public static class browser
 {
	 internal static bool WaitUntilElementIsDisplayed(By Element, int timeout)
	 {
		 var present = false;
		 _webDriver.Manage().TimeOuts().ImplicitlyWait(TimeSpan.FromSeconds(0));
		try
		{
			present = _webDriver.FindElement(element).Displayed;
		}
		catch (NoSuchElementExeception)
		{
			
		}
		_webDriver.Manage().Timeouts.ImplicitlyWait(TimeSpan.FromSeconds(10));
		return present;
		
	 }
 }
}

```

##### Note: 
- It is easier to write , looks simple, but old browsers do not support, and need a learning effort. 
- Reference: [saucelabs](https://saucelabs.com/) 	[elementalSelenium]([Elemental Selenium](https://elementalselenium.com/tips/33-xpath-css-revisited))
- As per elemenalSelenium XPAth is faster than CssSelector
-
- Absolute Xpath is easiest way to identify and use , but offtently instable with change in structure of locator

Relative Xpath

```
By byxPath = By.Xpath("//input[@type='radio']");
IList<IWebElement> elements = driver.FindElements(byXpath)
// Return list of all radio button with matched identification

//Using Table with identifier
locator  = By.Id("tableidentifier");
var table = driver.FindElement(Locator);
 IList<IWebElement> collectionOfRows = table.FindElements(By.XPath("//[@id='htmlTableId']/tbody/tr'))';

const string DESIRED_COLUMN_HEADER = "HeaderTitle";
const string DESIRED_VALUE = "ExpectedValueFor"

//Select HeaderTitle,ReferenceColumn form table where ReferenceColumn = DESIRED_VALUE


IList<IWebElement> allcellsInRow = row.FindElements(By.XPath("/*"));

foreach (var cell in allcellsInRow)
{
	if (cell.Text == Desired_ColumnHeader)
	{
		columnIndex = columnCounter;
	}

	if (Cell.Text == DESIRED_VALUE)
	{
		string salarylocator  = string.Format (".//*[@id='htmlTableID']/tbody/tr[{0}][{1}], tr_1, columnIndex);
	var salary = driver.FindElement(By.Xp[ath(salaryLocator));
	}

// if there is no table identifier than take collection of tables and using index could be helpful
// locator = By.Tagname("table");
IList<IWebElement> tables = driver.FindElements(locator);
 IList<IWebElement> collectionOfRows = table[1].FindElements(By.XPath("//[@id='htmlTableId']/tbody/tr'))';



```

> 