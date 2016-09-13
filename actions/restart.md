### RESTART
The RESTART action conducts a STOP of a system or an activity followed by a START of a system or an activity.

A RESTART implies a graceful shutdown, maintenance of state, and a new configuration.

**Table. Supported Targets and Actuators: RESTART**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:System<br>cybox:Process |  | process.virtualization-service<br>endpoint | 

The RESTART action accepts the following modifiers:

**Table. Modifiers: RESTART**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| delay | duration | Optional. The time to wait before performing the action. | All | 
| options |  | Additional options that specify how to restart | All | 
| frequency | duration | Optional. The frequency at which to perform the action. The value is the requested time between execution events. | All | 

Below is a sample of OpenC2 commands to perform a RESTART of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: RESTART**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Restart device (system) | RESTART | cybox:System<hr>cybox:SystemObjectType | <hr> |  | 
| 2 | Restart device (system) with different OS | RESTART | cybox:System<hr>cybox:SystemObjectType | <hr> | options, e.g., OS | 
| 3 | Restart VM | RESTART | cybox:System<hr>cybox:SystemObjectType | process.virtualization-service<hr>(optional) |  | 

