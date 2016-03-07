## Actions
This section defines the set of OpenC2 actions grouped by their general activity.  The following table summarizes the definition of the OpenC2 actions.  Subsequent sections provide further example usages for each action.
### Actions that Gather and Convey Information
These actions are used to gather information needed to further determine courses of action or assess the effectiveness of courses of action.  These actions can be used to support data enrichment use cases and maintain situational awareness.  These actions typically do not impact the state of the target and are normally not detectable by external observers.
### Actions that Control Permissions
These actions are used to control permissions and accesses. The permissions and accesses can be for person or non-person entities.
### Actions that Control Activities/Devices
These actions are used to control the state or the activity of a system, a process, a connection, a host, or a device (e.g., endpoint, sensor, actuator). The actions are used to adjust configurations, set and update parameters, and modify attributes.
### Sensor-Related Actions
These actions are used to control the activities of a sensor in terms of how to collect and provide the sensor data.
### Effects-Based Actions
Effects-based actions are at a higher level of abstraction and focus on the desired impact rather than a command to execute specific task(s) within an enclave.  The benefit of including effects-based actions is that it permits a higher level or peer enclave to coordinate actions, while still permitting a local enclave to optimize its workflow for its specific environment in order to achieve the desired result. 
Implementation of an effects-based action requires that the recipient enclave has a decision making capability because an effects-based action permits multiple possible responses.
### Response and Alert
Response is used to provide data requested as a result of an action.  Alert is used to signal the occurrence of an event or error.

**Table. Summary of Action Definitions**

| <MERGE> | Actions that Gather and Convey Information | 
| :--- | :--- | 
| [SCAN](actions/scan.md) | The SCAN action is the systematic examination of some aspect of the entity or its environment in order to obtain information. | 
| [LOCATE](actions/locate.md) | The LOCATE action is used to find an object either physically, logically, functionally, or by organization.  This action enables one to tell where in the system an event or trigger occurred. | 
| [QUERY](actions/query.md) | The QUERY action initiates a single request for information. | 
| [REPORT](actions/report.md) | The REPORT action tasks an entity to provide information to a designated recipient of the information. | 
| [GET](actions/get.md) | The GET action tasks an entity to retrieve a specific object. | 
| [NOTIFY](actions/notify.md) | The NOTIFY action is used to direct an entity to send information to another entity. | 
|  | **Actions that Control Permissions** | 
| [DENY](actions/deny.md) | The DENY action is used to prevent a certain event or action from completion, such as preventing a flow from reaching a destination (e.g., block) or preventing access. | 
| [CONTAIN](actions/contain.md) | The CONTAIN action stipulates the isolation of a file or process or entity such that it cannot modify or access assets or processes that support the business and/or operations of the enclave.   | 
| [ALLOW](actions/allow.md) | The ALLOW action permits the access to or execution of something.  | 
|  | **Actions that Control Activities/Devices** | 
| [START](actions/start.md) | The START action initiates a process, application, system or some other activity.   | 
| [STOP](actions/stop.md) | The STOP action halts a system or ends an activity. | 
| [RESTART](actions/restart.md) | The RESTART action conducts a STOP of a system or an activity followed by a START of a system or an activity. | 
| [PAUSE](actions/pause.md) | The PAUSE action ceases a system or activity while maintaining state. | 
| [RESUME](actions/resume.md) | The RESUME action starts a system or activity from a paused state. | 
| [SET](actions/set.md) | The SET action changes a value, configuration, or state of a managed entity within an IT system. | 
| [UPDATE](actions/update.md) | The UPDATE action instructs the component to retrieve and process a software update, reconfiguration, or some other update. | 
| [MOVE](actions/move.md) | The MOVE action changes the location of a file, subnet, network, or, process. | 
| [REDIRECT](actions/redirect.md) | The REDIRECT action changes the flow of traffic to a particular destination other than its original intended destination. | 
| [DELETE](actions/delete.md) | The DELETE action removes data and files. | 
| [SNAPSHOT](actions/snapshot.md) | The SNAPSHOT action records and stores the state of a target at an instant in time. | 
| [DETONATE](actions/detonate.md) | The DETONATE action executes and observes the behavior of an object (e.g., file, hyperlink) in a manner that isolates the object from assets that support the business or operations of the enclave. | 
| [RESTORE](actions/restore.md) | The RESTORE action deletes and/or replaces files, settings, or attributes such that the state of the system is identical to its state at some previous time. | 
| [SAVE](actions/save.md) | The SAVE action commits data or system state to memory. | 
| [MODIFY](actions/modify.md) | The MODIFY action augments, enhances, transforms, or changes some aspect of a system. | 
| [THROTTLE](actions/throttle.md) | The THROTTLE action adjusts the throughput of entire data flow to a different  rate.  | 
| [DELAY](actions/delay.md) | The DELAY action stops or holds up an activity or data transmittal. | 
| [SUBSTITUTE](actions/substitute.md) | The SUBSTITUTE action replaces all or part of the data, content or payload in the least detectable manner. | 
| [COPY](actions/copy.md) | The COPY action duplicates a file or data flow. | 
| [SYNC](actions/sync.md) | The SYNC action synchronizes a sensor or actuator with other system components. | 
|  | **Sensor-Related Actions** | 
| [DISTILL](actions/distill.md) | The DISTILL action tasks the sensor to send a summary or abstraction of the sensing information instead of the raw data feed. | 
| [AUGMENT](actions/augment.md) | The AUGMENT action tasks the sensor to do a level of preprocessing or sense making prior to sending the sensor data. | 
|  | **Effects-Based Actions** | 
| [INVESTIGATE](actions/investigate.md) | The INVESTIGATE action tasks the recipient enclave to aggregate and report information as it pertains to an anomaly. | 
| [MITIGATE](actions/mitigate.md) | The MITIGATE action tasks the recipient enclave to circumvent the problem without necessarily eliminating the vulnerability or attack point.  <br>Mitigate implies that the impacts to the enclave’s operations should be minimized while addressing the issue. | 
| [REMEDIATE](actions/remediate.md) | The REMEDIATE action tasks the recipient enclave to eliminate the vulnerability or attack point.  <br>Remediate implies that addressing the issue is paramount. | 
|  | **Response and Alert** | 
| [RESPONSE](actions/response.md) | RESPONSE is used to provide any data requested as a result of an action. RESPONSE can be used to signal the acknowledgement of an action, provide the status of an action along with additional information related to the requested action, or signal the completion of the action. The recipient of the RESPONSE can be the original requester of the action or to another recipient(s) designated in the modifier of the action. | 
| [ALERT](actions/alert.md) | ALERT is used to signal the occurrence of an event or error. | 

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
| cybox:Network_Packet<br> | The Network_Packet object provides the definition of a network packet based on the TCP/IP model/Internet protocol suite. In the TCP/IP stack, "packet" is generally defined as IP header plus payload, but we also include the LinkLayer from the OSI model, which defines the physical network interfaces and routing protocols. The application layer has not yet been defined.<br> | cybox:NetworkPacket:<br>Link Layer, Internet Layer, Transport Layer<br> | 
| cybox:Network_Subnet<br> | The Network_Subnet object is intended to characterize a generic system network subnet.<br> | cybox:NetworkSubnetObjectType:<br>Name, Description, Number Of IP Addresses, Routes<br> | 
| cybox:Port<br> | The Port object is intended to characterize networking ports.<br> | cybox:PortObjectType:<br>Port Value, Layer4 Protocol<br> | 
| cybox:Process<br> | The Process object is intended to characterize system processes.<br> | cybox:ProcessObjectType:<br>PID, Name, Creation Time, Parent PID, Child PID List, Image Info, Argument List, Environment Variable List, Kernel Time, Post List, Network Connection List, Start Time, Status, Username, User Time, Extracted Features<br> | 
| cybox:Product<br> | The Product object is intended to characterize software or hardware products.<br> | cybox:ProductObjectType:<br>Edition, Language, Product, Update, Vendor, Version, Device Details<br> | 
| cybox:System<br> | The System object is intended to characterize computer systems (as a combination of both software and hardware).<br> | cybox:SystemObjectType:<br>Available Physical Memory, BIOS Info, Date, Hostname, Local Time, Network Interface List, OS, Processor, Processor Architecture, System Time, Timezone DST, Timezone Standard, Total Physical Memory, Uptime, Username<br> | 
| cybox:URI<br> | The URI object is intended to characterize Uniform Resource Identifiers (URI’s).<br> | cybox:URIObjectType<br>Value<br> | 
| cybox:User_Account<br> | The User_Account object is intended to characterize generic user accounts.<br> | cybox:UserAccountObjectType:<br>Full Name, Group List, Home Directory, Last Login, Privilege List, Script Path, Username, User Password Age<br> | 
| cybox:User_Session<br> | The User_Session object is intended to characterize user sessions.<br> | cybox:UserSessionObjectType:<br>Effective Group, Effective Group ID, Effective User, Effective User ID, Login Time, Logout Time<br> | 
| cybox:Volume<br> | The Volume object is intended to characterize generic drive volumes.<br> | cybox:VolumeObjectType:<br>Name, Device Path, File System Type, Total Allocation Units, Sectors Per Allocation Unit, Bytes Per Sector, Actual Available Allocation Units, Creation Time, File System Flag List, Serial Number<br> | 
| cybox:Windows_Registry_Key<br> | Windows_Registry_Key object characterizes windows registry objects, including Keys and Key/Value pairs. [Link](http://msdn.microsoft.com/en-us/library/windows/desktop/ms724871(v=vs.85).asp)<br> | cybox:WindowsRegistryKeyObjectType:<br>Key, Hive, Number Values, Values, Modified Time, Creator Username, Handle List, Number Subkeys, Subkeys, Byte Runs<br> | 
| cybox:Windows_Service<br> | Windows_Service object is intended to characterize Windows services. [Link](http://msdn.microsoft.com/en-us/library/windows/desktop/ms685141(v=vs.85).aspx)<br> | cybox:WindowsServiceObjectType:<br>Description List, Display Name, Group Name, Service Name, Service DLL, Service DLL Certificate Issuer, Service DLL Certificate Subject, Service DLL Hashes, Service DLL Signature Description, Startup Command Line, Startup Type, Service Status, Service Type, Started As<br> | 
| cybox:X509_Certificate<br> | X509_Certificate object represents a public key certificate for use in a public key infrastructure.<br> | cybox:X509CertificateObjectType:<br>Certificate, Raw Certificate, Certificate Signature<br> | 
| openc2:Data<br> | The Data object is intended to characterize the result of information gathering and publishing activities.<br> | openc2:DataObjectType:<br>Value, Attributes, Search<br> | 

## Actuator Vocabulary
An ACTUATOR is the entity that puts command and control into motion or action. The ACTUATOR executes the ACTION on the TARGET. To the extent possible, OpenC2 will leverage existing standardized data models for ACTUATORs (e.g., IETF Security Automation and Continuous Monitoring, Information Security Continuous Monitoring (ISCM)).  Refer to the following table for a summary of the OpenC2 ACTUATOR Namespaces.

**Table. Actuator Namespace**

| Type | Description | Options | 
| :--- | :--- | :--- | 
| namespace | Used to uniquely identify a set of names so there is no ambiguity; defines the context in which names are defined. | Choice of:<br>  TBD: e.g., ISCM, SACM<br>  OpenC2<br>  Custom | 
ACTUATORs fall into classes (e.g., endpoint device, network, services/processes, and human). Refer to the following table for a summary of supported OpenC2 ACTUATORs.

**Table. Summary of Supported Actuators**

| Actuator Type | Description | Actuator Specifier | 
| :--- | :--- | :--- | 
| endpoint | Endpoint Device |  | 
| endpoint.workstation |  |  | 
| endpoint.server |  |  | 
| endpoint.laptop |  |  | 
| endpoint.smart-phone |  |  | 
| endpoint.tablet |  |  | 
| endpoint.printer |  |  | 
| endpoint.smart-meter |  |  | 
| endpoint.pos-terminal |  |  | 
| endpoint.digital-telephone-handset |  |  | 
| endpoint.sensor |  |  | 
| network | Network Platform |  | 
| network.firewall |  |  | 
| network.router |  |  | 
| network.ids |  |  | 
| network.hub |  |  | 
| network.bridge |  |  | 
| network.switch |  |  | 
| network.modem |  |  | 
| network.wap | Wireless Access Point |  | 
| network.gateway |  |  | 
| network.proxy |  |  | 
| network.nic | Network Interface Card |  | 
| network.vpn | VPN Concentrator/Appliance |  | 
| network.guard |  |  | 
| network.sensor |  |  | 
| network.hips |  |  | 
| network.ips |  |  | 
| network.security_manager |  |  | 
| network.sense_making |  |  | 
| process | Services/Processes |  | 
| process.vulnerability-scanner |  |  | 
| process.network-scanner |  |  | 
| process.connection-scanner |  |  | 
| process.anti-virus-scanner |  |  | 
| process.file-scanner |  |  | 
| process.aaa-server |  |  | 
| process.virtualization-service |  |  | 
| process.sandbox |  |  | 
| process.dns-server |  |  | 
| process.email-service |  |  | 
| process.directory-service |  |  | 
| process.remediation-service |  |  | 
| process.reputation-service |  |  | 
| process.virtualization-service |  |  | 
| process.location-service |  |  | 

## Modifier Vocabulary
Modifiers provide additional information about the action such as time, periodicity, duration, and location. Modifiers can denote the when, where, and how aspects of an action. The modifier can also be used to convey the need for additional status information about the execution of an action.  Modifiers can be used to indicate whether the actuator should explicitly acknowledge receipt of the command, respond upon completion of the execution of the command, or provide some other status information. The requested status/information will be carried in a RESPONSE. Refer to Section 4.6.
The following table lists the set of modifiers that is broadly applicable across the different types of actions.

**Table. Summary of Universal Modifiers**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| delay | time | Optional.  The time to wait before performing the action. | All | 
| duration | time | Optional.  The time to wait until returning to the previous state. | All | 
| frequency |  | Optional.  The frequency at which to perform the action. | All | 
| response | ack, status | Optional.  Indicate the type of response required for the action. | All | 
| time | time | Optional.  The specific time to initiate the action. | All | 

Modifiers are similar to specifiers in that they can provide additional context specific details for an action, and are intended to provide additional details for action/target pairs. Action-specific modifiers are identified in the sections detailing out each action.
