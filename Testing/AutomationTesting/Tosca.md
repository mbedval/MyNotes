
URL
Test Manager: Source : https://www.youtube.com/watch?v=cXhlHjHBym0

TBOX Theory - Engines and Framework
File Operations : [Link](https://documentation.tricentis.com/tosca/1600/en/content/standard_subset/automation_tools/file_operations.htm)
Folder Operations : [Link](https://documentation.tricentis.com/tosca/1600/en/content/standard_subset/automation_tools/folder_operations.htm)
Expression Evaluation: [Link](https://documentation.tricentis.com/tosca/1600/en/content/standard_subset/automation_tools/expression_evaluation.htm)
Basic Windows Operations : [Link](https://documentation.tricentis.com/tosca/1600/en/content/standard_subset/automation_tools/windows_operations.htm)
XML: [Link](https://documentation.tricentis.com/tosca/1600/en/content/standard_subset/engines_3.0/xml.htm)
JSON : [Link](https://documentation.tricentis.com/tosca/1600/en/content/standard_subset/engines_3.0/json.htm)
Database : [Link](https://documentation.tricentis.com/tosca/1600/en/content/standard_subset/engines_3.0/database.htm)


##### Import Excel in Qtest
https://youtu.be/CmOaEaTxdvk

- Download sample template 
	- Click "Excel icon" on toolbar. and click "sample import template" hyper link
	- Fill template with required details of testcases.
> Sample template can have custom field which should be active in project. As admin you can select "Setting --> Field Settings" , using this you can add and make field active.
> For new test case keep test case id blank , but to update add test case id, 

- In Navigation panel select "Import Test case wizard"
- Select Excel spreadsheet field , and map it will field of Test case (donot map test id for new test case)
- 

##### How to Create Test Run Configuration
https://youtu.be/vMmtsy_zph0
- Select Configuration Field settings in the administration Area
- Configure "Variables" example Platform There are 2 variable Apple Device {iphone x, ipad mini, ipad Pro, Apple TV}, while  IOS version could be {iOS 11, iOS 12, iOS 13, iOS 14}
- Using this variables configure "configuration Set" like Apple + IOS where it allow various combination
- Now In "Test Execution" Tab, select Setting --> "Field Settings" , select Configuration and choose which configuration are needed in test planning
- So that Test can select which configuration to use while Test Execution.
- Once selection is done, qTest will generate and add test run comination 


##### qTest Converting Manual automation testing to Automated testing
https://www.youtube.com/watch?v=X6h6T5_DlTQ

- Setting up 
	- Install Automation Host
	- Enable Automation Integration "Setting --> Automation Setting" 
	- Execution Mapping
- Test Conversion (Test Design Module)
	- Convert individual test cases 
		- In Test Design select Individual Test Case and Click "Convert" button 
		- Add Unique Automation Content (i.e. name="testSum" classname="sample junit classtest" time="0.025")
		- if we need test log to existing test run then it must match the automation content field
	- Convert multiple test cases:
		- Select multiple test cases and Right Click and click "Convert" item in right click menu
	- Convert Data Query Result
		- From System Query , result with Status "is Approve = 'yes'" select required test cases
		- From Edit option Select "Batch Convert" icon
		- In Batch convert select convert To "Automation"
		- on completion, select "Input Automation Contents" button in Update progress dialog
		- enter the "Automation Content" for converted test cases. (information like test class, test method, identifier is used to  point automation execution result to test run)

> on conversion design tree changes from gree dot to a blue dot.






#### Ticentis Tosca Offers two types of Workspaces
- Single-user workspaces : for environments where only one person needs access to data.
- Multi-user workspaces for environments where several people can access. It supports by check-in/ check-out mechanism that users don't interfere with each.
	- Distributed execution is available only for multi-user workspaces.

Tosca Commander:
It is user interface of Trecentist Tosca:
> if Tosca commander is single-view mode, it can be displayed on only one desktop. You can mirror the screen on second display / monitor / projector. But options such as dual-screen mode are not supported. Same applies for remote desktops

> Default Location: `%TRICENTIS_PROJECTS%Tosca_Workspaces` Workspacesw have the file extension `*.tws`


#### Anatomy of Workspace:

|              |                                                                                                                                                                                                             |
| ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Ribbon Menu  | Consists of static menus and few Dynamic Menus. Static menus are always displayed but Dynamic menu appears if you click specific object.                                                                    |
| Tabs         | Objects types are grouped as Modules, TestCases, etc. for example TestExecution Tab contains all objects related to the executed of tests such as `executionLists`, `ExecutionList Folder` or `TestEvents`. |
| Properties   | Properties pane shows all properties of selected objects                                                                                                                                                    |
| Project Tree | The hierarchical structure of all objects in the selected tab.                                                                                                                                              |
| Status bar   | The status bar shows the progress of the action that tosca commander currently perform as well as any additional information.                                                                               |
> You can customized the View and save it for future use.



#### TestEVents
Testevent organizes the execution with Tosca Distributed Execution 


with #ToscaDistributedExecution you can distribute your tests accross all available comupting resources such as computers in your network, virtual machines or the cloud. It consistes of 3 main elements

- The user machiens (workstation), where users creates tests and trigger the execution.
- The #ToscaDistributionServer which uses the AutomationObjectService (AOS) to manage and distribute the tests among the agents using its own workspace. The AOS workspace is connected to a common repository.
- The Agent machines the execute the tests. Thanks to AOS, they do so without hosting any local workspaces. After the execution, agents save the result to the common repository via the AOS.
	- Following Agents are supported by Tricentis:
		- Execution Agent: (Engine 3.0)
		- Agent that is a full client installation of Tosca Commander

#### Steer with Enginer 3.0
The Tosca TBox framework is the basis for steering all engines 3.0 for both GUI or Non-GUI based tests. It is built on .NET Technology and provides you with additional testing functionalities suchs as Business recover or XBrowser. Tosca TBOX framework offers the following advantages
- Higher performance in the creation and execution of tests.
- One common interface for all supported technologies
- Easy Creation of XModules and TestCases with #ToscaXScan and Tricentis Automation Recording
- Common dynamic exepression that behave the same way for all engines 3.0
- A broader range of Actionsmodes.


#ToscaXScan: While performing Xscan Tosca selects the engine which it scans the application. 
> You can select Ignore Application to excludes an application from showing in Select Application screen.

 #BasicScan : allows to select an individual controls in the test objects select or deslects them in the Xcan window.

#AdvancedView:Can select the controls to steer, The icons next to the controls indicates the identification criteria used. 

#Xmodules: Engines 3.0 use Xmodules to steer test controls. The XModule contain all required technical information to interact with the system under test. Xmodules and XModulesAttributes can be used repeatedly in tricentis by using References. System will adjust all references affected by these changes. There are 2 ways to Create references
- By dragging and Dropping Xmodule onto another Xmodule
- By Drapping and Dropping XmoduleAtrribute
> if Xmodules is marked as abstract modules, it can not be used as Testcase. (`IsAbract = True`)


Type of Modules
Typically there are 2 types of Modules:
- Modules you create by `Scanning your system under test`
- Modules from the `Standard Subset`
> TBOX automation Tools modules in the standard subset contains Xmodules that allow you to perform special tasks.

The folder has the following Sub-Folders
- Basic Windows Operations: Steer Windows dialog, context menus take screenshots or perform clipboard operations
- Buffer Operation: Save values to buffers.
- Expression Evaluation: Perform comparisons
- File operation: Create, read copy compare move rename delete files, verify the existence of files or append the files names
- Folder operations: Copy delete create or verify the existence of folders
- Numeric Operators : convert Decimal Formats
- Process Operations : Open an applications or an executable file.
- Resource Handling : Delete resources
- Test Scripts: Start test Scripts directly from Tosca Commander
- Timing: Measure execution time or set wait times

>Value : {B[A] > 100} && B[A] <200::
>ActionMode : Verify  
>Explanation:  Step verify whether buffer A contains a value greater than 100 and less than 200
> Value 

ActionMode: Input: , (In values use {F6} to press Special key 6 , `ALTCLICK`,  LWIN, RWIN, APPS , {SENDKEYS["{(}ABC{)"]} note: " double quote is escape special characters '{' and '}'
`{RND[Lower limit][Upper limit]}`
`{RNDDECIMAL[Length of random number][Decimal places]}`
`{RNDDECIMAL[Decimal places][Lower limit][Upper limit]}`
`{RANDOMTEXT[String length]}`
`{CTMSTMP}` Random unique string consist of 16 random numbers and characters based on current time stamp
`{RANDOMREGEX["Regular expression"]}`: example `{RANDOMREGEX["^[A-Z][a-z]+[0-9]{4}$"]}`
//output :Ecqwp1989




  
When you run your tests, keep the following things in mind:
- This module only removes the reference to the file in Tosca Commander. Tricentis Tosca doesn't delete the file itself.
- If the specified resources exists and can be deleted, the associated test passes.
- If the specified resources exists but can't be deleted the associate test fails
- if the specified resources doesn't exist, the associated test passses.

The ScratchBook allows you to perform trial runs of your TestCases. You can combine and run the following objects: individual TestSteps, TestCases or TestCase folders. This is particularly helpful when you build a new TestCase or want to examine elements of a failing TestCase.

However, unlike with [ExecutionLists](https://documentation.tricentis.com/tosca/2320/en/content/tosca_commander/execution_lists_section.htm), Tosca Commander does not save the structure you create in the ScratchBook, nor does it store the results.



![[Pasted image 20240823112020.png]]
![[Pasted image 20240823112353.png]]