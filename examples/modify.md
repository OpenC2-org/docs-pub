### MODIFY
**Table. Example Actions: MODIFY**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Modify a file | MODIFY | cybox:File<hr>cybox:FileObjectType | <hr> | modify-to | 
| 2 | Modify a device's configuration | MODIFY | cybox:Device<hr>cybox:DeviceObjectType | endpoint<hr>(optional) | modify-to | 
| 3 | Modify user account privileges | MODIFY | cybox:User_Account<hr>cybox:UserAccountObjectType | process.directory-service<hr>(optional) | modify-to | 
| 4 | Modify data within a process | MODIFY | cybox:Process<hr>cybox:ProcessObjectType | <hr> | modify-to | 
| 5 | Modify data within a software product | MODIFY | cybox:Product<hr>cybox:ProductObjectType | endpoint<hr>(optional) | modify-to | 
| 6 | Modify a system's configuration | MODIFY | cybox:System<hr>cybox:SystemObjectType | <hr> | modify-to | 

