# Aanlevervoorwaarden voor CollectieNederland.nl

## Inleiding

Op deze pagina worden de data-aanlevervoorwaarden beschreven voor
CollectieNederland.nl. Deze omschrijving is gebaseerd op het [nieuwe
datamodel voor
Collectienederland.nl](https://github.com/collectienederland/schema-profile).
Dit model is gebaseerd op het [Schema.org Application Profile for
NDE](https://docs.nde.nl/schema-profile/) en volgt dit
applicatieprofiel. Zodoende zijn de data-aanlevervoorwaarden ook in lijn
met het NDE applicatieprofiel. Maar betreft het een domein
specificering.

Let wel, op enkele punten wijken de aanlevervoorwaarden voor
CollectieNederland.nl af van het NDE Application Profile. Het gaat hier
altijd om versoepelingen en aanvullingen ten op zichten van het NDE
Applicatieprofiel, nooit om striktere eisen. Deze punten zijn terug te
vinden onder kopje 1.4.

De velden die minimaal nodig zijn om data aan te leveren aan
CollectieNederland.nl staan genoteerd onder kopje 1.2.

## Minimale velden voor CollectieNederland.nl

Bij het aanleveren van collectiedata aan CollectieNederland.nl wordt
gekeken naar of de volgende minimale velden aanwezig zijn in de data en
of de inhoud van deze velden in lijn is met het Schema.org Application
Profile for NDE en het aanvullende Collectie Nederland: Schema Profile.
Als er voor een veld een afwijking of versoepeling geldt, dan is deze
leidend ten opzichte van het NDE Application Profile. Bij overlap tussen
de twee profielen verwijst deze pagina door naar het NDE Application
Profile.

- **schema:additionalType**

  - Specifiek type van het werk (bijv. schilderij)

  - <https://docs.nde.nl/schema-profile/#subclasses>

- **schema:conditionsOfAccess**:

  - alleen benodigd voor Rijksmusea.

  - Actuele juridische status (Rijksmusea, Erfgoedwet)

  - *Waarde moet nog bepaald worden*

- **schema:isPartOf**:

  - Dataset of collectie waartoe het werk behoort

  - <https://docs.nde.nl/schema-profile/#CreativeWork-isPartOf>

- **schema:publisher**

  - Naam van de instelling / dataprovider

  - Wordt door CollectieNederland.nl opgehaald uit het NDE Dataset
    Register.

<!-- -->

- **schema:TemporalCoverage**

  - Datering — tekst, jaar of periode-URI

  - Minstens één datering verplicht. Formaat: string, integer of URI

  - <https://docs.nde.nl/schema-profile/#CreativeWork-temporalCoverage>

<!-- -->

- **schema:Creator**

  - Maker van het werk

  - <https://docs.nde.nl/schema-profile/#CreativeWork-creator>

- **schema:url**:

  - Link terug naar het record bij de bronhouder

  - <https://docs.nde.nl/schema-profile/#CreativeWork-URI>

- **schema:licence**

  - Rechtenstatement van het werk zelf (URI)

  - [https://docs.nde.nl/schema-profile/#MediaObject-license](https://docs.nde.nl/schema-profile/).

  - *NDE heeft alleen een licentie als verplicht bij MediaObject.*

  - *CN-extensie op CreativeWork-niveau*

> Als er een afbeelding (**schema:MediaObject**) aanwezig is, zijn de
> volgende velden verplicht:

- **schema:contentUrl**

  - Directe URI naar het mediabestand, verplicht als geldige URI.

  - <https://docs.nde.nl/schema-profile/#MediaObject-contentUrl>

- **schema:license**

  - Rechtenstatement van de afbeelding, verplicht als URI.

  - <https://docs.nde.nl/schema-profile/#MediaObject-license>

> Als er een persoon of organisatie (**schema:Person** en
> **schema:Organisation**) aanwezig is, zijn de volgende velden
> verplicht:

- **schema:name**

  - Naam van de persoon of organisatie

  - <https://docs.nde.nl/schema-profile/#Person-name>

  - <https://docs.nde.nl/schema-profile/#Organization-name>

> Als er gestructureerd afmetingen (**schema:QuantativeValue**) aanwezig
> zijn, zijn de volgende velden verplicht:

- **schema:value**

  - Numerieke waarde van de afmeting

- **schema:unitText**

  - Eenheid als tekst (bijv. 'cm', 'kg')

  - Xsd:string

> Als er een thesaurustermen (**schema:DefindedTerm**) aanwezig zijn,
> zijn de volgende velden verplicht:

- **schema:name**

  - Naam van de thesaurusterm

  - <https://docs.nde.nl/schema-profile/#reference-terms>

  - rdf:langString verplicht (bijv. 'olieverf'@nl)

  - Zie punt 1.5

> Als er geografische coördinaten (**schema:GeoCoordinates**) aanwezig
> zijn, zijn de volgende velden verplicht:

- **schema:latitude**

  - Breedtegraad

  - <https://docs.nde.nl/schema-profile/#GeoCoordinates-latitude>

- **schema:longitude**

  - Lengtegraad

  - <https://docs.nde.nl/schema-profile/#GeoCoordinates-longitude>

## Aanbevolen velden

- **schema:about**

  - Onderwerp of geassocieerde persoon / concept

  - [https://docs.nde.nl/schema-profile/#CreativeWork-about](https://docs.nde.nl/schema-profile/)

- **Schema:copyrightHolder**

  - Rechthebbende van het werk

  - [https://docs.nde.nl/schema-profile/#MediaObject-copyrightNotice](https://docs.nde.nl/schema-profile/)

- **Schema:material**

  - Materiaal of techniek, URI bij voorkeur (AAT)

  - [https://docs.nde.nl/schema-profile/#CreativeWork-material](https://docs.nde.nl/schema-profile/)

- **schema:locationCreated**

  - Plaats van productie, URI bij voorkeur (GeoNames, TGN)

  - [https://docs.nde.nl/schema-profile/#CreativeWork-locationCreated](https://docs.nde.nl/schema-profile/)

- **Schema:description**

  - Beschrijving

  - [https://docs.nde.nl/schema-profile/#CreativeWork-description](https://docs.nde.nl/schema-profile/).

- **schema:size**

  - Afmetingen als vrije tekst (bijv. '24,5 × 20,5 cm')

  - [https://docs.nde.nl/schema-profile/#CreativeWork-size](https://docs.nde.nl/schema-profile/)

<!-- -->

- **schema:name**

  - Naam of titel van het werk

  - [https://docs.nde.nl/schema-profile/#CreativeWork-name](https://docs.nde.nl/schema-profile/).

- **schema:dateCreated**

  - Vervaardigingsdatum conform ISO-8601

  - <https://docs.nde.nl/schema-profile/#CreativeWork-dateCreated>.

- **schema:temporal**

  - Ongestructureerde datering als vrije tekst (bijv. 'ca. 1650')

  - *Toevoeging op het NDE Application Profile*

<!-- -->

- **schema:MediaObject** en **schema:associatedMedia**

  - Digitale representatie van een werk (afbeelding, scan, audio, video)
    en koppeling naar digitale representatie (MediaObject)

  - <https://docs.nde.nl/schema-profile/#MediaObject>

  - <https://docs.nde.nl/schema-profile/#CreativeWork-associatedMedia>

- **schema:contentLocation**

  - Afgebeelde of genoemde locatie in het werk

  - [https://docs.nde.nl/schema-profile/#CreativeWork-contentLocation](https://docs.nde.nl/schema-profile/)

<!-- -->

- **schema:identifier**

  - Inventarisnummer, lokale identificatie of PID van het werk. Niet te
    verwarren met de URI van het object zelf.

  - Is een versoepeling ten opzichte van het NDE Application Profile

  - <https://docs.nde.nl/schema-profile/#CreativeWork-identifier>

- **schema:DefinedTerm -\> schema:sameAs**

  - Thesaurus-URI van de AAT, CHT, Geonames of Wikidata

  - NDE gebruikte **schema:url**; CN corrigeert naar **schema:sameAs**

  - <https://docs.nde.nl/schema-profile/#reference-terms>

<!-- -->

- **schema:provenance**

  - ….Nader te bepalen op basis van modellering

<!-- -->

- **schema:name**

  - Naam of titel van het werk

  - <https://docs.nde.nl/schema-profile/#CreativeWork-name>

- **schema:isPartOf**

  - Dataset of (deel)collectie waartoe het werk behoort

  - Niet verplicht gesteld door CollectieNederland.nl, wel aanbevolen

  - <https://docs.nde.nl/schema-profile/#CreativeWork-isPartOf>

## Afwijkingen en versoepelingen ten opzichte van het Schema.org Application Profile for NDE

**Afwijkingen en versoepelingen**

- **schema:name**

  - Naam of titel van het werk

  - Dit veld stelt CollectieNederland.nl niet verplicht

  - Als een bronhouder het aanlevert, neem dan de richtlijnen in acht in
    het NDE Application Profile

  - <https://docs.nde.nl/schema-profile/#CreativeWork-name>

- **Schema:publisher**

  - Uitgever van de dataset in het NDE dataset register

  - *CN-extensie*

  - URI naar schema:Organization.

  - Haalt CollectieNederland.nl op vanuit het NDE Dataset Register.

- **schema:isPartOf**

  - Dataset of (deel)collectie waartoe het werk behoort

  - Niet verplicht gesteld door CollectieNederland.nl, wel aanbevolen

  - <https://docs.nde.nl/schema-profile/#CreativeWork-isPartOf>

- **schema:license**

  - Rechtenstatement van het werk zelf (URI)

  - CollectieNederland.nl-extensie op CreativeWork-niveau. NDE
    Application Profile schrijft dit alleen op MediaObject voor.

  - <https://docs.nde.nl/schema-profile/#MediaObject-license>

- **Schema:temporal**

  - Ongestructureerde datering als vrije tekst (bijv. 'ca. 1650')

  - CollectieNederland.nl-extensie.

  - Wordt niet gebruikt door het NDE applicatieprofiel

- **Schema:conditionsOfAcces**s

  - Actuele juridische status voor Rijksmusea vanuit de Erfgoedwet

  - CollectieNederland.nl-extensie voor Rijksmusea.

  - Wordt niet gebruikt door het NDE applicatieprofiel

- **Schema:DefinedTerm -\> schema:sameAs**

  - Thesaurus term

  - NDE Application Profile gebruikt **schema:url.**
    CollectieNederland.nl geeft de voorkeur aan **schema:sameAs.**

  - <https://docs.nde.nl/schema-profile/#reference-terms>

## Thesauri-gebruik

Wanneer er gebruikt gemaakt wordt van thesaurus termen dan worden de
volgende thesauri aangenomen, afhankelijk van metadata veld: CHT,
RKDArtists, Geonames en AAT. Bekijk hier een omschrijving van thesaurustermen in het
NDE applicatieprofiel:
<https://docs.nde.nl/schema-profile/#reference-terms.>

