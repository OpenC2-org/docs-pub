# Abstract Syntax

Conceptually, an OpenC2 command has the following form:

```
<ACTION> (
    TARGET (
        type = <TARGET_TYPE>,
        [<target-specifier>]
    ),
    [ACTUATOR (
        type = <ACTUATOR_TYPE>,
        [<actuator-specifier>]
    )],
    [<modifiers>]
)
```

Fields denoted with angle brackets (“<>“) are replaced with the appropriate details.  Fields denoted with square brackets (“[]”) are optional. Actual implementation approaches will leverage pre-existing conventions and notations such as XML, JSON, and Type-Length-Value delimitation.

The OpenC2 command accepts the following fields:

| Field | Type | Description |
| :--- | :--- | :--- |
| **ACTION** | | Required. The task or activity to be performed (i.e., the 'verb'). |
| **TARGET** | | Required. The object of the action. The ACTION is performed on the TARGET. |
| **type** | namespace:target | Required. The TARGET type will be defined within the context of a namespace. |
| **target-specifier** | namespace:target-specifier | Optional. The specifier further describes a specific target, a list of targets, or a class of targets. |
| **ACTUATOR** | | Optional. The subject of the action. The ACTUATOR executes the ACTION on the TARGET. |
| **type** | namespace:actuator | The ACTUATOR type will be defined within the context of a namespace. |
| **actuator-specifier** | namespace:actuator-specifier | Optional. The specifier further describes a specific actuator, a list of actuators, or a class of actuators. |
| **_modifiers_** | | Optional. Provide additional information about the action such as time, periodicity, duration, and location. |

There are cases where an ACTION and TARGET are sufficient to complete the command, especially in the case of inter-domain commands where the method or approach to complete or execute the action can be determined within the receiving domain/enclave.

The majority of commands within an enclave will have an ACTION, TARGET and ACTUATOR.  Inclusion of the ACTUATOR provides additional context for the command as a whole and enables efficiency.

Specifiers for TARGETs and ACTUATORs are optional and can be used to provide context specific information that could be used to reflect the local environment, policies, and operational conditions within an enterprise/enclave.  Specifiers can call out a specific target/actuator, a list of targets/actuators, or a class of targets/actuators.

Modifiers to the ACTION are optional and are used to provide effect based context to the ACTION.  Modifiers are further discussed in Section 3.2.5.

The following table illustrates the use of specifiers and modifiers to extend the range of OpenC2 commands to cover the higher level ‘strategic’ commands to the unambiguous enclave-specific use case.  This provides greater flexibility to the language and allows the OpenC2 actions to be further contextualized for the mission environment. The figure below provides some examples of the different levels of specificity achievable in an OpenC2 command.

| DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | 
| Block traffic to/from specific IP address [effects-based, no actuator specified]; suitable for inter-domain coordination | DENY | Network Connection<hr>Source and Destination IP Address | | |
| Block traffic at all network devices [specify actuator class]; suitable for inter-domain coordination or as a command to an orchestration engine which further contextualizes for the enclave’s environment | DENY | Network Connection<hr>Source and Destination IP Address | Network (any devices)<hr> | |
| Block traffic at network routers [specify type of network device actuator]; suitable within an enclave | DENY | Network Connection<hr>Source and Destination IP Address | Network.router<hr>(optional) | |
| Block traffic at specific network router;[specify identity of network router]; suitable within an enclave | DENY | Network Connection<hr>Source and Destination IP Address | Network.router<hr>Router identity | |
| Block access to bad external IP by null routing; [specify method of performing action]; suitable within an enclave | DENY | Network Connection<hr>Source and Destination IP Address | Network.router<hr>(optional) | Method = blackhole |
