### NOTIFY
The NOTIFY action is used to direct an entity to send information to another entity.

NOTIFY is distinct from REPORT in that NOTIFY is used for time sensitive event notification and carries a sense of persistence.

**Table. Supported Targets and Actuators: NOTIFY**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:User_Account<br>cybox:System |  | process.email-service<br>endpoint.server | 

The NOTIFY action accepts the following modifiers:

**Table. Modifiers: NOTIFY**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| message |  | The intended message to notify the target. | All | 
| frequency | duration | Optional. The frequency at which to perform the action. The value is the requested time between execution events. | All | 

Below is a sample of OpenC2 commands to perform a NOTIFY of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: NOTIFY**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Notify security officer to report compliance with change of configuration | NOTIFY | cybox:User_Account<hr>cybox:UserAccountObjectType | process.email-service<hr>(optional) | message | 
| 2 | Send a command to notify an external enclave | NOTIFY | cybox:System<hr>cybox:SystemObjectType | <hr> | message = acknowledge | 

