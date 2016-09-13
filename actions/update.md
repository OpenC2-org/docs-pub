### UPDATE
The UPDATE action instructs the component to retrieve and process a software update, reconfiguration, or some other update.

The settings, files, patches associated with an UPDATE action are typically retrieved out of band from the control channel. UPDATE actions typically do not need to include details such as reboot or restart. It is incumbent upon the OpenC2 compliant devices to include implementation details. Modifiers such as ‘immediate’ and specifiers such as the path for the software may be added.

**Table. Supported Targets and Actuators: UPDATE**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:Product<br>cybox:Device |  | endpoint<br>process.anti-virus-scanner<br>network.sensor | 

The UPDATE action accepts the following modifiers:

**Table. Modifiers: UPDATE**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| source |  | The source of the updated information. | All | 
| frequency | duration | Optional. The frequency at which to perform the action. The value is the requested time between execution events. | All | 

Below is a sample of OpenC2 commands to perform an UPDATE of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: UPDATE**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Install software | UPDATE | cybox:Product<hr>cybox:ProductObjectType | endpoint<hr>(optional) | source | 
| 2 | Install patch | UPDATE | cybox:Product<hr>cybox:ProductObjectType | endpoint<hr>(optional) | source | 
| 3 | Update signature file (anti-virus) | UPDATE | cybox:Product<hr>cybox:ProductObjectType | process.anti-virus-scanner<hr>(optional) | source | 

