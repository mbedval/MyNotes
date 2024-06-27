Automation like Selenium for Apps.

- Mobile app/device automation tool (and more)
- Fully open source project (development on gitHub, run by OpenJS Foundation)
- Wraps automation up in a WebDriver interface. Doesn't perform automation 'Directly' for much greater flexibility.
- Allow authoring of automation scripts and tests in any language.
- Cross-platform API, by and large
- Huge community of users and practitioners. Lots of places to go for help.

Features of Appium:
- Basic UI Automation behaviours (find and interact with elements)
- Functionality beyond UI Automation
- Send file, take screenshots, start/stops apps, etc

**Pre-requisites for using Appium:**
- Virtual or real devices to test on (or cloud service provider)
- Mobile app development setup (Xcode for iOS, Android Studio for Android)
- The Appium software (installed via NPM or GUI App)
- Appium driver(s) for the platform you want to automate ( eg. XCUITest driver for iOS)

Appium adds implementation of mobile functionality automation not represented in the standard WebDriver spec.

Appium extends the WebDriver Protocol. Add more route so Appium commands are found in the WebDriver specs.

lock device "Post /session/{session id}/appium/device/lock"
Unlock Device: POSt /session/{session id}/appium/device/unlock
Check App Installed POST /session/{session id}/appium/device/app_uninstalled

Appium Drivers Today:
	All mobile drivers are unofficial and 
	We can write custom driver. and published
	Appium Drivers
		IOS : XCUITest Driver
		Android: UIAutomator2 Driver
		Android: Espresso Driver
		Windows: Windows Driver (WinAppDriver; Microsoft)
		macOS: Mac Driver (Applum4Mac)
		Tizen: Tizen Driver (Samsung)
		Flutter : Flutter Driver
		Youi.tv : Youi Driver

	
3 Types of App
1. Native Apps: Vendor-provided SDby all functionality is inside a 'webview'.  Ks, Obj-C or swift (iOS) , java or Kotlin (downloaded for app stores)
2. Mobile Web Apps: Web Apps accessed via mobile browser. Built using web technologies. ( access on internet, navigate to url)
3. Hybrid Apps: It is like Native apps . Developed with web technologies but published on app stores.
4. Flutter/ react native will be developed like native application.

Requirement for Mobile app under test
-  Running Appium server to connect to
- Copy of an app build somewhere on the machine appium is running on (or connected via network) Other wise already

App requirement
- App should be a debug or development build (not a production or release build)
- App should be in .apk or .app format for android and iOS respectively. 

Capabilities
- PlatformName: iOS or Android
- plafformVersion: STring representing the version of iOS or Android (optional for Android)
- deviceNameL Name of the device you want to automate (eg. iPhone 11 pro) (option for Android)
- automationName: Which Appium driver is to use (XCUITest or UiAtuomator2)
- browser

 



