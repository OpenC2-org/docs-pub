## Use Case: Update Sensor Signatures
### Description
TBSL

**Table. Scenario Diagram: Update Sensor Signatures**

![alt text](https://github.com/OpenC2-org/docs-members/blob/master/use-cases/update-sensor-sig.png "Use Case Diagram")


**Table. Scenario Steps: Update Sensor Signatures**

|  | DESCRIPTION | ACTION | TARGET<hr>TARGET-SPECIFIER | ACTUATOR<hr>ACTUATOR-SPECIFIER | MODIFIER | 
| :--- | :--- | :--- | :--- | :--- | :--- | 
| 1 | [Assume Snort is already running] |  | <hr> | <hr> |  | 
| 2 | Decision-Making commands Acting to update sensors' signatures. |  | <hr> | <hr> |  | 
| 3 | Acting sends command to "Rules Manager" to update sensors' signatures. | UPDATE | data.signature<hr>id = <SIGNATURE_ID>, <br>ruleset = <RULESET> | <hr> |  | 
| 4 | Upon signature update, restart the sensor. | RESTART | cybox:Product<hr>id = <PRODUCT_ID> | <hr> | delay = 0..n (seconds) | 
| 5 | Rules Manager commands the sensor to update their signatures. |  | <hr> | <hr> |  | 
|  | [Alternative Commands] |  | <hr> | <hr> |  | 
| 6a | Acting sends to the Rules Manager a reference to a signature file that contains the new or updated rules. | UPDATE | data.signature<hr>id = <SIGNATURE_ID>, file = <FILE_REF> | <hr> |  | 
| 6b | Acting commands the Rules Manager to retrieve updated rules from a Rules Provider. | UPDATE | data.signature<hr>id = (<PROVIDER_ID>, [<RULESET_ID>] | <hr> |  | 
| 6c | Acting commands the Rules Manager to remove signature rules. | DELETE | data.signature<hr>id = <SIGNATURE_ID>, <br>ruleset = <RULESET> | <hr> |  | 
| 7 |  |  | <hr> | <hr> |  | 

