Testing is set of activities that attempt to find error in the system 

## Principles of Testing 

- Testing should be exhaustive and optimized 
- Testing should be considered creative and not simple as it need domain knowledge and knowledge of methods 
- Testing should be independent and without assumption 
- Testing should have more focus on defect prevention along with defect detection. 
- Testing must be planned activity. 
- Testing should be risked based 
- Testing should be considered based on documented expected result.

## Anomaly
According IEEE guidde [1044-1-1995] describes the standard for the classification of the software anomolies.
1. Error: a discrepancy between a computed or observed value or condition 
2. Bug : A catchall term for all software  
3. Fault: A fault in program which cause the program in an unintended manner.


## Standard 9126

Std-9126 is standard for the evaluation of the software. This distinguish between the defect a non-conformity. 
Defect is the non-fulfilment of intended of intended usage requirement while the nonconformity is the nonfulfillment of specified requirement. 
Quality model (9126-1) classifies quality in structured set and sub-characteristic.

|                 |                                                                                                                                                                                                               |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Functionality   | Set of attributes that bears on the existence of set of functions and their specified stated or implied needs. <br><br>Example: Accuracy, Compliance, Security, Suitability, Interoperability.                |
| Reliability     | A set of attribute that bear on the capability of software to maintain its level of performance under stated condition for stated period of time. <br><br>Example: Maturity, Recoverability, Fault tolerance. |
| Usability       | A set of attributes that bear on effort to use and on individual assessment of such use, by stated or implied set of users. <br><br>Example: Understandability, learnability and operability.                 |
| Efficiency      | A set of attribute that bear on relationship between the level of performance of software and the amount of resource used under stated condition. <br><br>Example: Time behaviour and resource behaviour      |
| Maintainability | A set of attributes that bear on the effort needed to make specified modification.  <br><br>Example: stability, Analysability, changeability, and Testability                                                 |
| Portability     | A set of attributes that bear on ability of software to be transferred from one environment to another.  <br><br>Example:  Instability, Replaceability, Co-existence and Adaptability.                        |
|                 |                                                                                                                                                                                                               |

## Quality

The concept of Quality establishes the foundation for an understanding of continuous process improvement. 

There are multiple quality philosophies documented for quality. 

Peter & Scholtes introduces the contract between effectiveness and efficiency, where effectiveness is doing the right things and efficiency means doing things rights. 

And so they concluded that Quality Organization must be effective and efficient. 

Patrick Townsend examines quality in fact and perception. Quality in fact is usually the supplier point of view while quality in perception is the customer view 

| Quality in Fact                                                                                                                          | Quality in Perception                                                                                                                       |
| ---------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. Doing the right things <br>    <br>2. Doing it the right way <br>    <br>3. Doing it right first time <br>    <br>4. Doing in on time | 1. Delivering right product <br>    <br>2. Meeting expectation <br>    <br>3. Treating every customer with integrity, courtesy and respect. |

Above than just absence of defect, Quality is meeting customer requirement (Effectiveness) and following controlled process to improve efficiency internally. This can make customer loyal. 

Excellence is the measure/degree of quality. 

For any organization defining Quality and Excellence should be important and first step.  

Dr. Deming  stated that quality improves productivity, which leads to an improved competitive position and ensure that the organization will stay in business. As there will be pressure of doing more with less, only effective action will be to improve productivity by improving quality of its process. Because Quality reduces the cost 

Michael Tveite regrouped Deming points into 3 themes 

- Theme1 ' Purposes' :-      
    - Stop focusing on judgement result and start focusing on          
    - Start focusing on (1) creating constancy of purpose and (14) put everybody to work to accomplishing the transformation          

- Theme2 'Leadership':- 
	 - Stop: (11) Eliminate numerical goals and quote, (12) Remove barriers to pride of work force. (12)drive out fear 
	 - Start (7) institute leadership        

- Theme3 'Co-operation':-     
	- Stop: (9) Breakdown barrier bets department (4) End the practise of awarding business on the basis of price along.
	- Start (2) Adopt a new philosophy. 
        
    

Quality Assurance Versus Quality Control: 

Quality methods can be segmented into two categories preventive methods and detective methods. This distinction serve as the mechanism used to distinguish quality assurance activities from Quality control activities. 

Quality Assurance is planned and systematic set of activities necessary to provide adequate confidence that product and service will conform to specified requirement.  

QA helps in establish, evaluate process is responsibility of management. 

QA Responsibility is to implement the quality policy defined through the development and continuous improvement of development process 

QA Activities: 

- System development methodologies      
- Estimation process     
- System maintenance process     
- Requirements definition process      
- Testing Process and standards.     

Quality Control is process by which product quality is compared with the applicable standards and the actions taken when non-conformance is detected. 

QC responsibility is to ensure that the work product conform to standard and requirement under the process compliance. 

QC help compliance to process, evaluate product/service and it is responsibility of execution team. 

QC Activities: 

- Identifying defects in actual product. 
    
- Starting from reviewing requirement to testing of the developed product. 
    

Audit is independent activity to review the operation and service to management. By audit management evaluate the effectiveness of the other control.

Verification Vs Validation:


| Verification                                                                                                                                  | Validation                                                                                                                          |
| --------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| Ensures the system complies with an organization standard and process through review methods.                                                 | Validation is ensuring the system operates according to plan by executing the system functionality through a series or checks/tests |
| Verification method requires several types of reviews like walkthrough, code-inspection, design reviews. It can catch defect before it occur. | It is accomplished by executing or using the product/service in real-like scenarios.                                                |
| Did we build the right system                                                                                                                 | Did we build system right.                                                                                                          |
| Verification demonstrate completeness and correctness of the software at different stage                                                      | Validation determines the correction of the final product/service                                                                   |
| Verification is Detailed level or unit level activity                                                                                         | Validation is high level activity. It includes unit, integration, system and User Acceptance Testing                                |


Automation Tools

1. [[AutomationTool/Cypress]]  #javascript
2. [[Playwright_py]] #javascript  #python #java #csharp
3. [[k6]] #javascript 
4. [[Selenium]]


