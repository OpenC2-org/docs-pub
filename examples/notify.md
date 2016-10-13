### NOTIFY
**Table. Example Actions: NOTIFY**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Notify security officer to report compliance with change of configuration | NOTIFY | cybox:User_Account<hr>cybox:UserAccountObjectType | process.email-service<hr>(optional) | message | 
| 2 | Send a command to notify an external enclave | NOTIFY | cybox:System<hr>cybox:SystemObjectType | <hr> | message = acknowledge | 
| 3 | Send a command to notify an authorized user to request approval | NOTIFY | cybox:User_Account<hr>cybox:UserAccountObjectType | endpoint.server<hr> | message | 

