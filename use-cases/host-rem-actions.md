## Use Case: Host Remediation Actions
### Description
TBSL

**Table. Scenario Diagram: Host Remediation Actions**

![alt text](https://github.com/OpenC2-org/docs-members/blob/master/use-cases/host-rem-actions.png "Use Case Diagram")
![alt text](https://github.com/OpenC2-org/docs-members/blob/master/use-cases/host-rem-actions-2.png "Use Case Diagram")


**Table. Scenario Steps: Host Remediation Actions**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | PATTERN A:<br>Acting commands Mitigation Manager. |  | <hr> | <hr> |  | 
| 2 | Acting sends an OpenC2 command to the Mitigation Manager to perform an action to support host remediation. |  | <hr> | <hr> |  | 
| 3 | The Mitigation Manager commands an Actuator to perform an action. |  | <hr> | <hr> |  | 
| 4 | The Actuator performs the requested action. |  | <hr> | <hr> |  | 
| 5 | PATTERN B:<br>Acting commands Actuator, directly. |  | <hr> | <hr> |  | 
| 6 | Acting commands an Actuator to perform an action to support host remediation. |  | <hr> | <hr> |  | 
| 7 | The Actuator will perform the requested action. |  | <hr> | <hr> |  | 
| 8 | The following are some of the commands that support host remediation: |  | <hr> | <hr> |  | 
| 9 | Set registry key value | SET | cybox:Windows_Registry_Key<hr>id = <REGISTRY_ID>,<br>key = <REGISTRY_KEY>,<br>value = <VALUE> | <hr> |  | 
| 10 | Set file permissions | SET | cybox:File<hr>id = <FILE_ID>,<br>key = "permission",<br>value = <VALUE> | process.directory-service<hr> |  | 
| 11 | Set user rights | SET | cybox:User_Account<hr>id = <USER_ID>,<br>key = "permission",<br>value = <VALUE> | process.directory-service<hr> |  | 
| 12 | Set password policy | SET | cybox:System<hr>id = <POLICY_ID>,<br>key = "password",<br>value = <VALUE> | <hr> |  | 
| 13 | Set auditing policy | SET | cybox:System<hr>id = <POLICY_ID>,<br>key = "audit",<br>value = <VALUE> | <hr> |  | 
| 14 | Start services | START | cybox:Process<hr>id = <PROCESS_ID> | <hr> |  | 
| 15 | Stop services | STOP | cybox:Process<hr>id = <PROCESS_ID> | <hr> |  | 
| 16 | Set registry permissions | SET | cybox:Windows_Registry_Key<hr>id = <REGISTRY_ID>,<br>key = "permission",<br>value = <VALUE> | <hr> |  | 
| 17 | Set service permissions | SET | cybox:Process<hr>id = <PROCESS_ID>,<br>key = "permission",<br>value = <VALUE> | <hr> |  | 
| 18 | Set group policy (computer, user) | SET | cybox:System<hr>id = <POLICY_ID>,<br>key = "group",<br>value = <VALUE> | <hr> |  | 
| 19 | Set user settings (remediate per user instead of per computer) | SET | cybox:User_Account<hr>id = <USER_ID>,<br>key = <SETTING>,<br>value = <VALUE> | <hr> |  | 
| 20 | Start Powershell | START | cybox:Process<hr>id = <PROCESS_ID> | <hr> |  | 
| 21 | Execute scripts | START | cybox:Process<hr>id = <PROCESS_ID> | <hr> |  | 
| 22 | Install software | UPDATE | cybox:Product<hr>id = <SOFTWARE_ID>,<br>location = <HOST_ID>,<br>source = <SOFTWARE_SOURCE> | <hr> |  | 
| 23 | Uninstall software | DELETE | cybox:Product<hr>id = <SOFTWARE_ID>,<br>location = <HOST_ID> | <hr> |  | 
| 24 | Install patch | UPDATE | cybox:Product<hr>id = <SOFTWARE_ID>,<br>location = <HOST_ID>,<br>source = <PATCH_SOURCE> | <hr> |  | 
| 25 | Update signature file (anti-virus) | UPDATE | data.signature<hr>id = <SIGNATURE_ID>,<br>location = <HOST_ID>,<br>source = <SIGNATURE_SOURCE> | <hr> |  | 
| 26 | Change a specific value in a config file | SET | data.configuration<hr>id = <CONFIGURATION_ID>,<br>key = <CONFIGURATION_KEY>,<br>value = <VALUE> | <hr> |  | 
| 27 | Change firewall rule | SET | data.configuration<hr>id = <FIREWALL_ID>,<br>key = <RULE_ID>,<br>value = <VALUE> | <hr> |  | 
| 28 | Change HIPS rule | SET | data.configuration<hr>id = <HIPS_ID>,<br>key = <RULE_ID>,<br>value = <VALUE> | network.hips<hr> |  | 
| 29 | Change network device rule | SET | data.configuration<hr>id = <DEVICE_ID>,<br>key = <RULE_ID>,<br>value = <VALUE> | <hr> |  | 
| 30 | Instruct an admin a make a manual fix | NOTIFY | cybox:User_Account<hr>id = "admin request",<br>message = <FIX_INSTRUCTIONS> | process.email-service<hr> |  | 

