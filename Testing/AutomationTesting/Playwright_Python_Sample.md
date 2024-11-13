C:\Users\jmbx9\AppData\Local\ms-playwright

#### Installation
```
pip install pytest-playwright
playwright install
```

#### Update playwright
```
pip install pytest-playwright playwright -U
```

#### Locator

[Locator](https://playwright.dev/python/docs/api/class-locator "Locator")s are the central piece of Playwright's auto-waiting and retry-ability. In a nutshell, locators represent a way to find element(s) on the page at any moment.
https://playwright.dev/python/docs/api/class-locator


- [page.get_by_role()](https://playwright.dev/python/docs/locators#locate-by-role) to locate by explicit and implicit accessibility attributes.
- [page.get_by_text()](https://playwright.dev/python/docs/locators#locate-by-text) to locate by text content.
- [page.get_by_label()](https://playwright.dev/python/docs/locators#locate-by-label) to locate a form control by associated label's text.
- [page.get_by_placeholder()](https://playwright.dev/python/docs/locators#locate-by-placeholder) to locate an input by placeholder.
- [page.get_by_alt_text()](https://playwright.dev/python/docs/locators#locate-by-alt-text) to locate an element, usually image, by its text alternative.
- [page.get_by_title()](https://playwright.dev/python/docs/locators#locate-by-title) to locate an element by its title attribute.
- [page.get_by_test_id()](https://playwright.dev/python/docs/locators#locate-by-test-id) to locate an element based on its `data-testid` attribute (other attributes can be configured).
> https://playwright.dev/python/docs/codegen use code-generator to generate locator

```
	playwright codegen demo.playwright.dev/todomvc
```

#### Assertion
https://playwright.dev/python/docs/test-assertions


#### Test Isolation:
The playwright Pytest is based on the concept of test fixture such as the built in page fixture, which is passed into your test. Pages are isolated tests due to the `Browser Context` 

##### Benefit of isolation
- No failure carry-over. if one test fails it doesn't affect the other test.
- Easy to debug errors or flakiness, because you can run just a single test as many times as you'd like.
- Don't have to think about the order when running in parallel, sharding, etc.

#playwright uses browser contexts to achieve test isolation. each test has its own browser context. Running the test creates a new browser context each time. when using playwright as Test runner, browser context are created by default. Otherwise, you can create browser contexts manually.
```
browser = playwright.chromium.launch()
context = browser.new_context()
page = context.new_page()
```

> Browser contexts can also be used to emulate multi-page scenarios involving mobile devices, permissions, locale and color schemes. this can be achieved by emulations.
> refer : https://playwright.dev/python/docs/emulation

> Playwright can create multiple browser contexts within a single scenario. This is useful when you want to test for multi-user functionality , like a chat.

```
from playwright.sync_api import sync_playwright, Playwright

def run(playwright: Playwright):
    # create a chromium browser instance
    chromium = playwright.chromium
    browser = chromium.launch()

    # create two isolated browser contexts
    user_context = browser.new_context()
    admin_context = browser.new_context()

    # create pages and interact with contexts independently

with sync_playwright() as playwright:
    run(playwright)
```

#### Mocking 


https://playwright.dev/python/docs/mock
Sometimes, its is essential to make an API request, but the response needs to be patched to allowed for reproducing testing, in that case instead of mocking the request, one perform the request and fulfill it with the modified response.

- Mocking API requests
- Mocking API Response
- Mocking with HAR Files : HAR is an HTTP archive file that contains a record of all the network requests that are made when a page is loaded. it contains information about the request and response headers, cookies, content, timings and more. You can use HAR files to mock network requests in your tests. You will need to:

