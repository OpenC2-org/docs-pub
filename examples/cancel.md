### CANCEL
**Table. Example Actions: CANCEL**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Cancel a previously issued command | CANCEL | openc2:Command<hr>openc2:CommandObjectType | <hr> | command-ref = command reference | 
| 2 | Cancel a previously issued command, directed to a specific actuator (endpoint) | CANCEL | openc2:Command<hr>openc2:CommandObjectType | endpoint<hr>(optional) | command-ref = command reference | 
| 3 | Cancel a previously issued command, directed to a specific actuator (network) | CANCEL | openc2:Command<hr>openc2:CommandObjectType | network<hr>(optional) | command-ref = command reference | 
| 4 | Cancel a previously issued command, directed to a specific actuator (process) | CANCEL | openc2:Command<hr>openc2:CommandObjectType | process<hr>(optional) | command-ref = command reference | 

