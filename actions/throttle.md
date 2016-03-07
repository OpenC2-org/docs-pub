### THROTTLE
The THROTTLE action adjusts the throughput of entire data flow to a different  rate. 

**Table. Supported Targets and Actuators: THROTTLE**

| cybox:Network_Connection |  | network.router | 

The THROTTLE action accepts the following modifiers:

**Table. Modifiers: THROTTLE**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| TBSL |  |  |  | 

Below is a sample of OpenC2 commands to perform a THROTTLE of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate. These samples are intended to show the flexibility of the OpenC2 language. A fuller set of example usages can be found in Appendix A.

**Table. Sample of OpenC2 Commands: THROTTLE**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Limit bandwidth | THROTTLE | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.router<hr>(optional) |  | 
