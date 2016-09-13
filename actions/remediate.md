### REMEDIATE
The REMEDIATE action tasks the recipient enclave to eliminate the vulnerability or attack point.
Remediate implies that addressing the issue is paramount.

Examples of actions resulting from a received REMEDIATE OpenC2 command could include contain/quarantine to a VLAN, set authorizations, redirect URL to quarantine portal, get new configuration, or update patches.

**Table. Supported Targets and Actuators: REMEDIATE**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:Email_Message<br>cybox:Hostname<br>cybox:Address<br>cybox:Device<br>cybox:File<br>cybox:Network_Connection<br>cybox:Process<br>cybox:Product<br>cybox:System<br>cybox:X509_Certificate |  |  | 

The REMEDIATE action accepts the following modifiers:

**Table. Modifiers: REMEDIATE**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| None to Date |  |  |  | 

Below is a sample of OpenC2 commands to perform a REMEDIATE of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: REMEDIATE**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Remediate the specified malicious email message | REMEDIATE | cybox:Email_Message<hr>cybox:EmailMessageObjectType | <hr> | [report-to] | 
| 2 | Remediate the specified infected hostname | REMEDIATE | cybox:Hostname<hr>cybox:HostnameObjectType | <hr> | [report-to] | 

