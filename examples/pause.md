### PAUSE
**Table. Example Actions: PAUSE**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Pause device (system) | PAUSE | cybox:System<hr>cybox:SystemObjectType | <hr> | [method = sleep] | 
| 2 | Hibernate device (system) | PAUSE | cybox:System<hr>cybox:SystemObjectType | <hr> | method = hibernate | 
| 3 | Pause VM | PAUSE | cybox:System<hr>cybox:SystemObjectType | process.virtualization-service<hr>(optional) |  | 
| 4 | Pause a system or VM for a specified duration | PAUSE | cybox:System<hr>cybox:SystemObjectType | <hr> | duration = <DURATION> | 
| 5 | Pause process | PAUSE | cybox:Process<hr>cybox:ProcessObjectType | endpoint<hr>(optional) |  | 
| 6 | Pause a process for a specified duration | PAUSE | cybox:Process<hr>cybox:ProcessObjectType | endpoint<hr>(optional) | duration = <DURATION> | 

