## SCAN

**Table. Example Actions: SCAN**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Scan a device for vulnerabilities | SCAN | cybox:Device<hr>cybox:DeviceObjectType | network.sensor<hr>(optional) | search = CVE | 
| 2 | Scan email messages for malware | SCAN | cybox:Email_Message<hr>cybox:EmailMessageObjectType | network.sensor<hr>(optional) | search = malware signature | 
| 3 | Scan network traffic for malicious activities | SCAN | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.sensor<hr>(optional) | search = network signature | 

