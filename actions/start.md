### START
The START action initiates a process, application, system or some other activity.

**Table. Supported Targets and Actuators: START**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:Process<br>cybox:Product<br>cybox:System<br>cybox:Disk_Partition |  | endpoint<br>network<br>process.virtualization-service | 

The START action accepts the following modifiers:

**Table. Modifiers: START**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| delay | duration | Optional. The time to wait before performing the action. | All | 
| method | enumeration: spawn |  | cybox:Process | 

Below is a sample of OpenC2 commands to perform a START of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: START**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Start Process, general | START | cybox:Process<hr>cybox:ProcessObjectType | <hr> |  | 
| 2 | Start Process | START | cybox:Process<hr>cybox:ProcessObjectType | endpoint<hr>(optional) |  | 
| 3 | Start Process with Delay | START | cybox:Process<hr>cybox:ProcessObjectType | endpoint<hr>(optional) | delay | 
| 4 | Spawn Process | START | cybox:Process<hr>cybox:ProcessObjectType | endpoint<hr>(optional) | method = spawn | 

