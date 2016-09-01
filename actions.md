## Actions
This section defines the set of OpenC2 actions grouped by their general activity.  The following table summarizes the definition of the OpenC2 actions.

**Table. Summary of Action Definitions**

| <MERGE> | Actions that Gather and Convey Information | 
| :--- | :--- | 
| [SCAN](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/scan.md) | The SCAN action is the systematic examination of some aspect of the entity or its environment in order to obtain information. | 
| [LOCATE](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/locate.md) | The LOCATE action is used to find an object either physically, logically, functionally, or by organization. This action enables one to tell where in the system an event or trigger occurred. | 
| [QUERY](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/query.md) | The QUERY action initiates a single request for information. | 
| [REPORT](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/report.md) | The REPORT action tasks an entity to provide information to a designated recipient of the information. | 
| [GET](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/get.md) | The GET action tasks an entity to retrieve a specific object. | 
| [NOTIFY](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/notify.md) | The NOTIFY action is used to direct an entity to send information to another entity. | 
|  | **Actions that Control Permissions** | 
| [DENY](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/deny.md) | The DENY action is used to prevent a certain event or action from completion, such as preventing a flow from reaching a destination (e.g., block) or preventing access. | 
| [CONTAIN](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/contain.md) | The CONTAIN action stipulates the isolation of a file or process or entity such that it cannot modify or access assets or processes that support the business and/or operations of the enclave. | 
| [ALLOW](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/allow.md) | The ALLOW action permits the access to or execution of something.  | 
|  | **Actions that Control Activities/Devices** | 
| [START](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/start.md) | The START action initiates a process, application, system or some other activity. | 
| [STOP](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/stop.md) | The STOP action halts a system or ends an activity. | 
| [RESTART](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/restart.md) | The RESTART action conducts a STOP of a system or an activity followed by a START of a system or an activity. | 
| [PAUSE](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/pause.md) | The PAUSE action ceases a system or activity while maintaining state. | 
| [RESUME](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/resume.md) | The RESUME action starts a system or activity from a paused state. | 
| [CANCEL](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/cancel.md) | The CANCEL action invalidates a previously issued action. | 
| [SET](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/set.md) | The SET action changes a value, configuration, or state of a managed entity within an IT system. | 
| [UPDATE](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/update.md) | The UPDATE action instructs the component to retrieve and process a software update, reconfiguration, or some other update. | 
| [MOVE](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/move.md) | The MOVE action changes the location of a file, subnet, network, or, process. | 
| [REDIRECT](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/redirect.md) | The REDIRECT action changes the flow of traffic to a particular destination other than its original intended destination. | 
| [DELETE](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/delete.md) | The DELETE action removes data and files. | 
| [SNAPSHOT](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/snapshot.md) | The SNAPSHOT action records and stores the state of a target at an instant in time. | 
| [DETONATE](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/detonate.md) | The DETONATE action executes and observes the behavior of an object (e.g., file, hyperlink) in a manner that isolates the object from assets that support the business or operations of the enclave. | 
| [RESTORE](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/restore.md) | The RESTORE action deletes and/or replaces files, settings, or attributes such that the state of the system is identical to its state at some previous time. | 
| [SAVE](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/save.md) | The SAVE action commits data or system state to memory. | 
| [MODIFY](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/modify.md) | The MODIFY action augments, enhances, transforms, or changes some aspect of a system. | 
| [THROTTLE](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/throttle.md) | The THROTTLE action adjusts the throughput of a data flow. | 
| [DELAY](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/delay.md) | The DELAY action stops or holds up an activity or data transmittal. | 
| [SUBSTITUTE](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/substitute.md) | The SUBSTITUTE action replaces all or part of the data, content or payload in the least detectable manner. | 
| [COPY](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/copy.md) | The COPY action duplicates a file or data flow. | 
| [SYNC](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/sync.md) | The SYNC action synchronizes a sensor or actuator with other system components. | 
|  | **Sensor-Related Actions** | 
| [DISTILL](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/distill.md) | The DISTILL action tasks the sensor to send a summary or abstraction of the sensing information instead of the raw data feed. | 
| [AUGMENT](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/augment.md) | The AUGMENT action tasks the sensor to do a level of preprocessing or sense making prior to sending the sensor data. | 
|  | **Effects-Based Actions** | 
| [INVESTIGATE](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/investigate.md) | The INVESTIGATE action tasks the recipient enclave to aggregate and report information as it pertains to an anomaly. | 
| [MITIGATE](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/mitigate.md) | The MITIGATE action tasks the recipient enclave to circumvent the problem without necessarily eliminating the vulnerability or attack point.<br>Mitigate implies that the impacts to the enclave’s operations should be minimized while addressing the issue. | 
| [REMEDIATE](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/remediate.md) | The REMEDIATE action tasks the recipient enclave to eliminate the vulnerability or attack point.<br>Remediate implies that addressing the issue is paramount. | 
|  | **Response and Alert** | 
| [RESPONSE](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/response.md) | RESPONSE is used to provide any data requested as a result of an action. RESPONSE can be used to signal the acknowledgement of an action, provide the status of an action along with additional information related to the requested action, or signal the completion of the action. The recipient of the RESPONSE can be the original requester of the action or to another recipient(s) designated in the modifier of the action. | 
| [ALERT](https://github.com/OpenC2-org/docs-contributors/blob/master/actions/alert.md) | ALERT is used to signal the occurrence of an event. | 

