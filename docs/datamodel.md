Deze pagina documenteert het datamodel voor het vernieuwde platform van [Collectie Nederland](https://collectienederland.nl/). Het datamodel gebruikt Schema.org als beschrijvende vocabulaire, en is ontwikkeld voor de vernieuwing van het platform [Collectie Nederland](https://collectienederland.nl/). Het model is een uitbreiding van het [NDE Schema.org Applicatieprofiel](https://github.com/netwerk-digitaal-erfgoed/schema-profile), versie [Version 1.2.0 (2026-07-09)](https://docs.nde.nl/schema-profile/#v1.2.0), dat hier [hier](https://docs.nde.nl/schema-profile/) beschreven staat. Afwijkingingen van het NDE applicatieprofiel zijn gemarkeerd door middel van een asterisk (*).

Kardinaliteit van velden worden beschreven in de [Aanlevervoorwaarden](https://collectienederland.github.io/schema-profile/docs/aanlevervoorwaarden.html).

## Overzicht


Hieronder is een overzicht van het datamodel te zien. Als centrale klasse word [CreativeWork](https://schema.org/CreativeWork) gebruikt.

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
  alternateName* xsd:string 
  creditText* xsd:string 
  publisher* xsd:string 
  datePublished* xsd:string 
  citation* xsd:string 
  dateCreated xsd:string 
  temporal* xsd:string 
  license* xsd:string 
  description xsd:string 
  size xsd:string 
  url xsd:anyURI 
  isPartOf xsd:anyURI 
  sdDatePublished xsd:date 
}

class additional["Text*, DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> additional: additionalType

class product["Product*"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> product: material

class defterm["DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> defterm: genre, keywords, about
class place["Place"] {
  name xsd:string
  sameAs xsd:anyURI
}
class geocoor["GeoCoordinates"] {
  latitude xsd:string
  longitude xsd:string
}
class adminarea["AdministrativeArea*, DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> place: locationCreated
place --> geocoor: geo
place --> adminarea: addressRegion

class person["Person"]{
  name xsd:string 
  sameAs xsd:anyURI 
  deathDate xsd:string  
  birthDate xsd:string 
}
creativework --> person: creator
person --> place: birthPlace
person --> place: deathPlace

class occupation["Occupation, DefinedTerm"]{
  name xsd:string 
  sameAs xsd:anyURI 
}
person --> occupation: hasOccupation

class mediaobject["MediaObject"] {
  contentUrl xsd:anyURI
  thumbnailUrl xsd:anyURI
  license xsd:string
  copyrightNotice xsd:string
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
  temporal* xsd:string
}
class place["Place"] {
  name xsd:string
  sameAs xsd:anyURI
}
class geocoor["GeoCoordinates"] {
  latitude xsd:string
  longitude xsd:string
}
class adminarea["AdministrativeArea*, DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> place: locationCreated
place --> geocoor: geo
place --> adminarea: addressRegion

class person["Person"]{
  name xsd:string 
  sameAs xsd:anyURI 
  deathDate xsd:string 
  birthDate xsd:string 
}
person --> place: birthPlace
person --> place: deathPlace

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
De rol van de maker van het werk, bv. 'schilder'.
#### [Place](https://schema.org/Place)
De plek waar het werk gemaakt is.
#### [GeoCoordinates](https://schema.org/CreativeWork)
De coördinaten van de plek waar het werk gemaakt is.
#### [AdministrativeArea](https://schema.org/AdministrativeArea)
De provincie waarin de plek zich bevindt.
#### [dateCreated](https://schema.org/dateCreated) and [temporal](https://schema.org/temporal)
Als de datum van de creatie door middel van een ISO-8601 conformerende waarde beschikbaar is, wordt die opgenomen in het veld dateCreated. Zo niet, kan temporal worden gebruikt.

### MediaObject

Rechthebbenden van een MediaObject, zoals een afbeelding kunnen opgenomen worden als copyrightHolder. 

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
  license* xsd:string
  copyrightNotice xsd:string
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
##### [license*](https://schema.org/license)
Rechtenstatement vanuit brondata edm:rights.
##### [copyrightNotice](https://schema.org/copyrightNotice)
Rechtenstatement vanuit brondata dc:rights.
##### [copyrightHolder](https://schema.org/copyrightHolder)
Als MediaObjecten onder copyright vallen, kan dat opgenomen worden door middel van de relatie copyrightHolder.


### [identifier](https://schema.org/identifier)
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

### [additionalType](https://schema.org/additionalType), [material](https://schema.org/material), [genre](https://schema.org/genre),[keywords](https://schema.org/keywords), [about](https://schema.org/about)
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

class additional["Text*, DefinedTerm"] {
  name xsd:string
  sameAs xsd:anyURI
}
creativework --> additional: additionalType

class product["Product*"] {
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
#### [material](https://schema.org/material)
Materiaal dat bij de vervaardiging van het werk gebruikt is.
#### [additionalType](https://schema.org/additionalType)
Aanvullende tekstuele beschrijving, of categorisering van het werk. 
#### [DefinedTerm](https://schema.org/DefinedTerm)
Aanvullende relevante termen via relaties genre, keywords en about.

<script type="module">
	import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs';
	mermaid.initialize({
		startOnLoad: true,
		theme: 'dark'
	});
</script>