### QUERY
The QUERY action initiates a single request for information.
QUERY, like SCAN, is used to find out more information about the system or its environment.  In the case of QUERY, however, it is an isolated or specific information request, rather than a broadly scoped scan or on-going check.  QUERY tends to be a simple retrieval of a value for a specific parameter, while SCAN implies a more thorough examination and identification of anomalies (relative to a known good state).   The response to a query is typically (but not necessarily) conveyed within the command and control channel.

**Table. Supported Targets and Actuators: QUERY**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| openc2:Data |  | network.router<br>endpoint<br>process.directory-service | 

The QUERY action accepts the following modifiers:

**Table. Modifiers: QUERY**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| response |  | Where and how to direct the response to the query. | All | 

Below is a sample of OpenC2 commands to perform a QUERY of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate. These samples are intended to show the flexibility of the OpenC2 language. A fuller set of example usages can be found in Appendix A.

**Table. Sample of OpenC2 Commands: QUERY**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | List all network connections | QUERY | openc2:Data<hr>openc2:DataObjectType | network.router<hr>(optional) | response | 
| 2 | List running processes on a machine | QUERY | openc2:Data<hr>openc2:DataObjectType | endpoint<hr>(optional) | response | 
| 3 | Get attributes of a user | QUERY | openc2:Data<hr>openc2:DataObjectType | process.directory-service<hr>(optional) | response | 
