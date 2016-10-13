### DENY
**Table. Example Actions: DENY**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Block traffic to/from specific IP address; suitable for coordinating across multiple enclaves and allowing enclaves to determine most appropriate response | DENY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> |  | 
| 2 | Block traffic to/from specific IP address at all network firewalls | DENY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.firewall<hr>(optional) |  | 
| 3 | Block traffic at the network routers | DENY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.router<hr>(optional) |  | 
| 4 | Block network traffic inside the enclave | DENY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> | where = internal | 
| 5 | Block network traffic at the perimeter | DENY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> | where = perimeter | 
| 6 | Block network traffic by ACL | DENY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.router<hr>(optional) | method = acl | 
| 7 | Block access to a bad external IP address by null routing at the network routers. | DENY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType<br>(external IP address) | network.router<hr>(optional) | method = blackhole | 
| 8 | Block access to/from suspicious internal IP address by null routing at the network routers | DENY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType<br>(internal IP address) | network.router<hr>(optional) | method = blackhole | 
| 9 | Block network traffic at the perimeter routers | DENY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.router<hr>(specify perimeter routers) |  | 
| 10 | Block access to suspicious external IP address by redirecting external DNS queries to an internal DNS server | DENY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> | method = sinkhole | 
| 11 | Block traffic to/from specific IP address at all endpoints' firewalls | DENY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | process<hr>(specify endpoint and firewall application) |  | 
| 12 | Block malicious URL (blacklist domain); suitable for coordinating across multiple enclaves and allowing enclaves to determine most appropriate response | DENY | cybox:URI<hr>cybox:URIObjectType | <hr> |  | 
| 13 | Block malicious URL at proxy server | DENY | cybox:URI<hr>cybox:URIObjectType | network.proxy<hr>(optional) |  | 
| 14 | Block malicious URL at all network firewalls | DENY | cybox:URI<hr>cybox:URIObjectType | network.firewall<hr>(optional) |  | 
| 15 | Block malicious URL at all endpoint firewalls | DENY | cybox:URI<hr>cybox:URIObjectType | process<hr>(specify endpoint and firewall application) |  | 
| 16 | Block malicious URL at all endpoint browsers | DENY | cybox:URI<hr>cybox:URIObjectType | process<hr>(optional) |  | 
| 17 | Block system application; suitable for coordinating across multiple enclaves and allowing enclaves to determine most appropriate response | DENY | cybox:Product<hr>cybox:ProductObjectType | <hr> |  | 
| 18 | Block system application from executing at endpoint with certain characteristics or specific endpoint(s) | DENY | cybox:Product<hr>cybox:ProductObjectType | endpoint<hr>(specify based on endpoint characteristics) |  | 
| 19 | Block system application from executing by application white listing | DENY | cybox:Product<hr>cybox:ProductObjectType | endpoint<hr>(optional) | method = whitelist | 
| 20 | Deny Device Access (Infected Host) | DENY | cybox:Device<hr>cybox:DeviceObjectType | process.aaa-server<hr>(optional) |  | 
| 21 | Block Process | DENY | cybox:Process<hr>cybox:ProcessObjectType | endpoint<hr>(optional) |  | 
| 22 | Block Process by Domain | DENY | cybox:Process<hr>cybox:ProcessObjectType<br>(specify process by domain) | endpoint<hr>(optional) |  | 
| 23 | Deny user access to the system; suitable for coordinating across multiple enclaves | DENY | cybox:User_Account<hr>cybox:UserAccountObjectType | <hr> |  | 

