### RESPONSE
**Table. Example Actions: RESPONSE**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Acknowledge the receipt of an action | RESPONSE | <hr> | <hr> | type = acknowledge,<br>command-ref = command reference | 
| 2 | Signal completion of an action | RESPONSE | <hr> | <hr> | type = status,<br>value = complete,<br>command-ref = command reference | 
| 3 | Provide the status of an action | RESPONSE | <hr> | <hr> | type = status,<br>value = current,<br>command-ref = command reference | 

