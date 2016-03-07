### GET
The GET action tasks an entity to retrieve a specific object.
The location of the object can be designated in the specifier of the TARGET.  The entity typically (but not necessarily) retrieves the object outside of the command and control channel.

**Table. Supported Targets and Actuators: GET**

| cybox:Email_Message<br>cybox:File<br>cybox:Memory |  | network.sense_making<br>endpoint.workstation | 

The GET action accepts the following modifiers:

**Table. Modifiers: GET**

| Modifier | Type | Description | Target Applicability | 
| :--- | :--- | :--- | :--- | 
| TBSL |  |  |  | 

Below is a sample of OpenC2 commands to perform a GET of targets, utilizing actuators at different levels of specificity, qualified by modifiers to the action as appropriate. These samples are intended to show the flexibility of the OpenC2 language. A fuller set of example usages can be found in Appendix A.

**Table. Sample of OpenC2 Commands: GET**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | Acting gets the potentially malicious email, including URLs and attachments. | GET | cybox:Email_Message<hr>cybox:EmailMessageObjectType | network.sense_making<hr> |  | 
| 2 | Get process file | GET | cybox:File<hr>cybox:FileObjectType | endpoint.workstation<hr> |  | 
