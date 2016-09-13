### MODIFY
The MODIFY action augments, enhances, transforms, or changes some aspect of a system.

MODIFY is used to change the attributes or behavior of some system element without stopping it or removing it from the system. MODIFY is a superset of commands such as set and rename.

**Table. Supported Targets and Actuators: MODIFY**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:File<br>cybox:Device<br>cybox:User_Account<br>cybox:Process<br>cybox:Product<br>cybox:System |  | endpoint<br>process.directory-service | 

The MODIFY action accepts the following modifiers:

**Table. Modifiers: MODIFY**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| modify-to |  | The new value resulting from the modification | All | 

Below is a sample of OpenC2 commands to perform a MODIFY of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: MODIFY**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Modify a file | MODIFY | cybox:File<hr>cybox:FileObjectType | <hr> | modify-to | 
| 2 | Modify a device's configuration | MODIFY | cybox:Device<hr>cybox:DeviceObjectType | endpoint<hr>(optional) | modify-to | 
| 3 | Modify user account privileges | MODIFY | cybox:User_Account<hr>cybox:UserAccountObjectType | process.directory-service<hr>(optional) | modify-to | 

