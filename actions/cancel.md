### CANCEL
The CANCEL action invalidates a previously issued action.

CANCEL must be associated with a previously issued command through the "command-ref" modifier. This action should not be considered an undo. It can set the validity period to immediately end or it could define a future duration for which the action is valid.

**Table. Supported Targets and Actuators: CANCEL**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| openc2:Command |  | endpoint<br>network<br>process | 

The CANCEL action accepts the following modifiers:

**Table. Modifiers: CANCEL**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| command-ref | string | The reference to the associated command that is to be cancelled. | openc2:Command | 
| duration | duration | Optional. The period of time that an action is valid. If not present, the CANCEL operation should occur immediately. | openc2:Command | 

Below is a sample of OpenC2 commands to perform a CANCEL of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: CANCEL**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Cancel a previously issued command | CANCEL | openc2:Command<hr>openc2:CommandObjectType | <hr> | command-ref = command reference | 
| 2 | Cancel a previously issued command, directed to a specific actuator (endpoint) | CANCEL | openc2:Command<hr>openc2:CommandObjectType | endpoint<hr>(optional) | command-ref = command reference | 

