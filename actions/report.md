### REPORT
The REPORT action tasks an entity to provide information to a designated recipient of the information.

The REPORT action is used to request an actuator/sensor to provide certain information. Along with the REPORT action and the type of information being requested, the recipient of the information must be specified in the command. The response to a REPORT action is typically (but not necessarily) conveyed outside of the command and control channel.

**Table. Supported Targets and Actuators: REPORT**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| openc2:Data |  |  | 

The REPORT action accepts the following modifiers:

**Table. Modifiers: REPORT**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| report-to | cybox:AddressObjectType | Required. This modifier identifies where to send the report. | All | 
| frequency | duration | Optional. The frequency at which to perform the action. The value is the requested time between execution events. | All | 

Below is a sample of OpenC2 commands to perform a REPORT of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: REPORT**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Produce and send a report | REPORT | openc2:Data<hr>openc2:DataObjectType | <hr> | report-to | 

