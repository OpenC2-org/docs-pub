### DISTILL
The DISTILL action tasks the sensor to send a summary or abstraction of the sensing information instead of the raw data feed.
The DISTILL action reduces the amount of sensor data.  The means of reduction or filtering is indicated by a specifier.

**Table. Supported Targets and Actuators: DISTILL**

| cybox:Network_Connection |  | network.sensor | 

The DISTILL action accepts the following modifiers:

**Table. Modifiers: DISTILL**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| TBSL |  |  |  | 

Below is a sample of OpenC2 commands to perform a DISTILL of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate. These samples are intended to show the flexibility of the OpenC2 language. A fuller set of example usages can be found in Appendix A.

**Table. Sample of OpenC2 Commands: DISTILL**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Filter | DISTILL | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.sensor<hr> |  | 
