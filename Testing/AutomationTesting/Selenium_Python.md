
#### Element identification
Available Strategies
- By.CSS_Selector
- By.Tag_Name
- By.Link_Text
- By.PARTIAL_LINK_TEXT
- By.XPATH

Element Selectors
- A selector is used in conjunction with locator strategy to narrow down exactly which element or elements should be found
- Selectors are just strings
- Selectors are strategy-dependent and app-dependent

example
```
el =driver.find_element(By.CSS_Selector, '#loginField')
```
it will return either 1 element or will raise an Exception
selenium.common.exceptions.NoSuchElementException

if you expect that an element might not be present, and if this is nominal , you should wrap your find call in exception handling.

```
els = driver.find_elements(By.CSS_Selector, '#loginField')
```
this command will return list of elements matching with specified selectors


Tip to find right selection
in DevTool --< Console
```
document.querySelector('#username')
```

#### waiting strategies

|     | Type          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                        | example                    |
| :-- | :------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------- |
| 1   | Static Wait   | wait for specified time                                                                                                                                                                                                                                                                                                                                                                                                                                            | time.sleep(x)              |
| 2   | Implicit Wait | user the webdriver servers built-in element finding retry, up to a timeout.  Under this wait type if element is not found, the server keep trying it up until the timeout you set. Implicit wait timeouts are global and apply to all elements you find. it is good if element appear quick but if not coming due to failure, script execution time will increase. Limitation is it can work only in case of FindElement. for other knd of app state it donot work | driver.implicitly_Wait(10) |
| 3   | Explicit Wait | Poll for app state using client-side methods. can check for any state which can be determined using web-driver functionality                                                                                                                                                                                                                                                                                                                                       | Read below                 |
|     |               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |                            |
Expected Condition
```
expected_condition.title_is('some title')
expected_condition.url_to_be('https://some.url.com')
expected_conditions.presence_of_element_located((By.CSS_Selector, '#foo'))
```

Sample code
```
from selenium.webdriver.support.wait import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC

wait = WebDriverWait(driver, 10)
form_auth_link= wait.until(EC.presence)_of_element_located(
	(By.LINK_TEXT, 'Form Authenttication')
))

form_auth_link.click()

```

StaleElementReferenceExceptions:
The server will respond with an error , and your code will raise a staleElementReferenceException if the element is not more available due to dynamic page.

Extra Other Methods or objects
There are many more methods in the webDriver API all of which are available on the driver objects
```
driver.back()
driver.refersh()
source = driver.page_source
res = drover.execute_Script('return 2+2;') : Execute JavaScript in the context of the page and get the result.
driver.save_screenshot('snapshotfilename.png')
```
There can have frames or alerts and multi window can be open


|                                                           |                                             |
| --------------------------------------------------------- | ------------------------------------------- |
| Command                                                   | Description                                 |
| name_list = driver.wiindow_handles                        | Get a list of IDs for all available windows |
| driver.switch_to_window(handle)                           | Switch to a given window by its handle      |
| driver.maximize_window()                                  |                                             |
| driver.minimize_window()                                  |                                             |
| driver.get_window_rect()                                  | get the value                               |
| driver.set_window_rect(x=50, y=50, height=100, width=200) | set the value                               |
|                                                           |                                             |


**Frames**
- Frames are webpages embedded in other webpages
- Frames come in to varieties. *frame*, *iframe*
- driver.switch_to.frame(frame) : switch to given frame , either by its index , its name or as found WebElement.
- driver.switch_to.parent_frame() : switch focus to the parent of the current frame (has no effect if already the top level)
- driver.switch_to.default_content() : switch focus back to the default frame/window.

Alerts


|                                 |                                                                          |
| ------------------------------- | ------------------------------------------------------------------------ |
| alerts = driver.switch_to.alert | Switch context to the alert and get a reference to it as an alert object |
| alert.accept()                  | Accept the alert (click ok button)                                       |
| alert.dismiss()                 | Dismiss the alert (click cancel button)                                  |
| text = alert.text               | Get the text displayed in the alert                                      |
| alert.send_keys('foo')          | send keystrokes into a prompt-type alert                                 |
|                                 |                                                                          |
|                                 |                                                                          |
|                                 |                                                                          |
