### REDIRECT
The REDIRECT action changes the flow of traffic to a particular destination other than its original intended destination.

The REDIRECT action includes the case of bypassing an intermediate point. REDIRECT is distinct from MOVE in that it encompasses the entire flow rather than a single instance, item or object. MOVE supports the more atomic case.

**Table. Supported Targets and Actuators: REDIRECT**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| cybox:Network_Connection<br>cybox:URI |  | network.router | 

The REDIRECT action accepts the following modifiers:

**Table. Modifiers: REDIRECT**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| where |  | Optional. The location within the enclave to redirect the target.  "where = null" will cancel previous redirection actions. | All | 

Below is a sample of OpenC2 commands to perform a REDIRECT of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: REDIRECT**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Redirect traffic to a honeypot; suitable for coordinating across multiple enclaves and allowing enclaves to determine most appropriate response | REDIRECT | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> | where | 
| 2 | Redirect traffic to a honeypot at a specific router | REDIRECT | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | network.router<hr> | where | 
| 3 | Cancel traffic redirection; suitable for coordinating across multiple enclaves and allowing enclaves to determine most appropriate response | REDIRECT | cybox:Network_Connection<hr>cybox:NetworkConnectionObjectType | <hr> | where = null | 

