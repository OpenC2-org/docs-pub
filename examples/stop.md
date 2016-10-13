### STOP
**Table. Example Actions: STOP**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Shutdown a system | STOP | cybox:Device<hr>cybox:DeviceObjectType | endpoint<hr>(optional) | [method = graceful] | 
| 2 | Shutdown a system, immediate | STOP | cybox:Device<hr>cybox:DeviceObjectType | endpoint<hr>(optional) | method = immediate | 
| 3 | Logoff User: Logoff all the sessions of a particular user from the machine | STOP | cybox:User_Account<hr>cybox:UserAccountObjectType | endpoint<hr>(optional) | [method = graceful] | 
| 4 | Stop a vm | STOP | cybox:System<hr>cybox:SystemObjectType | process.virtualization-service<hr>(optional) | [method = graceful] | 
| 5 | Terminate a process, general | STOP | cybox:Process<hr>cybox:ProcessObjectType | <hr> |  | 
| 6 | Terminate a process | STOP | cybox:Process<hr>cybox:ProcessObjectType | endpoint<hr>(optional) |  | 
| 7 | Stop service | STOP | cybox:Windows_Service<hr>cybox:WindowsServiceObjectType | endpoint<hr>(optional) |  | 
| 8 | Terminate a session | STOP | cybox:User_Session<hr>cybox:UserSessionObjectType | process.aaa-server<hr>(optional) |  | 
| 9 | Shutdown a system, general | STOP | cybox:Device<hr>cybox:DeviceObjectType | <hr> |  | 
| 10 | Disable Device | STOP | cybox:Device<hr>cybox:DeviceObjectType | network<hr>(optional) | method = disable | 
| 11 | Deactivate Partition: Deactivates the system partitions of a machine. Disallows booting from the specified partition | STOP | cybox:Disk_Partition<hr>cybox:DiskPartitionObjectType | endpoint<hr>(optional) |  | 
| 12 | Logoff User: Logoff all the sessions of a particular user, general | STOP | cybox:User_Account<hr>cybox:UserAccountObjectType | <hr> |  | 
| 13 | Logoff User: Logoff all the sessions of a particular user from the machine, immediate | STOP | cybox:User_Account<hr>cybox:UserAccountObjectType | endpoint<hr>(optional) | method = immediate | 
| 14 | Stop a vm, immediate | STOP | cybox:System<hr>cybox:SystemObjectType | process.virtualization-service<hr>(optional) | method = immediate | 

