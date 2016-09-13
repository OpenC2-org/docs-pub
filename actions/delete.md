### DELETE
The DELETE action removes data and files.

**Table. Supported Targets and Actuators: DELETE**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:File<br>cybox:Email_Message<br>openc2:Data |  | endpoint<br>process.email-service<br>network.firewall | 

The DELETE action accepts the following modifiers:

**Table. Modifiers: DELETE**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| None to Date |  |  |  | 

Below is a sample of OpenC2 commands to perform a DELETE of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: DELETE**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Delete file, inter-enclave | DELETE | cybox:File<hr>cybox:FileObjectType | <hr> |  | 
| 2 | Delete file, within an enclave | DELETE | cybox:File<hr>cybox:FileObjectType | endpoint<hr>(optional) |  | 
| 3 | Delete email, inter-enclave | DELETE | cybox:Email_Message<hr>cybox:EmailMessageObjectType | <hr> |  | 
| 4 | Delete email from exchange server | DELETE | cybox:Email_Message<hr>cybox:EmailMessageObjectType | process.email-service<hr>(optional) |  | 

