## Actuator Vocabulary
An ACTUATOR is the entity that puts command and control into motion or action. The ACTUATOR executes the ACTION on the TARGET. To the extent possible, OpenC2 will leverage existing standardized data models for ACTUATORs (e.g., IETF Security Automation and Continuous Monitoring, Information Security Continuous Monitoring (ISCM)).  Refer to the following table for a summary of the OpenC2 ACTUATOR Namespaces.

**Table. Actuator Namespace**

| Type | Description | Options | 
| :--- | :--- | :--- | 
| namespace | Used to uniquely identify a set of names so there is no ambiguity; defines the context in which names are defined. | Choice of:<br>  TBD: e.g., ISCM, SACM<br>  OpenC2<br>  Custom | 
ACTUATORs fall into classes (e.g., endpoint device, network, services/processes, and human). Refer to the following table for a summary of supported OpenC2 ACTUATORs.

**Table. Summary of Supported Actuators**

| Actuator Type | Description | Actuator Specifier | 
| :--- | :--- | :--- | 
| endpoint | Endpoint Device |  | 
| endpoint.workstation |  |  | 
| endpoint.server |  |  | 
| endpoint.laptop |  |  | 
| endpoint.smart-phone |  |  | 
| endpoint.tablet |  |  | 
| endpoint.printer |  |  | 
| endpoint.smart-meter |  |  | 
| endpoint.pos-terminal |  |  | 
| endpoint.digital-telephone-handset |  |  | 
| endpoint.sensor |  |  | 
| network | Network Platform |  | 
| network.firewall |  |  | 
| network.router |  |  | 
| network.ids |  |  | 
| network.hub |  |  | 
| network.bridge |  |  | 
| network.switch |  |  | 
| network.modem |  |  | 
| network.wap | Wireless Access Point |  | 
| network.gateway |  |  | 
| network.proxy |  |  | 
| network.nic | Network Interface Card |  | 
| network.vpn | VPN Concentrator/Appliance |  | 
| network.guard |  |  | 
| network.sensor |  |  | 
| network.hips |  |  | 
| network.ips |  |  | 
| network.security_manager |  |  | 
| network.sense_making |  |  | 
| process | Services/Processes |  | 
| process.vulnerability-scanner |  |  | 
| process.network-scanner |  |  | 
| process.connection-scanner |  |  | 
| process.anti-virus-scanner |  |  | 
| process.file-scanner |  |  | 
| process.aaa-server |  |  | 
| process.virtualization-service |  |  | 
| process.sandbox |  |  | 
| process.dns-server |  |  | 
| process.email-service |  |  | 
| process.directory-service |  |  | 
| process.remediation-service |  |  | 
| process.reputation-service |  |  | 
| process.virtualization-service |  |  | 
| process.location-service |  |  | 
