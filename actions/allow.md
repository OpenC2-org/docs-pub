### ALLOW
The ALLOW action permits the access to or execution of something. 

An ALLOW action is typically associated with something that was previously denied (e.g., block, quarantine).

**Table. Supported Targets and Actuators: ALLOW**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:Network_Connection<br>cybox:Device<br>cybox:File<br>cybox:URI<br>cybox:Product<br>cybox:Process<br>cybox:User_Account |  | network.firewall<br>network.router<br>process.aaa-server<br>endpoint<br>network.proxy | 

The ALLOW action accepts the following modifiers:

**Table. Modifiers: ALLOW**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| delay | duration | Optional. The time to wait before performing the action. | cybox:Device, cybox:User_Account | 
| permissions |  | Optional. Specific permissions to be granted to the user. | cybox:User_Account | 
| where | enumeration: internal, perimeter | Optional. The general location within the enclave to perform the DENY action. | cybox:Network_Connection | 

Below is a sample of OpenC2 commands to perform an ALLOW of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: ALLOW**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Unblock traffic to/from specific IP address; suitable for coordinating across multiple enclaves and allowing enclaves to determine most appropriate response | ALLOW | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> |  | 
| 2 | Unblock traffic to/from specific IP address at all network firewalls | ALLOW | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.firewall<hr>(optional) |  | 
| 3 | Unblock traffic at the network routers | ALLOW | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.router<hr>(optional) |  | 
| 4 | Unblock network traffic inside the enclave | ALLOW | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> | where = internal | 
| 5 | Delay Machine Authentication | ALLOW | cybox:Device<hr>cybox:DeviceObjectType | process.aaa-server<hr>(optional) | delay = <duration> | 
| 6 | Unquarantine a file | ALLOW | cybox:File<hr>cybox:FileObjectType | endpoint<hr>(optional) |  | 

