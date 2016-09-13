### MOVE
The MOVE action changes the location of a file, subnet, network, or, process.

MOVE is distinct from CONTAIN in that CONTAIN implies a desired effect of isolation and MOVE supports the more general case.

**Table. Supported Targets and Actuators: MOVE**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:File<br>openc2:Data |  |  | 

The MOVE action accepts the following modifiers:

**Table. Modifiers: MOVE**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| move-to |  | The location to move to | All | 

Below is a sample of OpenC2 commands to perform a MOVE of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: MOVE**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Move file/directory | MOVE | cybox:File<hr>cybox:FileObjectType | <hr> | move-to | 

