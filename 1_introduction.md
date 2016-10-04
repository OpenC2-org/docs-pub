# [FORWARD](0_forward.md#forward)

# 1. Introduction

Cyberattacks are increasingly more sophisticated, less expensive to execute, dynamic, and automated. Current cyber defense products are typically integrated in a unique or proprietary manner and statically configured. As a result, upgrading or otherwise modifying tightly integrated, proprietary cyber defense’s functional blocks is resource intensive; cannot be realized within a cyber-relevant timeframe; and the upgrades may degrade the overall performance of the system.

Future cyber defenses against current and pending attacks require the integration of new or upgraded functional capabilities, the coordination of responses across domains, synchronization of response mechanisms, and deployment of automated actions in cyber relevant time.

Standardization of the lexicons and languages used in the interfaces and protocols necessary for machine-to-machine command and control communications in cyber relevant time will enable cyber defense system flexibility, interoperability, and responsiveness in cyber relevant time.

## 1.1 Purpose

The purpose of the Open Command and Control (OpenC2) Language Description Document is to define a language and lexicon at a level of abstraction that will enable the coordination and execution of command and control of cyber defense components between domains and within a domain. It is expected that the OpenC2 language can be profiled (e.g., applicable commands, applicable values) by community groups for specific uses like Software Defined Networking.

## 1.2 Scope

The scope of this document is to create a set of terms that define the actions, the target of the actions, and the entities that execute the actions. The document also defines an extensible syntax to accommodate attributes that further specify the targets, components, and modify actions to support a wide range of operational environments.

Future OpenC2 efforts will further refine the controlled vocabulary and define implementation approaches to facilitate interoperable machine to machine communications. These efforts will support the development and promulgation of reference implementations to demonstrate the use and flexibility of the OpenC2 language and promote the incorporation of OpenC2 in cyber defense solutions.

The definition of a language such as OpenC2 is necessary but insufficient to enable future cyber defenses. OpenC2 commands can be carried within any number of constructs (e.g., STIX, workflows, playbooks). In addition, OpenC2 is designed to be flexible, agnostic of external protocols that provide services such as transport, authentication, key management and other services. Cyber defense implementations will still need to rely on other protocols and security services.

## 1.3 Intended Audience

This OpenC2 Language Description Document is intended for organizations investigating the implementation of automated pre-approved cyber defensive measures as well as academia and industry partners involved with the development and integration of security orchestration, network components or services, endpoint security applications, and security services for cyber defenses.

## 1.4 Document Overview

[Section 1, Introduction](#1-introduction), describes the impetus for the OpenC2 language and lays out the purpose, scope, and intended audience of the document.

[Section 2, Background](2_background.md#2-background), describes the design principles for the language and how the language can be contextualized for different operating environments.

[Section 3, OpenC2 Language](3.0_openc2-language.md#3-openc2-language), describes the abstract syntax and the basic building blocks of the language. It also further specifies the vocabulary for actions, targets, actuators, and modifiers.

[Section 4, Example OpenC2 Usage](4_example-openc2-usage.md#4-example-openc2-usage), provides examples of OpenC2 command constructs. For each action, the supported targets, actuators, and action specific modifiers are identified and example usages are provided.

[Section 5, Example OpenC2 Use Case](5_example-openc2-use-case.md#5-example-openc2-use-case), depicts an example use case for mitigating an evil domain. The use case shows the OpenC2 commands that could be used to mitigate the attacks or vulnerabilities and where they could be applied.

[Appendix A, Example OpenC2 Commands](A_example-openc2-commands.md#appendix-a-example-openc2-commands), contains example OpenC2 commands organized in tables by OpenC2 action. These example commands were based on use cases provided by government agencies, critical infrastructure, industry (e.g., security orchestrator, actuator, and sensor) and academia.

# [2. Background](2_background.md#2-background)
