Is an Object-Oriented browser automation API exposed as HTTP/REST

- Instance of automating a browser or device
- All other automation commands happen during the course of session
- Session reserves browsers and devices for your use over an extended period of time.
- Sessions should be ended so that Selenium/Appium know they can free the resource.

WebDriver Object : Element

- WebDriver elements represent UI Elements on a web-page or a device screen
- WebDriver elements are create when you find these UI elements, via commands that use an active session objects
- Once created, these elements objects are what are used to send commands that deal with the UI elements.

WebDriver Object : window
- used mostly in selenium and not in Appium
- Use the session object to query which windows are active, retrieving IDs for each one.
- Create new window to open new windows, or use window objects to close existing ones.

WebDriver Object: Cookie
- Cookies are text sent by the browser to the server in an HTTP header as a way to maintain state between client and server.
- There are webDriver protocol commands for getting, setting and deleting cookies
- Cookie objects in the protocol do not need special IDs, since Cookies already have a unique name which can be used.

WebDriver Responses:
	Was the command successful or not?
	For some commands only Arbitrary response data based on the type of command

WebDriver Error Responses
	Response with non-200 HTTP status code.
	JSON response body has special format with error details.

- WebDriver client == anything that can send WebDriver-appropriate HTTP requests
- Every programming language can produce HTTP requests
- Selenium and Appium client libraries already exist (i.e. Client Bindings)
- Binding client returns the object to interact 

Responsibilities of the WebDriver Server: 
The server translated WebDriver Protocol into actual automation.
- The server listens for automation commands
- Implements or triggers the appropriate automation behaviours
- Responds with any appropriate results for the automation command

There are independent "Drivers" one for each browser, that does this translation, each browser vendor products its own WebDriver server(its own 'driver')
	chrome: chromeDriver
	Firefox: GeckoDriver
	Edge: EdgeDriver
	Safari: SafariDriver


Technically there is no need for "Selenium" 
Driver used to be written by the selenium team and bundled with a single selenium server
Now they have migrated into their own projects at each of the browser companires
Selenium server still useful for having a single endpoints for client scripts
Selenium server still useful for allowing inter operation with selenium grid

