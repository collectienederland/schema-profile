# collectie-nederland-schema-profile
This repository describes the schema profile developed for the platform [Collectie Nederland](https://collectienederland.nl/). It is a less-strict version of the [NDE Schema.org Application Profile](https://github.com/netwerk-digitaal-erfgoed/schema-profile), which is described [here](https://docs.nde.nl/schema-profile/). 

## Shacl-file

The shacl shape is located here: ```data/shacl.ttl```.

## Datamodel

```mermaid
---
  config:
    theme: forest
    class:
      hideEmptyMembersBox: true
---
classDiagram
class creativework["CreativeWork, ItemList"]
class product["Product, DefinedTerm"]
class place["Place, DefinedTerm"]
class mediaobject["MediaObject"]
class person["Person, DefinedTerm"]
class occupation["Occupation, DefinedTerm"]
class propval["PropertyValue"]
class copyperson["Person"]

class lit_0["xsd:string"]
class lit_1["xsd:string"]
class lit_2["xsd:anyURI"]
class lit_3["xsd:string"]
class lit_4["xsd:string"]
class lit_5["xsd:string"]
class lit_6["xsd:string"]
class lit_7["xsd:string"]
class lit_8["xsd:string"]
class lit_9["xsd:string"]
class lit_10["xsd:string"]
class lit_11["xsd:string"]
class lit_12["xsd:string"]
class lit_13["xsd:string"]
class lit_14["xsd:anyURI"]
class lit_15["xsd:string"]
class lit_16["xsd:string"]
class lit_17["xsd:anyURI"]
class lit_18["xsd:string"]
class lit_19["xsd:string"]
class lit_20["xsd:string"]
class lit_21["xsd:string"]
class lit_22["xsd:string"]
class lit_23["xsd:anyURI"]

creativework --> lit_1: dateCreated
creativework --> product: material
product --> lit_0: name
product --> lit_2: sameAs
creativework --> place: locationCreated
place --> lit_3: name
place --> lit_4: sameAs
creativework --> person: creator
person --> lit_5: name
person --> lit_6: sameAs
person --> lit_7: deathDate
person --> lit_8: birthDate
creativework --> lit_9: description
creativework --> mediaobject: associatedMedia (encodesCreativeWork)
mediaobject --> lit_10: contentUrl
mediaobject --> lit_11: thumbnailUrl
mediaobject --> lit_12: license
mediaobject --> lit_23:encodingFormat
creativework --> lit_13: size
creativework --> lit_14: isPartOf
creativework --> occupation: hasOccupation
occupation --> lit_15: sameAs
occupation --> lit_16: name
creativework --> lit_17: url
creativework --> propval: identifier
propval --> lit_18: propertyID
propval --> lit_19: value
propval --> lit_20: description
creativework --> copyperson: copyrightHolder
copyperson --> lit_21: name
creativework --> lit_22: temporal
