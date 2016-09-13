### MITIGATE
The MITIGATE action tasks the recipient enclave to circumvent the problem without necessarily eliminating the vulnerability or attack point.
Mitigate implies that the impacts to the enclave’s operations should be minimized while addressing the issue.

Examples of actions resulting from a received MITIGATE OpenC2 command could include deny a URL or process, scan, redirect traffic to honeypot, or move.

**Table. Supported Targets and Actuators: MITIGATE**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:Address<br>cybox:Device<br>cybox:Email_Message<br>cybox:File<br>cybox:Hostname<br>cybox:Network_Connection<br>cybox:Process<br>cybox:Product<br>cybox:System<br>cybox:X509_Certificate |  |  | 

The MITIGATE action accepts the following modifiers:

**Table. Modifiers: MITIGATE**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| None to Date |  |  |  | 

Below is a sample of OpenC2 commands to perform a MITIGATE of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: MITIGATE**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Mitigate the specified malicious IP address | MITIGATE | cybox:Address<hr>cybox:AddressObjectType | <hr> | [report-to] | 
| 2 | Mitigate the specified infected device | MITIGATE | cybox:Device<hr>cybox:DeviceObjectType | <hr> | [report-to] | 
| 3 | Mitigate the specified malicious email message | MITIGATE | cybox:Email_Message<hr>cybox:EmailMessageObjectType | <hr> | [report-to] | 

