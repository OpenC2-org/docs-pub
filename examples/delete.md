### DELETE
**Table. Example Actions: DELETE**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Delete file, inter-enclave | DELETE | cybox:File<hr>cybox:FileObjectType | <hr> |  | 
| 2 | Delete file, within an enclave | DELETE | cybox:File<hr>cybox:FileObjectType | endpoint<hr>(optional) |  | 
| 3 | Delete email, inter-enclave | DELETE | cybox:Email_Message<hr>cybox:EmailMessageObjectType | <hr> |  | 
| 4 | Delete email from exchange server | DELETE | cybox:Email_Message<hr>cybox:EmailMessageObjectType | process.email-service<hr>(optional) |  | 
| 5 | Delete firewall rule | DELETE | openc2:Data<hr>openc2:DataObjectType | network.firewall<hr>(optional) |  | 
| 6 | Delete srp | DELETE | openc2:Data<hr>openc2:DataObjectType | <hr> |  | 

