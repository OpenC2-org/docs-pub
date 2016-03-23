## Target Vocabulary
The TARGET is the object of the ACTION (or conversely, the ACTION is performed on the TARGET).  OpenC2 will utilize pre-existing data models to provide the namespace for the TARGETs.  Initially, OpenC2 will reference the applicable CybOX objects in the OpenC2 TARGET namespace. However, OpenC2 can be supported by custom or other data models.  Refer to the following table for a summary of the OpenC2 TARGET Namespaces.

**Table. Target Namespace**

| Type | Description | Options | 
| :--- | :--- | :--- | 
| namespace | Used to uniquely identify a set of names so there is no ambiguity; defines the context in which names are defined. | Choice of:<br>  CybOX<br>  OpenC2<br>  Custom | 

Targets include objects such as network connections, URLs, hashes, IP addresses, files, processes, and domains. Refer to the following table for a summary of the supported OpenC2 TARGETs in CybOX Namespace.

**Table. Summary of Supported Targets**

| Target Type | Description | Target Specifier | 
| :--- | :--- | :--- | 
| cybox:Address<br> | The Address object is intended to specify a cyber address.<br> | cybox:AddressObjectType:<br>Address Value, VLAN Name, VLAN Num<br> | 
| cybox:Device<br> | The Device object is intended to characterize a specific Device.<br> | cybox:DeviceObjectType:<br>Description, Device Type, Manufacturer, Model, Serial Number, Firmware Version, System Details<br> | 
| cybox:Disk<br> | The Disk object is intended to characterize a disk drive.<br> | cybox:DiskObjectType:<br>Disk Name, Disk Size, Free Space, Partition List, Type<br> | 
| cybox:Disk_Partition<br> | The Disk_Partition object is intended to characterize a single partition of a disk drive.<br> | cybox:DiskPartitionObjectType:<br>Created, Device Name, Mount Point, Partition ID, Partition Length, Partition Offset, Space Left, Space Used, Total Space, Type<br> | 
| cybox:Domain_Name<br> | The Domain_Name object is intended to characterize network domain names.<br> | cybox:DomainNameObjectType:<br>Value<br> | 
| cybox:Email_Message<br> | The Email_Message object is intended to characterize an individual email message.<br> | cybox:EmailMessageObjectType:<br>Header, Email Server, Raw Body, Raw Header, Attachments, Links<br> | 
| cybox:File<br> | The File object is intended to characterize a generic file.<br> | cybox:FileObjectType:<br>File Name, File Path, Device Path, Full Path, File Extension, Size In Bytes, Magic Number, File Format, Hashes, Digital Signatures, Modified Time, Accessed Time, Created Time, File Attributes List, Permissions, User Owner, Packer List, Peak Entropy, Sym Links, Byte Runs, Extracted Features, Encryption Algorithm, Decryption Key, Compression Method, Compression Version, Compression Comment<br> | 
| cybox:Hostname<br> | The Hostname object is intended to specify a particular network hostname.<br> | cybox:HostNameObjectType:<br>Hostname Value, Naming System<br> | 
| cybox:Memory<br> | The Memory_Region object is intended to characterize generic memory objects.<br> | cybox:MemoryObjectType:<br>Hashes, Name, Memory Source, Region Size, Block Type, Region Start Address, Region End Address, Extracted Features<br> | 
| cybox:Network_Connection<br> | The Network_Connection object is intended to represent a single network connection.<br> | cybox:NetworkConnectionObjectType:<br>Layer3 Protocol, Layer4 Protocol, Source Socket Address (IP Address/Port), Destination Socket Address, (IP Address/Port)<br> | 
| cybox:Network_Flow<br> | The Network_Flow_Object object provides a summary of network traffic, expressed as flows of multiple packets instead of individual packets, without the packet payload data (i.e. the actual data that was uploaded/downloaded to and from the Dest IP to Source IP as included in packet monitoring tools, such as Wireshark).<br> | cybox:NetworkFlowObjectType:<br>Network Flow Label (Src Socket Address, Dest Socket Address, IP Protocol), Unidirectional Flow Record, Bidrectional Flow Record<br> | 
| cybox:Network_Packet<br> | The Network_Packet object provides the definition of a network packet based on the TCP/IP model/Internet protocol suite. In the TCP/IP stack, "packet" is generally defined as IP header plus payload, but we also include the LinkLayer from the OSI model, which defines the physical network interfaces and routing protocols. The application layer has not yet been defined.<br> | cybox:NetworkPacket:<br>Link Layer (Physical Interface, Logical Protocols), Internet Layer, Transport Layer<br> | 
| cybox:Network_Subnet<br> | The Network_Subnet object is intended to characterize a generic system network subnet.<br> | cybox:NetworkSubnetObjectType:<br>Name, Description, Number Of IP Addresses, Routes<br> | 
| cybox:Port<br> | The Port object is intended to characterize networking ports.<br> | cybox:PortObjectType:<br>Port Value, Layer4 Protocol<br> | 
| cybox:Process<br> | The Process object is intended to characterize system processes.<br> | cybox:ProcessObjectType:<br>PID, Name, Creation Time, Parent PID, Child PID List, Image Info, Argument List, Environment Variable List, Kernel Time, Post List, Network Connection List, Start Time, Status, Username, User Time, Extracted Features<br> | 
| cybox:Product<br> | The Product object is intended to characterize software or hardware products.<br> | cybox:ProductObjectType:<br>Edition, Language, Product, Update, Vendor, Version, Device Details<br> | 
| cybox:Socket_Address<br> | The Socket_Address element is intended to characterize a single network socket address.<br> | cybox:SocketAddressObjectType:<br>IP Address, Hostname, Port<br> | 
| cybox:System<br> | The System object is intended to characterize computer systems (as a combination of both software and hardware).<br> | cybox:SystemObjectType:<br>Available Physical Memory, BIOS Info, Date, Hostname, Local Time, Network Interface List, OS, Processor, Processor Architecture, System Time, Timezone DST, Timezone Standard, Total Physical Memory, Uptime, Username<br> | 
| cybox:URI<br> | The URI object is intended to characterize Uniform Resource Identifiers (URI’s).<br> | cybox:URIObjectType<br>Value<br> | 
| cybox:User_Account<br> | The User_Account object is intended to characterize generic user accounts.<br> | cybox:UserAccountObjectType:<br>Full Name, Group List, Home Directory, Last Login, Privilege List, Script Path, Username, User Password Age<br> | 
| cybox:User_Session<br> | The User_Session object is intended to characterize user sessions.<br> | cybox:UserSessionObjectType:<br>Effective Group, Effective Group ID, Effective User, Effective User ID, Login Time, Logout Time<br> | 
| cybox:Volume<br> | The Volume object is intended to characterize generic drive volumes.<br> | cybox:VolumeObjectType:<br>Name, Device Path, File System Type, Total Allocation Units, Sectors Per Allocation Unit, Bytes Per Sector, Actual Available Allocation Units, Creation Time, File System Flag List, Serial Number<br> | 
| cybox:Windows_Registry_Key<br> | Windows_Registry_Key object characterizes windows registry objects, including Keys and Key/Value pairs. [Link](http://msdn.microsoft.com/en-us/library/windows/desktop/ms724871(v=vs.85).asp)<br> | cybox:WindowsRegistryKeyObjectType:<br>Key, Hive, Number Values, Values, Modified Time, Creator Username, Handle List, Number Subkeys, Subkeys, Byte Runs<br> | 
| cybox:Windows_Service<br> | Windows_Service object is intended to characterize Windows services. [Link](http://msdn.microsoft.com/en-us/library/windows/desktop/ms685141(v=vs.85).aspx)<br> | cybox:WindowsServiceObjectType:<br>Description List, Display Name, Group Name, Service Name, Service DLL, Service DLL Certificate Issuer, Service DLL Certificate Subject, Service DLL Hashes, Service DLL Signature Description, Startup Command Line, Startup Type, Service Status, Service Type, Started As<br> | 
| cybox:X509_Certificate<br> | X509_Certificate object represents a public key certificate for use in a public key infrastructure.<br> | cybox:X509CertificateObjectType:<br>Certificate, Raw Certificate, Certificate Signature<br> | 
| openc2:Data<br> | The Data object is intended to characterize the result of information gathering and publishing activities.<br> | openc2:DataObjectType:<br>Value, Attributes, Search<br> | 

