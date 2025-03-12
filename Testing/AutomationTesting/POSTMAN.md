
Introduction
Postman is the API platform for using, building and testing APIs, you can use Postman desktop app to power every part of API Lifecycle

- Send requests with Postman API Client, including HTTP, GraphQL, and gRPC requests
- Design Build and Document APIs
- Build AI Agents that interacts APIs
- Test and Monitor your APIs' functionality and performance
- Organize your work and collabrate with your team on API development
- Discover new APIs and build API-Driven applications.


Workspace Overview:
	Workspace enable you to organize work and collaborate with team.  It allow to group related APIs, collections, environment, mocks, monitor and other linked elements

> Workspace Sidebar display few default component. You can enable/disable component from **`Configure sidebar`**
Workspace could be 
- Internal
- Partner
- Public

Allows to create following type of workspace
- Blank workspace
- API demos
- API Development
- API testing
- API Security
- Incident response
- Cloud infrastructure management
- Partner Collaboration

#### Collection
We can organize and automate API requests in collection.
- Using **`Collection Runner`** we can run run some or all API requests. i collection.
- It can be run manually or can be schedule or can be triggered from webhook.
- Collections can be executed from the command-line or as part of CI/CD pipeline by using the either tool
	- `postman cli`
	- `Newman`
- Simulate real-world user traffic with virtual users so you can observe how your API behaves under load.


Environments:
A Variable is a reusable value in API requests and scripts. Postman will use the variable's current value when running a request or script. We can group variables in an environments to make it easier to change values based on your work context. Variables can be create at 

`https://postman-echo.com/get?var={{Greeting}}`
Here {{env_base_url}} and {{Greeting}} are variables. and we can set value of this variable  This variable can be created at following level
`{{env_base_url}}/get?var={{my_variable}}`

