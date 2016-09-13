### INVESTIGATE
The INVESTIGATE action tasks the recipient enclave to aggregate and report information as it pertains to an anomaly.

Examples of actions resulting from a received INVESTIGATE OpenC2 command could include scan multiple machines, quarantine an endpoint, or detonate a file. These actions are determined by the enclave based on the results of sense-making/analytics and decision-making based on operational constraints and mission needs.

**Table. Supported Targets and Actuators: INVESTIGATE**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:Address<br>cybox:Device<br>cybox:Domain_Name<br>cybox:Email_Message<br>cybox:File<br>cybox:Hostname<br>cybox:Network_Connection<br>cybox:Port<br>cybox:Process<br>cybox:Product<br>cybox:System<br>cybox:X509_Certificate |  |  | 

The INVESTIGATE action accepts the following modifiers:

**Table. Modifiers: INVESTIGATE**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| report-to | cybox:AddressObjectType | Optional. If requested, this modifier identifies where to report the results of the investigation. | All | 

Below is a sample of OpenC2 commands to perform an INVESTIGATE of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: INVESTIGATE**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Investigate the specified IP address for malicious activities | INVESTIGATE | cybox:Address<hr>cybox:AddressObjectType | <hr> | [report-to] | 
| 2 | Investigate the specified device | INVESTIGATE | cybox:Device<hr>cybox:DeviceObjectType | <hr> | [report-to] | 
| 3 | Investigate the specified domain | INVESTIGATE | cybox:Domain_Name<hr>cybox:DomainNameObjectType | <hr> | [report-to] | 
| 4 | Investigate the specified email message | INVESTIGATE | cybox:Email_Message<hr>cybox:EmailMessageObjectType | <hr> | [report-to] | 
| 5 | Investigate the specified file(s) | INVESTIGATE | cybox:File<hr>cybox:FileObjectType | <hr> | [report-to] | 
| 6 | Investigate the specified hostname | INVESTIGATE | cybox:Hostname<hr>cybox:HostnameObjectType | <hr> | [report-to] | 

