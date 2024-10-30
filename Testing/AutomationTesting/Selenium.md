The W3C chose the selenium/webdriver model as the standard for all browser automation.
##### WebDriver
- Selenium limited to what could be achieved with JavaScript inside a page. 
- it had native modules called drivers, with full access to each browser.
- WebDriver's good architectural idea opened up test authoring in any language
- Selenium + WebDriver = Selenium (WebDriver)

#### Selenium is used:
- for Test Web applications
- Test apps on any browser to find cross-browser compatibility issues
- Used for all kinds of other non-testing automation as well.

#### Client/Server Architecture:
REST API:- Representational State Transfer

Installation of Browser Driver
Download required browser driver

| Browser | URL                                                                   |
| ------- | --------------------------------------------------------------------- |
| Firefox | https://github.com/mozilla/geckodriver/releases                       |
| Chrome  | https://chromedriver.chromium.org/downloads                           |
| edge    | https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/ |
| Safari  |                                                                       |
|         |                                                                       |
|         |                                                                       |


**Test Web Site URL**:- https://the-internet.herokuapp.com

Relative XPath
 w3schools.com/xsl/xpath_syntax.asp 

| Expression | Description                                                                                                                |
| ---------- | -------------------------------------------------------------------------------------------------------------------------- |
| /          | Selects From the root node                                                                                                 |
| //         | Selects nodes in the document from the current node that match the selection no matter where they are                      |
| .          | Selects the current node                                                                                                   |
| ..         | Selects the parents of the current node                                                                                    |
| @          | Selects attributes                                                                                                         |
| /html      | Selects the whole html document<br>Nots: if the path starts with a slash / it always represent absolute path to an element |
| //td       | Selects all td tags no matter where they are in the document                                                               |
| //@id      | Selects all attributes that are named id                                                                                   |
|            |                                                                                                                            |
##### Wildcard 

| Wildcard | Description                |
| -------- | -------------------------- |
| \*       | Matches any element node   |
| @*       | matches any attribute node |
|          |                            |

```
By.Xpath(".//*[@class='et_pb_promo_button']")
By.Xpath("//a[contains[text(),'Click Me')]")
By.Xpath("span[contains(text(),"Email")]")
By.Xpath("//*[id='et_pb_signup_email']")
By.Xpath("//input[@value='male']") (Radio button with value)
By.Xpath("//input[#type='radio][0]") Select first radio button
```


Error :

| Error /Exception                | Description                                                     | Mitigation                                                          |
| ------------------------------- | --------------------------------------------------------------- | ------------------------------------------------------------------- |
| System.TypeInitizationException | This could be because browser is not able to initiate correctly | Check and update if browser driver.<br>Add browser driver not added |
|                                 |                                                                 |                                                                     |

- 