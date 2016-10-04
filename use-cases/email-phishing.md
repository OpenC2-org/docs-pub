## Use Case: Email Phishing
### Description
TBSL

**Table. Scenario Diagram: Email Phishing**

![alt text](https://github.com/OpenC2-org/docs-members/blob/master/use-cases/email-phishing.png "Use Case Diagram")


**Table. Scenario Steps: Email Phishing**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 |  |  | <hr> | <hr> |  | 
| 2 | Sense-Making receives a potentially malicious email from a user. |  | <hr> | <hr> |  | 
| 3 | Sense-Making alerts Decision-Making about the potentially malicious email. |  | <hr> | <hr> |  | 
| 4 | Decision-Making commands Acting to have the potentially malicious email analyzed. | INVESTIGATE | cybox:Email_Message<hr>cybox:EmailMessageObjectType | <hr> |  | 
| 5 | Acting gets the potentially malicious email, including URLs and attachments. | GET | cybox:Email_Message<hr>cybox:EmailMessageObjectType | network.sense_making<hr> |  | 
| 6 | Acting sends the URL to be analyzed in a sandbox. | DETONATE | cybox:URI<hr>cybox:URIObjectType | process.sandbox<hr> |  | 
| 7 | Acting sends the attachments to be analyzed in a sandbox. | DETONATE | cybox:File<hr>cybox:FileObjectType | process.sandbox<hr> |  | 
| 8 | Acting sends the URL to a reputation service. | QUERY | cybox:URI<hr>cybox:URIObjectType | process.reputation-service<hr> |  | 
|  |  |  | <hr> | <hr> |  | 
| 9 |  |  | <hr> | <hr> |  | 
| 10 | Upon analysis by the sandboxes and/or the reputation service, the results of the analysis are sent to Sense-Making. |  | <hr> | <hr> |  | 
| 11 | Sense-Making confirms the email is malicious. |  | <hr> | <hr> |  | 
| 12 | Sense-Making notifies Decision-Making that the email is malicious. |  | <hr> | <hr> |  | 
| 13 | Decision-Making commands Acting to block the identified URL. | DENY | cybox:URI<hr>cybox:URIObjectType | <hr> |  | 
| 14 | Acting commands the network firewall(s) to block the maliciuos URL. | DENY | cybox:URI<hr>cybox:URIObjectType | network.firewall<hr> |  | 
| 15 | Acting commands the deletion of the malicious email. | REMOVE | cybox:Email_Message<hr>cybox:EmailMessageObjectType | process.email-service<hr> |  | 

