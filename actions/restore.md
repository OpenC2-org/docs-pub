### RESTORE
The RESTORE action deletes and/or replaces files, settings, or attributes such that the state of the system is identical to its state at some previous time.

The RESTORE could impact the whole system or return the state of an application or program to its previous state. RESTORE can be used to undo a previous action.

**Table. Supported Targets and Actuators: RESTORE**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:Device |  | process.remediation-service | 

The RESTORE action accepts the following modifiers:

**Table. Modifiers: RESTORE**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| restore-point |  | Required. The specific restore point to restore to. | All | 

Below is a sample of OpenC2 commands to perform a RESTORE of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: RESTORE**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Restore a device to a known restore point. | RESTORE | cybox:Device<hr>cybox:DeviceObjectType | process.remediation-service<hr>(optional) | restore-point | 

