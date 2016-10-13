### SET
**Table. Example Actions: SET**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Set registry key value | SET | cybox:Windows_Registry_Key<hr>cybox:WindowsRegistryKeyObjectType | endpoint.workstation<hr>(optional) | set-to | 
| 2 | Set file permissions | SET | cybox:File<hr>cybox:FileObjectType | process.directory-service<hr>(optional) | set-to | 
| 3 | Set user rights | SET | cybox:User_Account<hr>cybox:UserAccountObjectType | process.directory-service<hr>(optional) | set-to | 
| 4 | Set password policy | SET | cybox:System<hr>cybox:SystemObjectType | process.directory-service<hr>(optional) | set-to | 
| 5 | Set auditing policy | SET | cybox:System<hr>cybox:SystemObjectType | <hr> | set-to | 
| 6 | Set registry permissions | SET | cybox:Windows_Registry_Key<hr>cybox:WindowsRegistryKeyObjectType | endpoint.workstation<hr>(optional) | set-to | 
| 7 | Set service permissions | SET | cybox:Process<hr>cybox:ProcessObjectType | <hr> | set-to | 
| 8 | Set group policy (computer, user) | SET | cybox:System<hr>cybox:SystemObjectType | endpoint.workstation<hr>(optional) | set-to | 
| 9 | Set user settings (remediate per user instead of per computer) | SET | cybox:User_Account<hr>cybox:UserAccountObjectType | process.directory-service<hr>(optional) | set-to | 
| 10 | Change a specific value in a config file | SET | openc2:Data<hr>openc2:DataObjectType | <hr>(optional) | set-to | 
| 11 | Change firewall rule | SET | openc2:Data<hr>openc2:DataObjectType | network.firewall<hr>(optional) | set-to | 
| 12 | Change HIPS rule | SET | openc2:Data<hr>openc2:DataObjectType | network.hips<hr>(optional) | set-to | 
| 13 | Change network device rule | SET | openc2:Data<hr>openc2:DataObjectType | network.router<hr>(optional) | set-to | 
| 14 | Acting quarantines the infected Host by commanding Directory Services to set the Host's security group. (No return requested.) | SET | cybox:System<hr>cybox:SystemObjectType | process.directory-service<hr>(optional) | set-to | 
| 15 | Acting commands Directory Services to return the Host to the active group. (No return requested.) | SET | cybox:System<hr>cybox:SystemObjectType | process.directory-service<hr>(optional) | set-to | 
| 16 | [Alternative] Mitigation Manager sends an OpenC2 command containing the configuration update (signatures) | SET | openc2:Data<hr>openc2:DataObjectType | network.sensor<hr>(optional) | set-to | 
| 17 | Change system ou | SET | openc2:Data<hr>openc2:DataObjectType | <hr> | set-to | 
| 18 | Set system attribute | SET | openc2:Data<hr>openc2:DataObjectType | <hr> | set-to | 
| 19 | Set/reset password | SET | cybox:User_Account<hr>cybox:UserAccountObjectType | <hr> | set-to | 
| 20 | Change machine settings | SET | openc2:Data<hr>openc2:DataObjectType | <hr> | set-to | 
| 21 | Change desktop settings | SET | openc2:Data<hr>openc2:DataObjectType | <hr> | set-to | 
| 22 | Change device IP | SET | openc2:Data<hr>openc2:DataObjectType | <hr> | set-to | 
| 23 | Change device MAC | SET | openc2:Data<hr>openc2:DataObjectType | <hr> | set-to | 
| 24 | Change sensor sample rate | SET | openc2:Data<hr>openc2:DataObjectType | <hr> | set-to | 
| 25 | Limit connections to process | SET | openc2:Data<hr>openc2:DataObjectType | <hr> | set-to | 

