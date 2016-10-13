### UPDATE
**Table. Example Actions: UPDATE**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Install software | UPDATE | cybox:Product<hr>cybox:ProductObjectType | endpoint<hr>(optional) | source | 
| 2 | Install patch | UPDATE | cybox:Product<hr>cybox:ProductObjectType | endpoint<hr>(optional) | source | 
| 3 | Update signature file (anti-virus) | UPDATE | cybox:Product<hr>cybox:ProductObjectType | process.anti-virus-scanner<hr>(optional) | source | 
| 4 | Update sensor's signatures | UPDATE | cybox:Product<hr>cybox:ProductObjectType | network.sensor<hr>(optional) | source | 
| 5 | Load Machine Settings | UPDATE | cybox:Device<hr>cybox:DeviceObjectType | endpoint<hr>(optional) | source | 
| 6 | Synchronize Machine | UPDATE | cybox:Device<hr>cybox:DeviceObjectType | endpoint<hr>(optional) | source | 
| 7 | Update Registry | UPDATE | cybox:Device<hr>cybox:DeviceObjectType | endpoint<hr>(optional) | source | 
| 8 | Load File(s) | UPDATE | cybox:Device<hr>cybox:DeviceObjectType | endpoint<hr>(optional) | source | 

