### DENY
The DENY action is used to prevent a certain event or action from completion, such as preventing a flow from reaching a destination (e.g., block) or preventing access.

DENY is a superset of current terms such as BLOCK (network perimeter devices) and DENY (user, access to system, access to files).

**Table. Supported Targets and Actuators: DENY**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:Network_Connection<br>cybox:URI<br>cybox:Product<br>cybox:Device<br>cybox:Process<br>cybox:User_Account |  | network.firewall<br>network.router<br>process<br>network.proxy<br>endpoint<br>process.aaa-server | 

The DENY action accepts the following modifiers:

**Table. Modifiers: DENY**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| method | enumeration: acl, blackhole, sinkhole, blacklist, whitelist | Optional. When there is more than one way to perform the action, the method can be specified, if necessary. | cybox:Network_Connection, cybox:Product | 
| where | enumeration: internal, perimeter | Optional. The general location within the enclave to perform the DENY action. | cybox:Network_Connection | 

Below is a sample of OpenC2 commands to perform a DENY of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: DENY**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Block traffic to/from specific IP address; suitable for coordinating across multiple enclaves and allowing enclaves to determine most appropriate response | DENY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> |  | 
| 2 | Block traffic to/from specific IP address at all network firewalls | DENY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.firewall<hr>(optional) |  | 
| 3 | Block traffic at the network routers | DENY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.router<hr>(optional) |  | 
| 4 | Block network traffic inside the enclave | DENY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> | where = internal | 
| 5 | Block network traffic at the perimeter | DENY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> | where = perimeter | 
| 6 | Block network traffic by ACL | DENY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.router<hr>(optional) | method = acl | 
| 7 | Block access to a bad external IP address by null routing at the network routers. | DENY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType<br>(external IP address) | network.router<hr>(optional) | method = blackhole | 

