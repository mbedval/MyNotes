- It is all in one test framework, runner, automation API, and graphical running environment
- Java Script only
- JavaScript-injecting proxy server intercepts and rewrites all browser requests to enable feature
- Support : Chrome, Edge, Firefox, Electron
- it is faster since it runs inside of browser
- Framework Support: Mocha JS
- Reporting is supported with Mocha Reporters. 
- Cypress Dashboard is paid.
- 

#### Features:
1. Time travel
2. Debug-ability
3. Automatic Waits (built-in waits)
4. Consistence result (less flaky)
5. screenshot and video will be generated on failure
6. Cross Browser testing

#### Limitation
- can't automate window based and mobile apps
- supported with JavaScript and Typescript
- it do not support multiple super domain.
- it do not support validating various tab and windows
- reading/writing data into file is difficult.  (so might need to depend on 3rd party plugins)
- Reporting tools limited

Installation
```
npm -i init
npm install cypress --save-dev
npx cypress open
```

Sample Test Script : myFirstSuite.cy.js

```
describe('Suite1', () => {
	it('test1', () => {
		cy.visit('https://www.google.com')
	})
	
	it('test2',() => {
		expect(true).to.equal(true)
	})
})

```

#### Run Test Script 
```
npx cypress run
npx cypress run --headed
npx cypress run --spec 
npx cypress run --browser chrome --headed
```

Locator
CSS Selector = { Tag ID, Class, attribute, class attribute}
#id , .class , [attribute='value\], .class[attribute='value']
XPath 

```
cy.get('[data-cy="last-name-chars-left-count"]').as('charsleftSpan') 

cy.get('@charleftSpan').type('hello world')
```



Note: 
Cypress will retry a failing command or assertion until it passes or until the timeout is reached

#### how to debug
```
cy.get('[attribute=value] > :nth-child(2)').then( (()=> {debugger;}));

or

cy.get('[attribute=value] > :nth-child(2)').debug();
```
note: in debug mode, DevTool --> Console we can find variable subject. this subject will be context of object where debug control exit

#### working with environment variables/ Paramaters
```
In Script :CAll
	Cypress.env("MY_ENV_VARIABLE")


case 'value set at OS level:
	cmd$ export CYPRESS_MY_ENV_VARIABLE="Say Hello"
	
case 'value passed through Parameter to the Script'
	cmd$ npx cypress open --env MY_ENV_VARIABLE="Say Hello"

case 'Add to cypress.json'
	{
		baseurl" : "http://www.testurl.mb",
		"env": {
				MY_ENV_VARIRABLE: "Say hello"
		}		
	}
case "Create cypress.env.json"
	{
		"MY_ENV_VARIABLE":"hello"
	}
```

#### Simon Library /Test Doubles
'Sinon.js'
```
import {api} from './my-api'
cy.stub(api, 'getUser').returns({name: 'Bill'});

cy.stub(api, 'getUser').resolves({name: 'Bill'});
cy.stub(api, 'getUser').rejects({name: 'Bill'});


cy.spy ???????
```






#### - Tips/Tricks
To get details documentation help/code-complete at file level
```
/// <reference types="Cypress" /> 
```
To configure code-complete and documentation at project level, create "==jsconfig.json==" 
```
{
	"include": [
		".node_modules/cypress",
		"cypress/**/*.js"
	]
}
```

```
cy.type("{ENTER}")
```

Cypress is sync, but the non-cypress command will be Async . 
example: any console.log("Finished") even at end will be executed first.  Instead cy.log('message') will behave sync nature. Alternatively .then will control block of code JavaScript native async call in sync nature.
```
cy.wait(5000).then( () => {
	console.log(test is finished')	
})
```


#### hooks
order of execution is "before -> beforeEach -> afterEach -> after"

1. before : 
2. beforeEach
3. after
4. afterEach

fixtures
- to be used for local variables.
```

beforeEach(( => {
	cy.fixture('example').then(function (data) {
		this.data = data
	})
})
cy.fixture('example').then(function(data) => {
	data.email = 'updated@email.com'
	cy.log('updated: ', data)
})
```
- 
#### Custom Command
##### Add
Differentiate between adding and overwriting existing commands
```
Cypress.Commands.add('setLocalStorage, (key,value) =>{
 cy.window().then(window) => {
 window.localStorage.setItem(key,value
 )}
})

Cypress.Commands.add('getLocalStorage', (key) => {
	cy.window().then((window) => {
		return window.LocalStorage.getItem(key)
	})
})
```
Overwrite


#### references:
https://www.linkedin.com/learning/advanced-cypress/introduction-to-cypress-testing
https://github.com/cypress-io/cypress-example-kitchensink