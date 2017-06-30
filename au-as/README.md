# Conformance class: Application schema, Administrative Units - Administrative Units (DRAFT)

Conformance class for the requirements associated with the application schema. 

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schemas, Administrative Units - Administrative Units".

This conformance class is part of the [Abstract Test Suite for the INSPIRE Data Specification on Administrative Units](http://inspire.ec.europa.eu/id/ats/data-au/3.1).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

none

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-AU](http://inspire.ec.europa.eu/id/ats/data-au/3.1/au-as/README#ref_TG_DS_HY) | [GML application schemas, Administrative Units](http://inspire.ec.europa.eu/id/ats/data-au/3.1/hy-gml) | INSPIRE spatial data set encoded in GML, Administrative Units features | n/a |
 
## Feature types <a name="feature-types"></a>

The instantiable feature types in the application schema are:

* AdministrativeBoundary
* AdministrativeUnit
* Condominium
* Baseline
* MaritimeBoundary
* MaritimeZone

*Note*: When "features" or "spatial objects" are mentioned in the test cases, this refers only to instances of feature types of this application schema, not to any types specified in any other application schema.

## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
TG DS-AU <a name="ref_TG_DS_AU"></a>   | [INSPIRE Data Specification on Administrative Units – Technical Guidelines version 3.1](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_AU_v3.1.pdf)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-AU](#ref_TG_DS_AU)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Code list values](http://inspire.ec.europa.eu/id/ats/data-au/3.1/au-as/code-list-values)  | Draft  | A.1.3  |
| [Constraints](http://inspire.ec.europa.eu/id/ats/data-au/3.1/au-as/constraints)  | Draft  | A.1.6  |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
net3           | urn:x-inspire:specification:gmlas:Network:3.2
net4           | http://inspire.ec.europa.eu/schemas/net/4.0
au          | http://inspire.ec.europa.eu/schemas/au/4.0 or urn:x-inspire:specification:gmlas:AdministrativeUnits:3.0
au3          | urn:x-inspire:specification:gmlas:AdministrativeUnits:3.0
net            | urn:x-inspire:specification:gmlas:Network:3.2 or http://inspire.ec.europa.eu/schemas/net/4.0
base           | http://inspire.ec.europa.eu/schemas/base/3.3
gml            | http://www.opengis.net/gml/3.2
wfs            | http://www.opengis.net/wfs/2.0
xsi            | http://www.w3.org/2001/XMLSchema-instance
xlink          | http://www.w3.org/1999/xlink
xml            | http://www.w3.org/XML/1998/namespace

