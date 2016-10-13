### ALLOW
**Table. Example Actions: ALLOW**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Unblock traffic to/from specific IP address; suitable for coordinating across multiple enclaves and allowing enclaves to determine most appropriate response | ALLOW | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> |  | 
| 2 | Unblock traffic to/from specific IP address at all network firewalls | ALLOW | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.firewall<hr>(optional) |  | 
| 3 | Unblock traffic at the network routers | ALLOW | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.router<hr>(optional) |  | 
| 4 | Unblock network traffic inside the enclave | ALLOW | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> | where = internal | 
| 5 | Delay Machine Authentication | ALLOW | cybox:Device<hr>cybox:DeviceObjectType | process.aaa-server<hr>(optional) | delay = <duration> | 
| 6 | Unquarantine a file | ALLOW | cybox:File<hr>cybox:FileObjectType | endpoint<hr>(optional) |  | 
| 7 | Unblock network traffic at the perimeter | ALLOW | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> | where = perimeter | 
| 8 | Unblock network traffic at the perimeter routers | ALLOW | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.router<hr>(specify perimeter routers) |  | 
| 9 | Unblock traffic to/from specific IP address at all endpoints' firewalls | ALLOW | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | process<hr>(specify endpoint and firewall application) |  | 
| 10 | Unblock URL (blacklist domain); suitable for coordinating across multiple enclaves and allowing enclaves to determine most appropriate response | ALLOW | cybox:URI<hr>cybox:URIObjectType | <hr> |  | 
| 11 | Unblock URL at proxy server | ALLOW | cybox:URI<hr>cybox:URIObjectType | network.proxy<hr>(optional) |  | 
| 12 | Unblock URL at all network firewalls | ALLOW | cybox:URI<hr>cybox:URIObjectType | network.firewall<hr>(optional) |  | 
| 13 | Unblock URL at all endpoint firewalls | ALLOW | cybox:URI<hr>cybox:URIObjectType | process<hr>(specify endpoint and firewall application) |  | 
| 14 | Unblock URL at all endpoint browsers | ALLOW | cybox:URI<hr>cybox:URIObjectType | process<hr>(optional) |  | 
| 15 | Unblock system application; suitable for coordinating across multiple enclaves and allowing enclaves to determine most appropriate response | ALLOW | cybox:Product<hr>cybox:ProductObjectType | <hr> |  | 
| 16 | Unblock system application from executing at endpoint with certain characteristics or specific endpoint(s) | ALLOW | cybox:Product<hr>cybox:ProductObjectType | endpoint<hr>(specify based on endpoint characteristics) |  | 
| 17 | Authenticate Machine | ALLOW | cybox:Device<hr>cybox:DeviceObjectType | process.aaa-server<hr>(optional) |  | 
| 18 | Unblock Process | ALLOW | cybox:Process<hr>cybox:ProcessObjectType | endpoint<hr>(optional) |  | 
| 19 | Unblock Process by Domain | ALLOW | cybox:Process<hr>cybox:ProcessObjectType<br>(specify process by domain) | endpoint<hr>(optional) |  | 
| 20 | Authenticate user; suitable for coordinating across multiple enclaves | ALLOW | cybox:User_Account<hr>cybox:UserAccountObjectType | <hr> |  | 
| 21 | Delay user authentication; suitable for coordinating across multiple enclaves | ALLOW | cybox:User_Account<hr>cybox:UserAccountObjectType | <hr> | delay = <duration> | 
| 22 | Grant User Access to Specific System | ALLOW | cybox:User_Account<hr>cybox:UserAccountObjectType | process.aaa-server<hr>(optional) | permissions | 
| 23 | Unquarantine a file, general | ALLOW | cybox:File<hr>cybox:FileObjectType | <hr> |  | 
| 24 | Release a process from isolation, general | ALLOW | cybox:Process<hr>cybox:ProcessObjectType | <hr> |  | 
| 25 | Release a process from isolation | ALLOW | cybox:Process<hr>cybox:ProcessObjectType | endpoint<hr>(optional) |  | 
| 26 | Unquarantine a device, general | ALLOW | cybox:Device<hr>cybox:DeviceObjectType | <hr> |  | 
| 27 | Unquarantine a device | ALLOW | cybox:Device<hr>cybox:DeviceObjectType | network<hr>(optional) |  | 

