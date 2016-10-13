### CONTAIN
**Table. Example Actions: CONTAIN**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Quarantine a file, general | CONTAIN | cybox:File<hr>cybox:FileObjectType | <hr> |  | 
| 2 | Quarantine a file | CONTAIN | cybox:File<hr>cybox:FileObjectType | endpoint<hr>(optional) | where | 
| 3 | Contain a user or group, general | CONTAIN | cybox:User_Account<hr>cybox:UserAccountType | <hr> |  | 
| 4 | Contain network traffic to a honeynet, general | CONTAIN | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> |  | 
| 5 | Isolate a process, general | CONTAIN | cybox:Process<hr>cybox:ProcessObjectType | <hr> |  | 
| 6 | Isolate a process | CONTAIN | cybox:Process<hr>cybox:ProcessObjectType | endpoint<hr>(optional) | where | 
| 7 | Quarantine a device, general | CONTAIN | cybox:Device<hr>cybox:DeviceObjectType | <hr> |  | 
| 8 | Quarantine a device | CONTAIN | cybox:Device<hr>cybox:DeviceObjectType | network<hr>(optional) | where (network segment, vlan) | 
| 9 | Contain a user or group | CONTAIN | cybox:User_Account<hr>cybox:UserAccountType | network<hr>(optional) | where | 
| 10 | Contain network traffic to a honeynet | CONTAIN | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network<hr>(optional) | where | 

