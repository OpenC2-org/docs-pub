### DELAY
The DELAY action stops or holds up an activity or data transmittal.
The period of time for the delay can be specified in a modifier to the DELAY action.

**Table. Supported Targets and Actuators: DELAY**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:Network_Connection |  |  | 

The DELAY action accepts the following modifiers:

**Table. Modifiers: DELAY**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| delay | time | Required.  The time delay to add to a network connection. |  | 

Below is a sample of OpenC2 commands to perform a DELAY of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate. These samples are intended to show the flexibility of the OpenC2 language. A fuller set of example usages can be found in Appendix A.

**Table. Sample of OpenC2 Commands: DELAY**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Delay all traffic | DELAY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> | delay | 
