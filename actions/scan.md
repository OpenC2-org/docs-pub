### SCAN
The SCAN action is the systematic examination of some aspect of the entity or its environment in order to obtain information.

This action can be used to command the characterization of an environment (e.g., perform network, port, or vulnerability scanning) or to look for a specific occurrence of an object (e.g., file, IP, process). SCAN commands are distinct from the QUERY in that SCAN implies an analytic while a QUERY implies a routine retrieval of data.

**Table. Supported Targets and Actuators: SCAN**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:Device<br>cybox:Email_Message<br>cybox:Network_Connection<br>cybox:Disk<br>cybox:Disk_Partition<br>cybox:Domain_Name<br>cybox:File<br>cybox:Memory<br>cybox:Network_Packet<br>cybox:Network_Subnet<br>cybox:Process<br>cybox:Product<br>cybox:System<br>cybox:URI<br>cybox:User_Account<br>cybox:User_Session<br>cybox:Volume |  | network.sensor | 

The SCAN action accepts the following modifiers:

**Table. Modifiers: SCAN**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| method | enumeration: non-authenticated, authenticated | Optional. When there is more than one way to perform the action, the method can be specified, if necessary. | All | 
| search | cve, patch, vendor bulletin, signature | Required. The search criteria for performing the scan. | All | 

Below is a sample of OpenC2 commands to perform a SCAN of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: SCAN**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Scan a device for vulnerabilities | SCAN | cybox:Device<hr>cybox:DeviceObjectType | network.sensor<hr>(optional) | search = CVE | 
| 2 | Scan email messages for malware | SCAN | cybox:Email_Message<hr>cybox:EmailMessageObjectType | network.sensor<hr>(optional) | search = malware signature | 
| 3 | Scan network traffic for malicious activities | SCAN | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.sensor<hr>(optional) | search = network signature | 

