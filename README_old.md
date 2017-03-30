## OpenC2 Language Description Document

## Revision History

Revision | Date | Description
---------|------|------------
1.0 - RC | 08/22/2016 | Version 1.0 -- Release Candidate

## TABLE OF CONTENTS

# [1. Introduction](1_introduction.md#1-introduction)

## [1.1 Purpose](1_introduction.md#11-purpose)
## [1.2 Scope](1_introduction.md#12-scope)
## [1.3 Intended Audience](1_introduction.md#13-intended-audience)
## [1.4 Document Overview](1_introduction.md#14-document-overview)

# [2. Background](2_background.md#2-background)

## [2.1 Design Principles](2_background.md#21-design-principles)
## [2.2 OpenC2 and Deployment Environments](2_background.md#22-openc2-and-deployment-environments)

# [3. OpenC2 Language](3.0_openc2-language.md#3-openc2-language)

## [3.1 Overview](3.0_openc2-language.md#31-overview)
## [3.2 Abstract Syntax](3.0_openc2-language.md#32-abstract-syntax)

### [3.2.1 Action](3.0_openc2-language.md#321-action)
### [3.2.2 Target](3.0_openc2-language.md#322-target)
### [3.2.3 Actuator](3.0_openc2-language.md#323-actuator)
### [3.2.4 Specifiers](3.0_openc2-language.md#324-specifiers)
### [3.2.5 Modifiers](3.0_openc2-language.md#325-modifiers)

## [3.3 Actions](3.3_actions.md#33-actions)

### [3.3.1 Actions that Gather and Convey Information](3.3_actions.md#331-actions-that-gather-and-convey-information)
### [3.3.2 Actions that Control Permissions](3.3_actions.md#332-actions-that-control-permissions)
### [3.3.3 Actions that Control Activities/Devices](3.3_actions.md#333-actions-that-control-activitiesdevices)
### [3.3.4 Sensor-Related Actions](3.3_actions.md#334-sensor-related-actions)
### [3.3.5 Effects-Based Actions](3.3_actions.md#335-effects-based-actions)
### [3.3.6 Response and Alert](3.3_actions.md#336-response-and-alert)

## [3.4 Target Vocabulary](3.4_target-vocabulary.md#34-target-vocabulary)
## [3.5 Actuator Vocabulary](3.5_actuator-vocabulary.md#35-actuator-vocabulary)
## [3.6 Modifier Vocabulary](3.6_modifier-vocabulary.md#36-modifier-vocabulary)

# [4. Example OpenC2 Usage](4_example-openc2-usage.md#4-example-openc2-usage)

## [4.1 Actions that Gather and Convey Information](4_example-openc2-usage.md#41-actions-that-gather-and-convey-information)

### [4.1.1 SCAN](actions/scan.md#scan)
### [4.1.2 LOCATE](actions/locate.md#locate)
### [4.1.3 QUERY](actions/query.md#query)
### [4.1.4 REPORT](actions/report.md#report)
### [4.1.5 GET](actions/get.md#get)
### [4.1.6 NOTIFY](actions/notify.md#notify)

## [4.2 Actions that Control Permissions](4_example-openc2-usage.md#42-actions-that-control-permissions)

### [4.2.1 DENY](actions/deny.md#deny)
### [4.2.2 CONTAIN](actions/contain.md#contain)
### [4.2.3 ALLOW](actions/allow.md#allow)

## [4.3 Actions that Control Activities/Devices](4_example-openc2-usage.md#43-actions-that-control-activitiesdevices)

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

## [4.4 Sensor-Related Actions](4_example-openc2-usage.md#44-sensor-related-actions)

### [4.4.1 DISTILL](actions/distill.md#distill)
### [4.4.2 AUGMENT](actions/autment.md#augment)

## [4.5 Effects-Based Actions](4_example-openc2-usage.md#45-effects-based-actions)

### [4.5.1 INVESTIGATE](actions/investigate.md#investigate)
### [4.5.2 MITIGATE](actions/mitigate.md#mitigate)
### [4.5.3 REMEDIATE](actions/remediate.md#remediate)

## [4.6 Response and Alert](4_example-openc2-usage.md#46-response-and-alert)

### [4.6.1 RESPONSE](actions/response.md#response)
### [4.6.2 ALERT](actions/alert.md#alert)

# [5. Example OpenC2 Use Case: Mitigate Evil Domain](use-cases/mitigate-evil-domain.md)

# [Appendix A. Example OpenC2 Commands](A_example-openc2-commands.md#appendix-a-example-openc2-commands)
