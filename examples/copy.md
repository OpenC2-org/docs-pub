### COPY
**Table. Example Actions: COPY**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Copy a file | COPY | cybox:File<hr>cybox:FileObjectType | <hr> | where,<br>copy-to | 
| 2 | Copy network traffic | COPY | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> | copy-to | 
| 3 | Copy netflow information related to particular ip address | COPY | cybox:Network_Flow<hr>cybox:NetworkFlowObjectType | <hr> | copy-to | 
| 4 | Copy the full contents of a disk partition | COPY | cybox:Disk_Partition<hr>cybox:DiskPartitionObjectType | <hr> | where,<br>copy-to | 
| 5 | Copy the full contents of a system's memory | COPY | cybox:Memory<hr>cybox:MemoryObjectType | <hr> | where,<br>copy-to | 

