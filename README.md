## Actions
This section defines the set of OpenC2 actions grouped by their general activity.  The following table summarizes the definition of the OpenC2 actions.  Subsequent sections provide further example usages for each action.

[Action Details](actions.md)

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

## Target Vocabulary
The TARGET is the object of the ACTION (or conversely, the ACTION is performed on the TARGET).  OpenC2 will utilize pre-existing data models to provide the namespace for the TARGETs.  Initially, OpenC2 will reference the applicable CybOX objects in the OpenC2 TARGET namespace. However, OpenC2 can be supported by custom or other data models.

[Target Details](targets.md)

## Actuator Vocabulary
An ACTUATOR is the entity that puts command and control into motion or action. The ACTUATOR executes the ACTION on the TARGET. To the extent possible, OpenC2 will leverage existing standardized data models for ACTUATORs (e.g., IETF Security Automation and Continuous Monitoring, Information Security Continuous Monitoring (ISCM)).

[Actuator Details](actuators.md)

## Modifier Vocabulary
Modifiers provide additional information about the action such as time, periodicity, duration, and location. Modifiers can denote the when, where, and how aspects of an action. The modifier can also be used to convey the need for additional status information about the execution of an action.  Modifiers can be used to indicate whether the actuator should explicitly acknowledge receipt of the command, respond upon completion of the execution of the command, or provide some other status information. The requested status/information will be carried in a RESPONSE. Refer to Section 4.6.

[Modifier Details](modifiers.md)