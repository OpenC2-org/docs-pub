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

