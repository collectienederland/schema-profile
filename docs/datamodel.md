## Overzicht

Het datamodel voor Collectie Nederland gebruikt schema.org als beschrijvende vocabulaire. Hieronder is een overzicht van het datamodel te zien. Als centrale klasse word [CreativeWork](https://schema.org/CreativeWork) gebruikt.

<pre class="mermaid">
---
  config:
    theme: forest
    class:
      hideEmptyMembersBox: true
---
classDiagram
class creativework["CreativeWork"] {
  name xsd:string 
  alternateName xsd:string 
  creditText xsd:string 
  publisher xsd:string 
  datePublished xsd:string 
  citation xsd:string 
  dateCreated xsd:string 
  temporal xsd:string 
  license xsd:string 
  description xsd:string 
  size xsd:string 
  url xsd:anyURI 
  isPartOf xsd:anyURI 
  sdDatePublished xsd:date 
}

class additional["Text, DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> additional: additionalType

class product["Product, DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> product: material

class defterm["DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> defterm: genre, keywords, about
class place["Place, DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
class geocoor["GeoCoordinates"] {
  latitude xsd:string
  longitude xsd:string
}
class adminarea["AdministrativeArea, DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> place: locationCreated
place --> geocoor: geo
place --> adminarea: addressRegion

class person["Person, DefinedTerm"]{
  name xsd:string 
   sameAs xsd:anyURI 
  deathDate xsd:string 
  birthDate xsd:string 
  birthPlace xsd:anyURI 
}
creativework --> person: creator
class occupation["Occupation, DefinedTerm"]{
  name xsd:string 
  sameAs xsd:anyURI 
}
person --> occupation: hasOccupation

class mediaobject["MediaObject"] {
  contentUrl xsd:anyURI
  thumbnailUrl xsd:anyURI
  license xsd:string
  encodingFormat xsd:anyURI
}
creativework --> mediaobject: associatedMedia (encodesCreativeWork)
mediaobject --> person:copyrightHolder

class propval["PropertyValue"] {
  propertyID xsd:string
  value xsd:string
  description xsd:string
}
creativework --> propval: identifier

</pre>

### Person, Place, Occupation 

Gegevens over het ontstaan van een werk worden in het model weergegeven als volgt.

<pre class="mermaid">
---
  config:
    theme: forest
    class:
      hideEmptyMembersBox: true
---
classDiagram
class creativework["CreativeWork"] {
  dateCreated xsd:string
  temporal xsd:string
}
class place["Place, DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
class geocoor["GeoCoordinates"] {
  latitude xsd:string
  longitude xsd:string
}
class adminarea["AdministrativeArea, DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> place: locationCreated
place --> geocoor: geo
place --> adminarea: addressRegion

class person["Person, DefinedTerm"]{
  name xsd:string 
   sameAs xsd:anyURI 
  deathDate xsd:string 
  birthDate xsd:string 
  birthPlace xsd:anyURI 
}
creativework --> person: creator
class occupation["Occupation, DefinedTerm"]{
  name xsd:string 
  sameAs xsd:anyURI 
}

person --> occupation: hasOccupation
</pre>

#### [Person](https://schema.org/Person)
De maker van het werk. In sommige gevallen kan dit een organisatie zijn. 
#### [Occupation](https://schema.org/Occupation)
De rol van de maker van het werk.
#### [Place](https://schema.org/Place)
De plek waar het werk gemaakt is.
#### [GeoCoordinates](https://schema.org/CreativeWork)
De coordinaten van de plek waar het werk gemaakt is.
#### [AdministrativeArea](https://schema.org/AdministrativeArea)
De provincie van de plek waar het werk gemaakt is.
#### [dateCreated](https://schema.org/dateCreated) and [temporal](https://schema.org/temporal)
Als de datum van de creatie door middel van een ISO-8601 conformerende waarde beschikbaar is, wordt die opgenomen in het veld dateCreated. Zo niet, kan temporal worden gebruikt.

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

class mediaobject["MediaObject"] {
  contentUrl xsd:anyURI
  thumbnailUrl xsd:anyURI
  license xsd:string
  encodingFormat xsd:anyURI
}
creativework --> mediaobject: associatedMedia (encodesCreativeWork)
class cpholder["Person"] {
  name xsd:string
  sameAs xsd:anyURI
}
mediaobject --> cpholder:copyrightHolder
</pre>
#### [MediaObject](https://schema.org/MediaObject)
De link naar beschikbare media van het werk word gemaakt door middel van het MediaObject. 
#### [copyrightHolder](https://schema.org/copyrightHolder)
Als MediaObjecten onder copyright vallen, kan dat opgenomen worden door middel van de relatie copyrightHolder.

### identifier
IDs, bijvoorbeeld PIDs of IDs uit het collectiebeheersysteem die voor context belangrijk zijn kunnen worden toegevoegd door middel van de PropertyValuye klasse. 

<pre class="mermaid">
---
  config:
    theme: forest
    class:
      hideEmptyMembersBox: true
---
classDiagram
class creativework["CreativeWork"]
class propval["PropertyValue"] {
  propertyID xsd:string
  value xsd:string
  description xsd:string
}
creativework --> propval: identifier
</pre>

### additionalType, material, genre, keywords en about

Beschrijvende gegevens over het werk worden op de volgende manier opgenomen. 

<pre class="mermaid">
---
  config:
    theme: forest
    class:
      hideEmptyMembersBox: true
---
classDiagram
class creativework["CreativeWork"]

class additional["Text, DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> additional: additionalType

class product["Product, DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> product: material

class defterm["DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> defterm: genre, keywords, about
</pre>
#### [Product](https://schema.org/Product)
Materiaal van het werk.
#### [Text](https://schema.org/Text)
Aanvullende tekstuele beschrijving. 
#### [DefinedTerm](https://schema.org/DefinedTerm)
Aanvullende relevante termen.

<script type="module">
	import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs';
	mermaid.initialize({
		startOnLoad: true,
		theme: 'dark'
	});
</script>