### THROTTLE
The THROTTLE action adjusts the throughput of a data flow.

**Table. Supported Targets and Actuators: THROTTLE**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:Network_Connection |  | network.router | 

The THROTTLE action accepts the following modifiers:

**Table. Modifiers: THROTTLE**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| None to Date |  |  |  | 

Below is a sample of OpenC2 commands to perform a THROTTLE of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: THROTTLE**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Limit bandwidth | THROTTLE | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.router<hr>(optional) |  | 

