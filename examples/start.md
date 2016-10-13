### START
**Table. Example Actions: START**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Start Process, general | START | cybox:Process<hr>cybox:ProcessObjectType | <hr> |  | 
| 2 | Start Process | START | cybox:Process<hr>cybox:ProcessObjectType | endpoint<hr>(optional) |  | 
| 3 | Start Process with Delay | START | cybox:Process<hr>cybox:ProcessObjectType | endpoint<hr>(optional) | delay | 
| 4 | Spawn Process | START | cybox:Process<hr>cybox:ProcessObjectType | endpoint<hr>(optional) | method = spawn | 
| 5 | Execute Command | START | cybox:Process<hr>cybox:ProcessObjectType | endpoint<hr>(optional) |  | 
| 6 | Start an Application | START | cybox:Product<hr>cybox:ProductObjectType | endpoint<hr>(optional) |  | 
| 7 | Start a device | START | cybox:System<hr>cybox:SystemObjectType | network<hr>(optional) |  | 
| 8 | Start a virtual machine | START | cybox:System<hr>cybox:SystemObjectType | process.virtualization-service<hr>(optional) |  | 
| 9 | Activates the system partitions of a machine | START | cybox:Disk_Partition<hr>cybox:DiskPartitionObjectType | endpoint<hr>(optional) |  | 

