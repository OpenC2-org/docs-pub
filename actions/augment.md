### AUGMENT
The AUGMENT action tasks the sensor to do a level of preprocessing or sense making prior to sending the sensor data.

The means of augmentation and the source of additional data are indicated by a specifier.

**Table. Supported Targets and Actuators: AUGMENT**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:Network_Connection |  | network.sensor | 

The AUGMENT action accepts the following modifiers:

**Table. Modifiers: AUGMENT**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| method | enumeration | The specific augmentation function to perform on the network traffic. | cybox:Network_Connection | 

Below is a sample of OpenC2 commands to perform an AUGMENT of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: AUGMENT**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Preprocess network traffic, inter-enclave | AUGMENT | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> | method | 
| 2 | Preprocess network traffic, within an enclave | AUGMENT | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.sensor<hr>(optional) | method | 

