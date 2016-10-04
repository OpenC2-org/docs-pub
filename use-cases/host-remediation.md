## Use Case: Host Remediation
### Description
TBSL

**Table. Scenario Diagram: Host Remediation**

![alt text](https://github.com/OpenC2-org/docs-members/blob/master/use-cases/host-remediation.png "Use Case Diagram")
![alt text](https://github.com/OpenC2-org/docs-members/blob/master/use-cases/host-remediation-2.png "Use Case Diagram")


**Table. Scenario Steps: Host Remediation**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 |  |  | <hr> | <hr> |  | 
| 2a | External Enclave sends the COA to the Enclave to scan for a new malicious process and remediate the endpoint, if found. | SCAN | cybox:Process<hr>id = <SCAN_SIGNATURE> | <hr> |  | 
| 2b |  | RESTORE | cybox:Device<hr> | <hr> | on_action = "scan found" | 
| 3 | The COA is forwarded to the Decision-Making. |  | <hr> | <hr> |  | 
| 4 | Decision-Making commands Acting to orchestrate the update signatures at sensors. | UPDATE | data.signature<hr>id = <SCAN_SIGNATURE> | network.sensor<hr> | scan_ref = <SCAN_REF> | 
| 5 | Acting sends OpenC2 commands to appropriate sensors to update their signatures. | UPDATE | data.signature<hr>id = <SCAN_SIGNATURE> | network.sensor<hr> | scan_ref = <SCAN_REF> | 
| 6 |  |  | <hr> | <hr> |  | 
| 7 |  |  | <hr> | <hr> |  | 
| 8 | Sensor detects a Host running malicious process. |  | <hr> | <hr> |  | 
| 9 | Sense-Making notifies Decision-Making of Host running malicious process. |  | cybox:Device<hr>id = <HOST_ID>, <br>scan_ref = <SCAN_REF> | <hr> |  | 
| 10a | Decision-Making commands Acting to block the infected Host, investigate the cause of the infection, and restore the Host to a good state. | DENY | cybox:Device<hr>id = <HOST_ID> | <hr> |  | 
| 10b |  | SCAN | cybox:Process<hr>target_process = <PROCESS_ID>,<br>endpoint = <HOST_ID> | <hr> |  | 
| 10c |  | RESTORE | cybox:Process<hr>target_process = <PROCESS_ID>,<br>endpoint = <HOST_ID> | <hr> |  | 
| 11 | Acting contextualizes the commands from Decision-Making. |  | <hr> | <hr> |  | 
| 12 | Acting quarantines the infected Host by commanding Directory Services to set the Host's security group. (No return requested.) | SET | cybox:System<hr>id = <HOST_ID>,<br>name = "security group", <br>value = "quarantine group" | process.directory-service<hr> |  | 
| 13 | Acting queries infected Host for the file associated with the malicious process. | QUERY | openc2:Data<hr>search = "get file associated with <PROCESS_ID>" | endpoint<hr> | results_callback = <ACTING_ID> | 
| 14 | The file is returned to Acting. |  | <hr> | <hr> |  | 
| 15 | Acting sends the file to the Sandbox for detonation analysis. (No return requested.) | DETONATE | cybox:File<hr>file = <FILE> | process.sandbox<hr> |  | 
| 15 | Note: Sandbox will notify Sense-Making of the detonation results.  (Not shown.) |  | <hr> | <hr> |  | 
| 16 | Acting commands a Mitigation Manager to reimage the infected Host. (See Host Remediation Actions Use Case for alternative OpenC2 actions.) | RESTORE | cybox:Device<hr>id = <HOST_ID> | process.remediation-service<hr> | method = "reimage", results_callback = <SENSE_MAKING_ID> | 
| 17 | The Mitigation Manager works with other Actuators to reimage the Host. |  | <hr> | <hr> |  | 
| 18 |  |  | <hr> | <hr> |  | 
| 19 | The Mitigation Manager notifies Sense-Making that infected Host has been restored. | RESPONSE | openc2:Data<hr>to = <RECIPIENT_LIST>, <br>message = "host restored" | <hr> |  | 
| 20 | Sense-Making notifies Decision-Making that infected Host has been restored. |  | <hr> | <hr> |  | 
| 21 | Decision-Making commands Acting to un-block the infected Host. | ALLOW | cybox:Device<hr>id = <HOST_ID> | <hr> |  | 
| 22 | Acting commands Directory Services to return the Host to the active group. (No return requested.) | SET | cybox:System<hr>id = <HOST_ID>, <br>name = "security group", <br>value = "active group" | process.directory-service<hr> |  | 

