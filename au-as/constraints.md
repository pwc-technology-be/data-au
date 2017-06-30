# Constraints

**Version**: 1

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

Verify that the OCL constraints listed below that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation). 

For constraints that require retrieving a referenced resource and the resource cannot be retrieved, report [brokenLink](#brokenLink). The test accepts the following two types of content in @xlink:href attributes: Either a "#" followed by a @gml:id in the same document or a HTTP URI.

Automated tests:

* No unit at highest level can associate units at a higher level; OCL: "inv: self.nationalLevel = '1stOrder' implies self.upperLevelUnit->isEmpty() and self.loweLevelUnit->notEmpty()". Verify that units of [nationalLevel](#nationalLevel) 1stOrder do not reference a unit in [upperLevelUnit](#upperLevelUnit)
* No unit at lowest level can associate units at lower level; OCL: "inv: self.nationalLevel = '6thOrder' implies self.lowerLevelUnit->isEmpty and self.upperLevelUnit->notEmpty". Verify that units of [nationalLevel](#nationalLevel) 6thOrder do not reference a unit in [lowerLevelUnit](#lowerLevelUnit)
* Association role condominium applies only for administrative units which nationalLevel='1st order' (country level); OCL: "inv: self.condominium->notEmpty implies self.nationalLevel = '1stOrder'". Verify that [condominium](#condominium) is only set, if the [nationalLevel](#nationalLevel) is 1stOrder.

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-cp/3.2/cp-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-PS](http://inspire.ec.europa.eu/id/ats/data-cp/3.2/cp-as/README#ref_TG_DS_PS)) 5.4

**Test type**: Automated

**Notes** 


## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-au/3.2/au-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
nationalLevel <a name="nationalLevel"></a> 	| 	//schema-element(au:AdministrativeUnit)/au:nationalLevel/@xlink:href or //schema-element(au3:AdministrativeUnit)/au3:nationalLevel/text()
upperLevelUnit <a name="upperLevelUnit"></a> 	| 	//schema-element(au:AdministrativeUnit)/au:upperLevelUnit
lowerLevelUnit <a name="lowerLevelUnit"></a> 	| 	//schema-element(au:AdministrativeUnit)/au:lowerLevelUnit
condominium <a name="condominium"></a> 	| 	//schema-element(au:AdministrativeUnit)/au:condominium
