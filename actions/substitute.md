### SUBSTITUTE
The SUBSTITUTE action replaces all or part of the data, content or payload in the least detectable manner.

SUBSTITUTE is used in cases where an attack is to be impeded or thwarted in an undetectable manner.

**Table. Supported Targets and Actuators: SUBSTITUTE**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:File<br>cybox:Network_Connection |  | endpoint<br>network.router | 

The SUBSTITUTE action accepts the following modifiers:

**Table. Modifiers: SUBSTITUTE**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| options |  | Additional options that specify what to replace and replace with what. | All | 

Below is a sample of OpenC2 commands to perform a SUBSTITUTE of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: SUBSTITUTE**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Overwrite data | SUBSTITUTE | cybox:File<hr>cybox:FileObjectType | endpoint<hr>(optional) | options | 
| 2 | Substitute traffic | SUBSTITUTE | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.router<hr>(optional) | options | 

