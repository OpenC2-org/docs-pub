### COPY
The COPY action duplicates a file or data flow.

**Table. Supported Targets and Actuators: COPY**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:File<br>cybox:Network_Connection<br>cybox:Network_Flow<br>cybox:Disk_Partition<br>cybox:Memory<br>??? |  |  | 

The COPY action accepts the following modifiers:

**Table. Modifiers: COPY**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| copy-to |  | The location to copy to. | All | 
| where |  | Optional. The system to copy from. | cybox:Disk_Partition, cybox:Memory | 

Below is a sample of OpenC2 commands to perform a COPY of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: COPY**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Copy a file | COPY | cybox:File<hr>cybox:FileObjectType | <hr> | where,<br>copy-to | 
| 2 | Copy network traffic | COPY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> | copy-to | 

