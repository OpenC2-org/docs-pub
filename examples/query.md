### QUERY
**Table. Example Actions: QUERY**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | List all network connections | QUERY | openc2:Data<hr>openc2:DataObjectType | network.router<hr>(optional) | response | 
| 2 | List running processes on a machine | QUERY | openc2:Data<hr>openc2:DataObjectType | endpoint<hr>(optional) | response | 
| 3 | Request an Actuator's supported OpenC2 capabilities | QUERY | openc2:OpenC2<hr>openc2:OpenC2ObjectType | network.firewall<hr>(optional) | response | 
| 4 | Get attributes of a user | QUERY | openc2:Data<hr>openc2:DataObjectType | process.directory-service<hr>(optional) | response | 
| 5 | List all alerts configured on the device | QUERY | openc2:Data<hr>openc2:DataObjectType | endpoint<hr>(optional) | response | 
| 6 | List all endpoint applications/sensors configured on the device | QUERY | openc2:Data<hr>openc2:DataObjectType | endpoint<hr>(optional) | response | 
| 7 | Get current running configuration of the device | QUERY | openc2:Data<hr>openc2:DataObjectType | endpoint<hr>(optional) | response | 

