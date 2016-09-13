### SAVE
The SAVE action commits data or system state to memory.

**Table. Supported Targets and Actuators: SAVE**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:File<br>cybox:Email_Message<br>cybox:Network_Packet |  | endpoint<br>process.email-service<br>network.router | 

The SAVE action accepts the following modifiers:

**Table. Modifiers: SAVE**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| save-to |  | The location to save to. | All | 

Below is a sample of OpenC2 commands to perform a SAVE of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: SAVE**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Save data | SAVE | cybox:File<hr>cybox:FileObjectType | endpoint<hr>(optional) | save-to | 
| 2 | Save an email message | SAVE | cybox:Email_Message<hr>cybox:EmailMessageObjectType | process.email-service<hr>(optional) | save-to | 
| 3 | Save a raw network packet | SAVE | cybox:Network_Packet<hr>cybox:NetworkPacketObjectType | network.router<hr>(optional) | save-to | 

