### ALERT
ALERT is used to signal the occurrence of an event.

The ALERT action accepts the following modifiers:

**Table. Modifiers: ALERT**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| type | enumeration | The type of alert. | N/A | 
| value |  | Additional data associated with the alert. | N/A | 

Below is a sample of OpenC2 commands to perform an ALERT of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: ALERT**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | An actuator sends an alert as the result of some condition. | ALERT | <hr> | <hr> | type, value | 
| 2 | A sensor sends an alert as the result of some condition. | ALERT | <hr> | <hr> | type, value | 

