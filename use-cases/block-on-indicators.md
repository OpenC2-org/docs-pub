## Use Case: Block on Indicators
### Description
TBSL

**Table. Scenario Diagram: Block on Indicators**

![alt text](https://github.com/OpenC2-org/docs-members/blob/master/use-cases/block-on-indicators.png "Use Case Diagram")


**Table. Scenario Steps: Block on Indicators**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 |  |  | <hr> | <hr> |  | 
| 2 | External Enclave shares threat intelligence with lower tier. Alternative: External Enclave coordinates a specific COA to the Enclave to Block on Indicators. | MITIGATE | data.indicator<hr>id = <INDICATOR_ID>,<br>indicator = <BLOB> | <hr> |  | 
| 3 | Sense-Making forwards the indicators of compromise or COA to Decision-Making. |  | <hr> | <hr> |  | 
| 4 | Decision-Making commands Acting to confirm indicators of compromise. | SCAN | data.indicator<hr>id = <INDICATOR_ID>,<br>indicator = <BLOB> | <hr> |  | 
| 5 | Acting queries Sense-Making to confirm indicators of compromise. | SCAN | data.indicator<hr>id = <INDICATOR_ID>,<br>indicator = <BLOB> | <hr> |  | 
| 6 | Sense-Making scans for occurrence of indicators already within the Enclave. |  | <hr> | <hr> |  | 
| 7 | Sense-Making sends occurance information to Decision-Making. |  | <hr> | <hr> |  | 
|  | ALTERNATIVE A:<br>The occurrence of indicator was negative. |  | <hr> | <hr> |  | 
| 8 | Decision-Making commands Acting to block on indicators. | DENY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> |  | 
| 9 | (At this point, the scenario resembles the flow of "Mitigate Evil Domain".) |  | <hr> | <hr> |  | 
|  | ALTERNATIVE B:<br>The occurrence of indicator was found. |  | <hr> | <hr> |  | 
| 10a | Decision-Making commands Acting <br>- to notify appropriate administrators,  | NOTIFY | cybox:User_Account<hr>cybox:UserAccountObjectType | <hr> |  | 
| 10b | - investigate the cause of the compromise, | INVESTIGATE | cybox:Process<hr>cybox:ProcessObjectType | <hr> |  | 
| 10c | - and restore the compromised hosts to a good state. | REMEDIATE | cybox:Process<hr>cybox:ProcessObjectType | <hr> |  | 
| 11 | (At this point, the scenario resembles the flow of "Host Remediation".) |  | <hr> | <hr> |  | 

