### CONTAIN
The CONTAIN action stipulates the isolation of a file or process or entity such that it cannot modify or access assets or processes that support the business and/or operations of the enclave.

The CONTAIN action is a superset of currently used terms such as ISOLATE, QUARANTINE or SANDBOX.  

**Table. Supported Targets and Actuators: CONTAIN**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:File<br>cybox:User_Account<br>cybox:Network_Connection<br>cybox:Process<br>cybox:Device |  | endpoint<br>network | 

The CONTAIN action accepts the following modifiers:

**Table. Modifiers: CONTAIN**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| where |  | Optional. The general location within the enclave to contain the target. | cybox:Device, cybox:File, cybox:Network_Connection, cybox:Process, cybox:User_Account | 

Below is a sample of OpenC2 commands to perform a CONTAIN of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: CONTAIN**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Quarantine a file, general | CONTAIN | cybox:File<hr>cybox:FileObjectType | <hr> |  | 
| 2 | Quarantine a file | CONTAIN | cybox:File<hr>cybox:FileObjectType | endpoint<hr>(optional) | where | 
| 3 | Contain a user or group, general | CONTAIN | cybox:User_Account<hr>cybox:UserAccountType | <hr> |  | 
| 4 | Contain network traffic to a honeynet, general | CONTAIN | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> |  | 

