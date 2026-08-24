## Overview

<pre class="mermaid">
---
  config:
    theme: forest
    nodeSpacing: 20
    rankSpacing: 150
    class:  
      hideEmptyMembersBox: true
---
classDiagram
class creativework["CreativeWork"] {
  xsd:string name
  xsd:string alternateName
  xsd:string creditText
  xsd:string publisher
  xsd:string datePublished
  xsd:string citation
  xsd:string dateCreated
  xsd:string temporal
  xsd:string license
  xsd:string description
  xsd:string size
  xsd:disambiguatingDescription
  xsd:anyURI url
  xsd:anyURI isPartOf
  xsd:date sdDatePublished
}

class additional["Text, DefinedTerm"]
creativework --> additional: additionalType

class product["Product, DefinedTerm"]
creativework --> product: material

class defterm["DefinedTerm"]
creativework --> defterm: genre, keywords, about

class place["Place, DefinedTerm"]
creativework --> place: locationCreated

class person["Person, DefinedTerm"]
creativework --> person: creator

class mediaobject["MediaObject"]
creativework --> mediaobject: associatedMedia (encodesCreativeWork)

class propval["PropertyValue"]
creativework --> propval: identifier

class copyperson["Person"]
creativework --> copyperson: copyrightHolder
</pre>
### Person, Place, Occupation 

Data that includes geocoordinates for places may add this data using the GeoCoordinates class. Data that references the administrative area of a place (e.g. province), may add this using the AdministrativeArea class. 

<pre class="mermaid">
---
  config:
    theme: forest
    class:
      hideEmptyMembersBox: true
---
classDiagram
class creativework["CreativeWork"]
class place["Place, DefinedTerm"]
class geocoor["GeoCoordinates"]
class adminarea["AdministrativeArea, DefinedTerm"]
class lit_3["xsd:string"]
class lit_4["xsd:anyURI"]
class lit_31["xsd:string"]
class lit_32["xsd:anyURI"]
creativework --> place: locationCreated
place --> lit_3: name
place --> lit_4: sameAs
place --> geocoor: geo
place --> adminarea: addressRegion
adminarea --> lit_31: name
adminarea --> lit_32: sameAs

class person["Person, DefinedTerm"]{
  xsd:string name
  xsd:anyURI sameAs
  xsd:string deathDate
  xsd:string birthDate
  xsd:anyURI birthPlace
}
creativework --> person: creator
class occupation["Occupation, DefinedTerm"]{
  xsd:string name
  xsd:anyURI sameAs
}

person --> occupation: hasOccupation
</pre>

### dateCreated and temporal
In case an ISO-8601 value describing when the object was created is available, the field dateCreated must be used. In case another string is available that does not conform to ISO-8601, temporal must be used. In case dateCreated is used, and the value is not of the short form YYYY, xsd:Date may be used.  

<pre class="mermaid">
---
  config:
    theme: forest
    class:
      hideEmptyMembersBox: true
---
classDiagram
class creativework["CreativeWork"]
class lit_1["xsd:string"]
creativework --> lit_1: dateCreated

class lit_22["xsd:string"]
creativework --> lit_22: temporal
</pre>

### MediaObject

Providers that want to include data referencing the name of the holder of the copyright of a MediaObject may do so using the copyrightHolder property. 

<pre class="mermaid">
---
  config:
    theme: forest
    class:
      hideEmptyMembersBox: true
---
classDiagram
class creativework["CreativeWork"]
class lit_10["xsd:anyURI"]
class lit_11["xsd:anyURI"]
class lit_12["xsd:string"]
class lit_23["xsd:anyURI"]
class cpholder["Person"]
class lit_30["xsd:string"]
class mediaobject["MediaObject"]
creativework --> mediaobject: associatedMedia (encodesCreativeWork)
mediaobject --> lit_10: contentUrl
mediaobject --> lit_11: thumbnailUrl
mediaobject --> lit_12: license
mediaobject --> lit_23:encodingFormat
mediaobject --> cpholder:copyrightHolder
cpholder --> lit_30:name
</pre>

### identifier

Identifiers such as the ObjectID in the source collection system or persistent identifiers, may be added using the identifier property using the PropertyValue class. Providers should use a canonical URL in the propertyID property if one is available. 



<pre class="mermaid">
---
  config:
    theme: forest
    class:
      hideEmptyMembersBox: true
---
classDiagram
class creativework["CreativeWork"]
class propval["PropertyValue"]
class lit_18["xsd:string"]
class lit_19["xsd:string"]
class lit_20["xsd:string"]
creativework --> propval: identifier
propval --> lit_18: propertyID
propval --> lit_19: value
propval --> lit_20: description
</pre>

### additionalType, material, genre, keywords en about

<pre class="mermaid">
---
  config:
    theme: forest
    class:
      hideEmptyMembersBox: true
---
classDiagram
class creativework["CreativeWork"]

class additional["Text, DefinedTerm"]
class lit_27["xsd:string"]
class lit_28["xsd:anyURI"]
creativework --> additional: additionalType
additional --> lit_27: name
additional --> lit_28: sameAs

class product["Product, DefinedTerm"]
class lit_0["xsd:string"]
class lit_2["xsd:anyURI"]
creativework --> product: material
product --> lit_0: name
product --> lit_2: sameAs

class defterm["DefinedTerm"]
class lit_29["xsd:string"]
class lit_30["xsd:anyURI"]
creativework --> defterm: genre, keywords, about
defterm --> lit_29: name
defterm --> lit_30: sameAs
</pre>

## Datamodel 

<pre class="mermaid">
---
  config:
    theme: forest
    nodeSpacing: 20
    rankSpacing: 150
    class:  
      hideEmptyMembersBox: true
---
classDiagram
class creativework["CreativeWork"]

class lit_name["xsd:string"]
creativework --> lit_name: name

class lit_cretext["xsd:string"]
creativework --> lit_cretext: creditText

class lit_citation["xsd:string"]
creativework --> lit_citation: citation

class lit_publisher["xsd:string"]
creativework --> lit_publisher: publisher

class lit_alternateName["xsd:string"]
creativework --> lit_alternateName: alternateName

class lit_datePublished["xsd:string"]
creativework --> lit_datePublished: datePublished

class lit_1["xsd:string"]
creativework --> lit_1: dateCreated

class lit_24["xsd:anyURI"]
creativework --> lit_24: license

class lit_9["xsd:string"]
creativework --> lit_9: description

class lit_13["xsd:string"]
creativework --> lit_13: size

class lit_14["xsd:anyURI"]
creativework --> lit_14: isPartOf

class lit_40["CreativeWork"]
creativework --> lit_40: hasPart (isPartOf)

class lit_17["xsd:anyURI"]
creativework --> lit_17: url

class lit_22["xsd:string"]
creativework --> lit_22: temporal

class lit_25["xsd:date"]
creativework --> lit_25: sdDatePublished

class additional["Text, DefinedTerm"]
class lit_27["xsd:string"]
class lit_28["xsd:anyURI"]
creativework --> additional: additionalType
additional --> lit_27: name
additional --> lit_28: sameAs

class product["Product, DefinedTerm"]
class lit_0["xsd:string"]
class lit_2["xsd:anyURI"]
creativework --> product: material
product --> lit_0: name
product --> lit_2: sameAs

class defterm["DefinedTerm"]
class lit_29["xsd:string"]
class lit_30["xsd:anyURI"]
creativework --> defterm: genre, keywords, about
defterm --> lit_29: name
defterm --> lit_30: sameAs

class place["Place, DefinedTerm"]
class geocoor["GeoCoordinates"]
class adminarea["AdministrativeArea, DefinedTerm"]
class lit_3["xsd:string"]
class lit_4["xsd:anyURI"]
class lit_31["xsd:string"]
class lit_32["xsd:anyURI"]
creativework --> place: locationCreated
place --> lit_3: name
place --> lit_4: sameAs
place --> geocoor: geo
place --> adminarea: addressRegion
adminarea --> lit_31: name
adminarea --> lit_32: sameAs

class person["Person, DefinedTerm"]
class lit_5["xsd:string"]
class lit_6["xsd:anyURI"]
class lit_7["xsd:string"]
class lit_8["xsd:string"]
class lit_15["xsd:anyURI"]
class lit_16["xsd:string"]
creativework --> person: creator
person --> lit_5: name
person --> lit_6: sameAs
person --> lit_7: deathDate
person --> lit_8: birthDate
person --> place: birthPlace

class organisation["Organisation, DefinedTerm"]
class organisation_same_as["xsd:anyURI"]
class organisation_name["xsd:string"]
creativework --> organisation: creator
organisation --> organisation_name: name
organisation --> organisation_same_as: sameAs

class occupation["Occupation, DefinedTerm"]
class lit_15["xsd:anyURI"]
class lit_16["xsd:string"]
person --> occupation: hasOccupation
occupation --> lit_15: sameAs
occupation --> lit_16: name

class mediaobject["MediaObject"]
class lit_10["xsd:anyURI"]
class lit_11["xsd:anyURI"]
class lit_12["xsd:string"]
class lit_23["xsd:anyURI"]
creativework --> mediaobject: associatedMedia (encodesCreativeWork)
mediaobject --> lit_10: contentUrl
mediaobject --> lit_11: thumbnailUrl
mediaobject --> lit_12: license
mediaobject --> lit_23:encodingFormat

class propval["PropertyValue"]
class lit_18["xsd:string"]
class lit_19["xsd:string"]
class lit_20["xsd:string"]
creativework --> propval: identifier
propval --> lit_18: propertyID
propval --> lit_19: value
propval --> lit_20: description

class copyperson["Person"]
class lit_21["xsd:string"]
creativework --> copyperson: copyrightHolder
copyperson --> lit_21: name
</pre>

<!--<script type="module">
	import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs';
	mermaid.initialize({
		startOnLoad: true,
		theme: forest
    nodeSpacing: 20
    rankSpacing: 150
    class:  
      hideEmptyMembersBox: true
	});
</script>-->