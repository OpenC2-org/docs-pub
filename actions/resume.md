### RESUME
The RESUME action starts a system or activity from a paused state.
RESUME is only meaningful after a PAUSE command.

**Table. Supported Targets and Actuators: RESUME**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:System<br>cybox:Process |  | process.virtualization-service<br>endpoint | 

The RESUME action accepts the following modifiers:

**Table. Modifiers: RESUME**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| TBSL |  |  |  | 

Below is a sample of OpenC2 commands to perform a RESUME of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate. These samples are intended to show the flexibility of the OpenC2 language. A fuller set of example usages can be found in Appendix A.

**Table. Sample of OpenC2 Commands: RESUME**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Resume device (system) | RESUME | cybox:System<hr>cybox:SystemObjectType | <hr> |  | 
| 2 | Resume VM | RESUME | cybox:System<hr>cybox:SystemObjectType | process.virtualization-service<hr>(optional) |  | 
