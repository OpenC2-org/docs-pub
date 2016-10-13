### SCAN
**Table. Example Actions: SCAN**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Scan a device for vulnerabilities | SCAN | cybox:Device<hr>cybox:DeviceObjectType | network.sensor<hr>(optional) | search = CVE | 
| 2 | Scan email messages for malware | SCAN | cybox:Email_Message<hr>cybox:EmailMessageObjectType | network.sensor<hr>(optional) | search = malware signature | 
| 3 | Scan network traffic for malicious activities | SCAN | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.sensor<hr>(optional) | search = network signature | 
| 4 | Scan a disk for vulnerabilities | SCAN | cybox:Disk<hr>cybox:DiskObjectType | network.sensor<hr>(optional) | search | 
| 5 | Scan a disk partition for malware | SCAN | cybox:Disk_Partition<hr>cybox:DiskPartitionObjectType | network.sensor<hr>(optional) | search | 
| 6 | Scan a domain for malicious activities | SCAN | cybox:Domain_Name<hr>cybox:DomainNameObjectType | network.sensor<hr>(optional) | search | 
| 7 | Scan files for malware | SCAN | cybox:File<hr>cybox:FileObjectType | network.sensor<hr>(optional) | search | 
| 8 | Scan memory for malicious activities | SCAN | cybox:Memory<hr>cybox:MemoryObjectType | network.sensor<hr>(optional) | search | 
| 9 | Scan network packets for malicious activities | SCAN | cybox:Network_Packet<hr>cybox:NetworkPacketObjectType | network.sensor<hr>(optional) | search | 
| 10 | Scan a subnet for vulnerabilities or malicious activities | SCAN | cybox:Network_Subnet<hr>cybox:NetworkSubnetObjectType | network.sensor<hr>(optional) | search | 
| 11 | Scan a process for malicious activities | SCAN | cybox:Process<hr>cybox:ProcessObjectType | network.sensor<hr>(optional) | search | 
| 12 | Scan a software product for vulnerabilities or malicious activities | SCAN | cybox:Product<hr>cybox:ProductObjectType | network.sensor<hr>(optional) | search | 
| 13 | Scan a system for vulnerabilities or malicious activities | SCAN | cybox:System<hr>cybox:SystemObjectType | network.sensor<hr>(optional) | search | 
| 14 | Scan a URL for malicious activities | SCAN | cybox:URI<hr>cybox:URIObjectType | network.sensor<hr>(optional) | search | 
| 15 | Scan a user for malicious activities | SCAN | cybox:User_Account<hr>cybox:UserAccountObjectType | network.sensor<hr>(optional) | search | 
| 16 | Scan a user session for vulnerabilities or malicious activities | SCAN | cybox:User_Session<hr>cybox:UserSessionObjectType | network.sensor<hr>(optional) | search | 
| 17 | Scan a volume for malware | SCAN | cybox:Volume<hr>cybox:VolumeObjectType | network.sensor<hr>(optional) | search | 

