### QUERY
The QUERY action initiates a single request for information.

QUERY, like SCAN, is used to find out more information about the system or its environment. In the case of QUERY, however, it is an isolated or specific information request, rather than a broadly scoped scan or on-going check. QUERY is used to retrieve data that is already present in a database or data store, while SCAN implies a more thorough examination and identification of anomalies (relative to a known good state). The response to a query is typically (but not necessarily) conveyed within the command and control channel.

The target for QUERY is usually openc2:Data. The target-specifier describes the search criteria for the information request.  

A special target for QUERY is openc2:OpenC2 which signifies a request for an actuator's OpenC2 capabilities (i.e., a list of supported actions, targets). If not target-specifier is included in the request then the full report of the actuator's capabilities should be provided. A response could be filtered for a particular capability by providing details in the target-specifier.

**Table. Supported Targets and Actuators: QUERY**

| Target Type |  | Actuator Type | 
| :--- | :--- | :--- | 
| openc2:Data<br>openc2:OpenC2 |  | network.router<br>endpoint<br>network.firewall<br>process.directory-service | 

The QUERY action accepts the following modifiers:

**Table. Modifiers: QUERY**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| response |  | Where and how to direct the response to the query. | All | 

Below is a sample of OpenC2 commands to perform a QUERY of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate.

**Table. Sample of OpenC2 Commands: QUERY**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | List all network connections | QUERY | openc2:Data<hr>openc2:DataObjectType | network.router<hr>(optional) | response | 
| 2 | List running processes on a machine | QUERY | openc2:Data<hr>openc2:DataObjectType | endpoint<hr>(optional) | response | 
| 3 | Request an Actuator's supported OpenC2 capabilities | QUERY | openc2:OpenC2<hr>openc2:OpenC2ObjectType | network.firewall<hr>(optional) | response | 

