
API is abbreviation for "Application Programming interface". 

An API is set of rules and protocols that allows different software applications to communication with each other.
Example: The app sends request to the weather services' API , The API Receives the request, processes it , and sends the weather data back to the app.
> APIs facilitate the exchange of information and functionality between software applications

Benefit :
- Enable different software system to work together, even if they were built by different companies or use different technologies
- They are essential for building modern applications, especially those that rely on data from multiple sources.


### API Contract 
An API contract is formal agreement that defines how two software systems will interact through an application programming Interface (API). It essentially set the rules and expectations for communication between systems. 

> An API contract is a technical specification that outlines the rules for API communication, promoting clarity, consistency and efficiency in software development

Definition of interactions:
An API contract specifies the details of how an applications will call the API and what responses it can expect. This includes
- Endpoints (the URLs where the API can be accessed)
- HTTP methods (GET, POST, PUT DELETE, etc.)
- Request and response formats ( e.g. #JSON, #XML )
- Data types an structures
- Authentication methods
- Error codes and handling

#### API Request
- Headers
- Parameters (REST parameters specify the variable  parts of your resources.)
- Methods (Operation or Transactions)
- Raw Data (Source data that has not be processed for use)

#### HTTP Response
- Response Data
- Status Code
	- 1XX Informational
	- 2XX Success
	- 3XX Redirection
	- 4XX Client Error
	- 5XX Server Error	-  


### Benefits of API Testing
API testing contributes significantly to the quality and reliability of software applications, Here are some key benefits
- Early bug Detection: even before UI of application developed
- Improved Test Coverage : APIs expose the underlying functionality of application, so including API testing leads to better test coverage and more robust applications.
- Time Efficiency: API tests are generally faster and consistent than UI Tests, which saves time from testing process. The results become important and valuable in agile and #DevOps.
- Can be performed with any tool of choice and do not depend on any language binding. Example : API use `JSON` or `XML` .
- Enhance Security: API testing can help identify security vulnerabilities, such as authentication and authorization issues, before they are being exploited. 
- Increased Reliability : we can ensure that they functions reliably under various conditions like high loads and stress.
- Facilitates Automation: Allow automation testing during continuous integration and help to uncover new bugs due to new commit.
- Core Functionality Testing : Allows 
- 

#### AUTOMATION TOOLS FOR API TESTING
##### Top 5 Tools for API Testing
- [[Testing/AutomationTesting/POSTMAN|POSTMAN]]
- KatalonStudio
- SoapU
- Rest-Assured
- Jmeter

##### JavaScript based API Testing tools.
1. Jest 
2. Mocha
3. Supertest
4. Playwright
5. Axios