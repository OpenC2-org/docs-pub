### LOCATE
The LOCATE action is used to find an object either physically, logically, functionally, or by organization. This action enables one to tell where in the system an event or trigger occurred.

This action is used for example to enable one to tell where in the system an event or trigger occurred, confirm that an asset is appropriately deployed, or ascertain details regarding a rogue device.

**Table. Supported Targets and Actuators: LOCATE**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:Device<br>cybox:Address<br>cybox:User_Account<br>cybox:File |  | process.location-service | 

The LOCATE action accepts the following modifiers:

**Table. Modifiers: LOCATE**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| None to Date |  |  |  | 

Below is a sample of OpenC2 commands to perform a LOCATE of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: LOCATE**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Geolocate a device | LOCATE | cybox:Device<hr>cybox:DeviceObjectType | process.location-service<hr>(optional) |  | 
| 2 | Get location of an IP address | LOCATE | cybox:Address<hr>cybox:AddressObjectType | process.location-service<hr>(optional) |  | 

