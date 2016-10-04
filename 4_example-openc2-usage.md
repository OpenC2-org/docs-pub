# [3. OpenC2 Language](3.0_openc2-language.md#3-openc2-language)

## [3.6 Modifier Vocabulary](3.6_modifier-vocabulary.md#36-modifier-vocabulary)

# 4. EXAMPLE OpenC2 USAGE

This section provides examples of OpenC2 commands corresponding to each OpenC2 action and its applicable targets, actuators, and modifiers. These examples are samples of OpenC2 commands, intended to show the usability and flexibility of the OpenC2 language. A fuller set of example usages can be found in Appendix A. 

## 4.1 Actions that Gather and Convey Information

These actions are used to gather information needed to further determine courses of action or assess the effectiveness of courses of action. These actions can be used to support data enrichment use cases and maintain situational awareness. These actions typically do not impact the state of the target and are normally not detectable by external observers. 

### [4.1.1 SCAN](actions/scan.md#scan)
### [4.1.2 LOCATE](actions/locate.md#locate)
### [4.1.3 QUERY](actions/query.md#query)
### [4.1.4 REPORT](actions/report.md#report)
### [4.1.5 GET](actions/get.md#get)
### [4.1.6 NOTIFY](actions/notify.md#notify)

## 4.2 Actions that Control Permissions

These actions are used to control permissions and accesses. The permissions and accesses can be for person or non-person entities.

### [4.2.1 DENY](actions/deny.md#deny)
### [4.2.2 CONTAIN](actions/contain.md#contain)
### [4.2.3 ALLOW](actions/allow.md#allow)

## 4.3 Actions that Control Activities/Devices

These actions are used to control the state or the activity of a system, a process, a connection, a host, or a device (e.g., endpoint, sensor, actuator). The actions are used to adjust configurations, set and update parameters, and modify attributes.

### [4.3.1 START](actions/start.md#start)
### [4.3.2 STOP](actions/stop.md#stop)
### [4.3.3 RESTART](actions/restart.md#restart)
### [4.3.4 PAUSE](actions/pause.md#pause)
### [4.3.5 RESUME](actions/resume.md#resume)
### [4.3.6 CANCEL](actions/cancel.md#cancel)
### [4.3.7 SET](actions/set.md#set)
### [4.3.8 UPDATE](actions/update.md#update)
### [4.3.9 MOVE](actions/move.md#move)
### [4.3.10 REDIRECT](actions/redirect.md#redirect)
### [4.3.11 DELETE](actions/delete.md#delete)
### [4.3.12 SNAPSHOT](actions/snapshot.md#snapshot)
### [4.3.13 DETONATE](actions/detonate.md#detonate)
### [4.3.14 RESTORE](actions/restore.md#restore)
### [4.3.15 SAVE](actions/save.md#save)
### [4.3.16 MODIFY](actions/modify.md#modify)
### [4.3.17 THROTTLE](actions/throttle.md#throttle)
### [4.3.18 DELAY](actions/delay.md#delay)
### [4.3.19 SUBSTITUTE](actions/substitute.md#substitute)
### [4.3.20 COPY](actions/copy.md#copy)
### [4.3.21 SYNC](actions/sync.md#sync)

## 4.4 Sensor-Related Actions

These actions are used to control the activities of a sensor in terms of how to collect and provide the sensor data.

### [4.4.1 DISTILL](actions/distill.md#distill)
### [4.4.2 AUGMENT](actions/autment.md#augment)

## 4.5 Effects-Based Actions

Effects-based actions are at a higher level of abstraction and focus on the desired impact rather than a command to execute specific task(s) within an enclave. The benefit of including effects-based actions is that it permits a higher level or peer enclave to coordinate actions, while still permitting a local enclave to optimize its workflow for its specific environment in order to achieve the desired result.

Implementation of an effects-based action requires that the recipient enclave has a decision making capability because an effects-based action permits multiple possible responses.

### [4.5.1 INVESTIGATE](actions/investigate.md#investigate)
### [4.5.2 MITIGATE](actions/mitigate.md#mitigate)
### [4.5.3 REMEDIATE](actions/remediate.md#remediate)

## 4.6 Response and Alert

RESPONSE is used to provide data requested as a result of an action. The RESPONSE message will contain the requested data and have a reference to the action that initiated the response. ALERT is used to signal the occurrence of an event or error. It is an unsolicited message that does not reference a previously issued action.

### [4.6.1 RESPONSE](actions/response.md#response)
### [4.6.2 ALERT](actions/alert.md#alert)

# [5. Example OpenC2 Use Case: Mitigate Evil Domain](5_example-openc2-use-case.md#5-example-openc2-use-case)
