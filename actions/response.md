### RESPONSE
RESPONSE is used to provide any data requested as a result of an action. RESPONSE can be used to signal the acknowledgement of an action, provide the status of an action along with additional information related to the requested action, or signal the completion of the action. The recipient of the RESPONSE can be the original requester of the action or to another recipient(s) designated in the modifier of the action.

The RESPONSE action accepts the following modifiers:

**Table. Modifiers: RESPONSE**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| command-ref |  | The reference to the associated command that is in response to. | N/A | 
| type | enumeration: acknowledgement, status, query | The type of response. | N/A | 
| value |  | The value of the response. | N/A | 

Below is a sample of OpenC2 commands to perform a RESPONSE of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: RESPONSE**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Acknowledge the receipt of an action | RESPONSE | <hr> | <hr> | type = acknowledge,<br>command-ref = command reference | 
| 2 | Signal completion of an action | RESPONSE | <hr> | <hr> | type = status,<br>value = complete,<br>command-ref = command reference | 
| 3 | Provide the status of an action | RESPONSE | <hr> | <hr> | type = status,<br>value = current,<br>command-ref = command reference | 

