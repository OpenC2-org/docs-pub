## Use Case: Reference Implementation
### Description
TBSL

**Table. Scenario Diagram: Reference Implementation**

![alt text](https://github.com/OpenC2-org/docs-members/blob/master/use-cases/reference-implementation.png "Use Case Diagram")


**Table. Scenario Steps: Reference Implementation**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 |  |  | <hr> | <hr> |  | 
| 2 | External Enclave determines that there is a need to coordinate with other networks for the mitigation against an evil domain. |  | <hr> | <hr> |  | 
| 3 | External Enclave sends the COA containing an action to mitigate against the evil domain to the Enclave. | MITIGATE | cybox:Domain_Name<hr>Source Socket Address:<br>  IP Address = "8.8.8.8",<br>  Port = [80, 443]) | <hr> | uuid = xxxx-0001 | 
| 4 | Sense-Making at the Enclave provides the COA containing an action to mitigate against the evil domain to Decision-Making. |  | <hr> | <hr> |  | 
| 5 | Decision-Making commands Acting to send an application level Acknowledgement for the receipt of the COA.  | NOTIFY | cybox:System<hr>cybox:SystemObjectType | <hr> | message = acknowledge | 
| 6 | Acting sends the Acknowledgement for the receipt of the COA to the External Enclave. <Dependency: UUID for command from External Enclave> | RESPONSE | <hr> | <hr> | type = acknowledge,<br>command = xxxx-0001 | 
| 7 | Decision-Making commands Acting to execute the mitigation. | DENY | cybox:Network_Connection<hr>Source Socket Address:<br>  IP Address = "8.8.8.8",<br>  Port = [80, 443]) | <hr> |  | 
| 8 | Acting contextualized the mitigation steps. |  | <hr> | <hr> |  | 
| 9 | Acting notifies an authorized user of the new action plan.  Acting awaits approval before proceeding. | NOTIFY | cybox:User_Account<hr>Username | endpoint.server<hr>(specifier) | message = "approval request" | 
| 10 | Upon approval, Acting commands a firewall to block packets. | DENY | cybox:Network_Connection<hr>Source Socket Address:<br>  IP Address = "8.8.8.8",<br>  Port = [80, 443]) | network.firewall<hr>(specifier) |  | 
|  | ALTERNATIVE ACTIONS |  | <hr> | <hr> |  | 
| 1 | [Alternative] Acting issues a command to block access to a bad external IP so that any access to the ip will be denied (Perimeter Blocking using ACLs on the perimeter firewalls) | DENY | cybox:Network_Connection<hr>Source Socket Address:<br>  IP Address = "8.8.8.8",<br>  Port = [80, 443]) | network.router<hr>(specifiy perimeter routers) | uuid = xxxx-0002,<br>method = "acl" | 
| 2 | Mitigation Manager commands the update of the ACL at each perimeter firewall (vendor specific) |  | <hr> | <hr> |  | 
| 3 | Actuator notifes the Mitigation Manager of the status of the execution of the command (vendor specific) |  | <hr> | <hr> |  | 
| 4 | Mitigation Manager notifies Acting of the status of the execution of the OpenC2 command (e.g., completed, failed) | RESPONSE | <hr> | <hr> | type = status,<br>value = complete,<br>command = xxxx-0002 | 

