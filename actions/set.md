### SET
The SET action changes a value, configuration, or state of a managed entity within an IT system.

Typically this action is specified by a configuration item such as a sensor setting or privilege level and the command will have specifiers. SET commands are intended for specific individual changes to the entity and the parameters are communicated in the C2 channel.

**Table. Supported Targets and Actuators: SET**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:Windows_Registry_Key<br>cybox:File<br>cybox:User_Account<br>cybox:System<br>cybox:Process<br>openc2:Data |  | endpoint.workstation<br>process.directory-service<br>network.firewall<br>network.hips<br>network.router<br>network.sensor | 

The SET action accepts the following modifiers:

**Table. Modifiers: SET**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| set-to |  | The value to set the target to. | All | 

Below is a sample of OpenC2 commands to perform a SET of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: SET**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Set registry key value | SET | cybox:Windows_Registry_Key<hr>cybox:WindowsRegistryKeyObjectType | endpoint.workstation<hr>(optional) | set-to | 
| 2 | Set file permissions | SET | cybox:File<hr>cybox:FileObjectType | process.directory-service<hr>(optional) | set-to | 
| 3 | Set user rights | SET | cybox:User_Account<hr>cybox:UserAccountObjectType | process.directory-service<hr>(optional) | set-to | 

