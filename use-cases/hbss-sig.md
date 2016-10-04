## Use Case: HBSS Signature
### Description
TBSL

**Table. Scenario Diagram: HBSS Signature**

![alt text](https://github.com/OpenC2-org/docs-members/blob/master/use-cases/hbss-sig.png "Use Case Diagram")
![alt text](https://github.com/OpenC2-org/docs-members/blob/master/use-cases/hbss-sig-2.png "Use Case Diagram")


**Table. Scenario Steps: HBSS Signature**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 |  |  | <hr> | <hr> |  | 
| 2 | Cyber Security Center creates a Task Order. |  | <hr> | <hr> |  | 
| 3 | The Task Order is translated into a Course of Action. |  | <hr> | <hr> |  | 
| 4a | Cyber Security Center coordinates the Course of Action. | UPDATE | data.configuration<hr>url = <CONFIGURATION_FILE> | network.hips<hr> |  | 
| 4b |  | UPDATE | data.configuration<hr>url = <CONFIGURATION_FILE> | network.ips<hr> |  | 
| 4c |  | REPORT | openc2:Data<hr>openc2:DataObjectType | <hr> |  | 
| 5 | Sense-Making receives and validates the Course of Action; retrieves environmental conditions. |  | <hr> | <hr> |  | 
| 6 | Sense-Making sends the Course of Action, additional analytical results, and environmental conditions to Decision-Making. |  | <hr> | <hr> |  | 
| 7 | Decision-Making will evalutate the Course of Action against its operational mission and the current environmental conditions. |  | <hr> | <hr> |  | 
| 8 | Decision-Making sends Acting the command to  change the configuration of McAfee Signature 344 to 'Log'. | UPDATE | data.configuration<hr>url = <CONFIGURATION_FILE> | network.hips<hr> |  | 
| 9 | Acting contextualizes the Course of Action into an Action Plan. |  | <hr> | <hr> |  | 
| 10 | Acting issues the command to a Mitigation Manager to have Host HIPS to update configuration.   | UPDATE | data.configuration<hr>url = <CONFIGURATION_FILE> | network.hips<hr> | results_callback = <ACTING_ID> | 
| 11 | The Host HIPS executes the command to update its configuration. |  | <hr> | <hr> |  | 
| 12 | The Host HIPS sends status of successful execution to the Mitigation Manager |  | <hr><br> | <hr> |  | 
| 13 | Mitigation Manager sends the results of the execution of the OpenC2 command to Acting. | RESPONSE | openc2:Data<hr>openc2:DataObjectType | <hr> |  | 
| 14 | Acting sends the command to Network IPS to update its configuration.   The Network IPS validates the command. | UPDATE | data.configuration<hr>url = <CONFIGURATION_FILE> | network.ips<hr> | results_callback = <ACTING_ID> | 
| 15 | The Network IPS executes the command to update its configuration. |  | <hr> | <hr> |  | 
| 16 | The Network IPS sends an acknowledgement of successful execution to Acting. | RESPONSE | openc2:Data<hr>openc2:DataObjectType | <hr> |  | 
| 17 | Acting notifies the Security Officer to report compliance with change of configuration. | NOTIFY | cybox:User_Account<hr>cybox:UserAccountObjectType | process.email-service<hr> | report compliance of action <UUID> to cyber security center | 
| 18 | Security Officer is notified. |  | <hr> | <hr> |  | 

