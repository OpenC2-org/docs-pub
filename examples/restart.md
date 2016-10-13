### RESTART
**Table. Example Actions: RESTART**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Restart device (system) | RESTART | cybox:System<hr>cybox:SystemObjectType | <hr> |  | 
| 2 | Restart device (system) with different OS | RESTART | cybox:System<hr>cybox:SystemObjectType | <hr> | options, e.g., OS | 
| 3 | Restart VM | RESTART | cybox:System<hr>cybox:SystemObjectType | process.virtualization-service<hr>(optional) |  | 
| 4 | Restart process | RESTART | cybox:Process<hr>cybox:ProcessObjectType | endpoint<hr>(optional) |  | 

