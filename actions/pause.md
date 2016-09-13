### PAUSE
The PAUSE action ceases a system or activity while maintaining state.

A PAUSE remains in effect until a RESUME is issued, unless the PAUSE action is accompanied by modifier for a time-interval.

**Table. Supported Targets and Actuators: PAUSE**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:System<br>cybox:Process |  | process.virtualization-service<br>endpoint | 

The PAUSE action accepts the following modifiers:

**Table. Modifiers: PAUSE**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| duration | duration | Optional. The time to wait until returning to the previous state. | All | 
| method | enumeration: sleep, hibernate, suspend | Optional. When there is more than one way to perform the action, the method can be specified, if necessary. | All | 

Below is a sample of OpenC2 commands to perform a PAUSE of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: PAUSE**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Pause device (system) | PAUSE | cybox:System<hr>cybox:SystemObjectType | <hr> | [method = sleep] | 
| 2 | Hibernate device (system) | PAUSE | cybox:System<hr>cybox:SystemObjectType | <hr> | method = hibernate | 
| 3 | Pause VM | PAUSE | cybox:System<hr>cybox:SystemObjectType | process.virtualization-service<hr>(optional) |  | 
| 4 | Pause a system or VM for a specified duration | PAUSE | cybox:System<hr>cybox:SystemObjectType | <hr> | duration = <DURATION> | 

