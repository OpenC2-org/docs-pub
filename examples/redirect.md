### REDIRECT
**Table. Example Actions: REDIRECT**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Redirect traffic to a honeypot; suitable for coordinating across multiple enclaves and allowing enclaves to determine most appropriate response | REDIRECT | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> | where | 
| 2 | Redirect traffic to a honeypot at a specific router | REDIRECT | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.router<hr> | where | 
| 3 | Cancel traffic redirection; suitable for coordinating across multiple enclaves and allowing enclaves to determine most appropriate response | REDIRECT | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> | where = null | 
| 4 | Cancel traffic redirection at a specific router | REDIRECT | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.router<hr> | where = null | 
| 5 | In order to investigate a suspicious user/endpoint, an investigator would want to issue a 'redirect' command so that the endpoint's traffic is redirected to an intrusion detection system where alerts will be fired as signatures are matched | REDIRECT | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> |  | 
| 6 | In order to enable self-remediation of a user's endpoint, the investigator would want to redirect all URLs to a quarantine portal so that remediation services can be accessed (URL redirection for self-service remediation) | REDIRECT | cybox:URI<hr>cybox:URIObjectType | network.router<hr> | where | 

