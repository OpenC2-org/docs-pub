### STOP
The STOP action halts a system or ends an activity.

The STOP OpenC2 action is used to convey terms in current use such as shutdown, kill, and terminate. The STOP action has nuances and options associated with it that are ACTUATOR specific. In the case where more than one type of STOP action is applicable for a particular target and actuator, if practical, the default implementation of STOP will be a graceful shutdown. Action modifiers are used to indicate immediate or atypical STOP actions.

**Table. Supported Targets and Actuators: STOP**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:Device<br>cybox:User_Account<br>cybox:System<br>cybox:Process<br>cybox:Windows_Service<br>cybox:User_Session<br>cybox:Disk_Partition |  | endpoint<br>process.virtualization-service<br>process.aaa-server<br>network | 

The STOP action accepts the following modifiers:

**Table. Modifiers: STOP**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| method | enumeration: graceful, immediate | Optional. When there is more than one way to perform the action, the method can be specified, if necessary. | All | 

Below is a sample of OpenC2 commands to perform a STOP of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: STOP**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Shutdown a system | STOP | cybox:Device<hr>cybox:DeviceObjectType | endpoint<hr>(optional) | [method = graceful] | 
| 2 | Shutdown a system, immediate | STOP | cybox:Device<hr>cybox:DeviceObjectType | endpoint<hr>(optional) | method = immediate | 
| 3 | Logoff User: Logoff all the sessions of a particular user from the machine | STOP | cybox:User_Account<hr>cybox:UserAccountObjectType | endpoint<hr>(optional) | [method = graceful] | 
| 4 | Stop a vm | STOP | cybox:System<hr>cybox:SystemObjectType | process.virtualization-service<hr>(optional) | [method = graceful] | 

