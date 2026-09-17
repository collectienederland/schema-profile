# CONCEPT Applicatieprofiel voor CollectieNederland.nl

# Inhoudsopgave

- [Applicatieprofiel voor CollectieNederland.nl](#applicatieprofiel-voor-collectienederlandnl)
- [1.1 Inleiding](#11-inleiding)
  - [Definities](#definities)
- [1.2 Velden voor CollectieNederland.nl](#12-velden-voor-collectienederlandnl)
  - [1.2.1 Minimale velden](#121-minimale-velden)
  - [1.2.2 Overzichtstabel minimale velden](#122-overzichtstabel-minimale-velden)
  - [1.2.3 Aanbevolen en optionele velden](#123-aanbevolen-en-optionele-velden)
  - [1.2.4 Overzichtstabel aanbevolen en optionele velden](#124-overzichtstabel-aanbevolen-en-optionele-velden)
  - [1.2.5 Afwijkingen ten opzichte van het NDE applicatieprofiel](#125-afwijkingen-ten-opzichte-van-het-nde-applicatieprofiel)
  - [1.2.6 Thesauri-gebruik](#126-thesauri-gebruik)
- [1.3 CollectieNederland.nl applicatieprofiel](#13-collectienederlandnl-applicatieprofiel)
  - [1.3.1 Schema:CreativeWork](#131-schemacreativework)
    - [1.3.1.1 schema:name (keuzeveld 1)](#1311-schemaname-keuzeveld-1)
    - [1.3.1.2 schema:alternateName](#1312-schemaalternatename)
    - [1.3.1.3 Schema:creditText](#1313-schemacredittext)
    - [1.3.1.4 schema:publisher](#1314-schemapublisher)
    - [1.3.1.5 schema:datePublished](#1315-schemadatepublished)
    - [1.3.1.6 Schema:citation](#1316-schemacitation)
    - [1.3.1.7 schema:dateCreated (keuzeveld 2)](#1317-schemadatecreated-keuzeveld-2)
    - [1.3.1.8 schema:temporal](#1318-schematemporal)
    - [1.3.1.9 schema:licence (verplicht)](#1319-schemalicence-verplicht)
    - [1.3.1.10 schema:description (keuzeveld 3)](#13110-schemadescription-keuzeveld-3)
    - [1.3.1.11 schema:size (keuzeveld 3)](#13111-schemasize-keuzeveld-3)
    - [1.3.1.12 schema:url (verplicht)](#13112-schemaurl-verplicht)
    - [1.3.1.13 schema:isPartOf (>Dataset of >CreativeWork)](#13113-schemaispartof-dataset-of-creativework)
    - [1.3.1.14 Schema:sdDatePublished](#13114-schemasddatepublished)
    - [1.3.1.15 schema:additionalType (Keuzeveld 1)](#13115-schemaadditionaltype-keuzeveld-1)
    - [1.3.1.16 Schema:material (keuzeveld 3)](#13116-schemamaterial-keuzeveld-3)
    - [1.3.1.17 schema:genre](#13117-schemagenre)
    - [1.3.1.18 schema:about](#13118-schemaabout)
    - [1.3.1.19 schema:identifier](#13119-schemaidentifier)
    - [1.3.1.20 schema:creator](#13120-schemacreator)
    - [1.3.1.21 schema:locationCreated (keuzeveld 3)](#13121-schemalocationcreated-keuzeveld-3)
    - [1.3.1.22 Schema:associatedMedia](#13122-schemaassociatedmedia)
  - [1.3.2 Schema:MediaObject](#132-schemamediaobject)
    - [1.3.2.1 schema:contentUrl](#1321-schemacontenturl)
    - [1.3.2.2 schema:license (verplicht)](#1322-schemalicense-verplicht)
    - [1.3.2.3 schema:thumbnailUrl (verplicht)](#1323-schemathumbnailurl-verplicht)
    - [1.3.2.4 schema:copyrightHolder](#1324-schemacopyrightholder)
    - [1.3.2.5 Schema:encodingFormat](#1325-schemaencodingformat)
    - [1.3.2.6 schema:copyrightNotice](#1326-schemacopyrightnotice)
  - [1.3.3 Schema:Person](#133-schemaperson)
    - [1.3.3.1 schema:name](#1331-schemaname)
    - [1.3.3.2 Schema:sameAs](#1332-schemasameas)
    - [1.3.3.3 Schema:hasOccupation](#1333-schemahasoccupation)
    - [1.3.3.4 Schema:birthDate](#1334-schemabirthdate)
    - [1.3.3.5 Schema:BirthPlace](#1335-schemabirthplace)
    - [1.3.3.6 Schema:deathDate](#1336-schemadeathdate)
    - [1.3.3.7 Schema:Deathplace](#1337-schemadeathplace)
  - [1.3.4 schema:geoCoordinates](#134-schemageocoordinates)
    - [1.3.4.1 schema:latitude](#1341-schemalatitude)
    - [1.3.4.2 schema:longitude](#1342-schemalongitude)
  - [1.3.5 schema:administrativeArea](#135-schemaadministrativearea)
    - [1.3.5.1 Schema:name](#1351-schemaname)
    - [1.3.5.2 Schema:sameAs](#1352-schemasameas)
  - [1.3.6 schema:PropertyValue](#136-schemapropertyvalue)
    - [1.3.6.1 schema:conditionsOfAccess (verplicht voor Rijksmusea)](#1361-schemaconditionsofaccess-verplicht-voor-rijksmusea)
    - [1.3.6.2 schema:propertyID](#1362-schemapropertyid)
    - [1.3.6.3 schema:value](#1363-schemavalue)
    - [1.3.6.4 schema:description](#1364-schemadescription)
  - [1.3.7 schema:Place](#137-schemaplace)
    - [1.3.7.1 Schema:adressRegion](#1371-schemaadressregion)
    - [1.3.7.2 Schema:name](#1372-schemaname)
    - [1.3.7.3 Schema:sameAs](#1373-schemasameas)
  - [1.3.8 schema:Occupation, schema:DefinedTerm](#138-schemaoccupation-schemadefinedterm)
    - [1.3.8.1 Schema:name](#1381-schemaname)
    - [1.3.8.2 Schema:sameAs](#1382-schemasameas)
  - [1.3.9 schema:DefinedTerm](#139-schemadefinedterm)
    - [1.3.9.1 Schema:name](#1391-schemaname)
    - [1.3.9.2 Schema:sameAs](#1392-schemasameas)
  - [1.3.10 schema:Product](#1310-schemaproduct)
    - [1.3.10.1 Schema:name](#13101-schemaname)
    - [1.3.10.2 Schema:sameAs](#13102-schemasameas)
  - [1.3.11 schema:Text, schema:DefinedTerm](#1311-schematext-schemadefinedterm)
    - [1.3.11.1 Schema:name](#13111-schemaname)
    - [1.3.11.2 Schema:sameAs](#13112-schemasameas)

# 1.1 Inleiding

In deze documentatie wordt het applicatieprofiel beschreven voor
CollectieNederland.nl. Dit profiel is gebaseerd op het [<u>nieuwe
datamodel voor
Collectienederland.nl</u>](https://github.com/collectienederland/schema-profile),
wat Schema.org gebruikt als beschrijvende vocabulaire. Dit model is weer
een uitbreiding op het [<u>Schema.org Application Profile for
NDE</u>](https://docs.nde.nl/schema-profile/) en volgt dit
applicatieprofiel grotendeels. Dit document vormt de basis voor de
publicatievoorwaarden van CollectieNederland.nl

Op enkele punten wijken het applicatieprofiel voor CollectieNederland.nl
af van het NDE Application Profile. Het gaat hier altijd om
versoepelingen en aanvullingen ten op zichten van het NDE
Applicatieprofiel, nooit om striktere eisen. Deze punten zijn terug te
vinden onder kopje 1.2.5.

De velden die minimaal nodig zijn om data aan te leveren aan
CollectieNederland.nl staan genoteerd onder kopje 1.2. De thesauri die
CollectieNederland.nl aanhoudt zijn terug te vinden onder sectie 1.5.

### Definities

**Kadinaliteit**: hoe vaak een waarde mag voorkomen in een veld.
Hierbinnen geeft dit document ook de specifieke datatypes aan (bijv. URI
of Date) of de Thesauri die toegestaan zijn.

- 0..\* de waarde mag nul, één of meerdere keren voorkomen

- 1..\* de waarde moet minimaal 1 keer voorkomen en mag meerdere malen
  voorkomen

- 0..1 de waarde mag 0 of 1 keer voorkomen

- 1..1 de waarde moet één keer voorkomen

**Classes**: Een type entiteit in schema.org (bijv. Place of
CreativeWork). Deze worden gebruikt om te bepalen welke entiteiten
toegestaan zijn in het applicatieprofiel.

**Properties**: de kenmerken die binnen een Class vallen (bijv.
schema:name en schema:description). ). Deze worden gebruikt om te
bepalen welke entiteiten toegestaan zijn in het applicatieprofiel.

**Verplichtingsniveau:**

- **Verplicht** : de waarden die altijd moeten worden aangeleverd
  (schema:license)

- **Optioneel:** de waarden die mogen worden aangeleverd
  (schema:material)

- **Aanbevolen**: de waarden waarvan sterk wordt aangeraden dat ze
  worden aangeleverd

# 1.2 Velden voor CollectieNederland.nl

## 1.2.1 Minimale velden

Bij het aanleveren van collectiedata aan CollectieNederland.nl wordt
gekeken naar of de volgende minimale velden aanwezig zijn in de data en
of de inhoud van deze velden in lijn is met het Schema.org Application
Profile for NDE en het aanvullende CollectieNederland.nl: Schema
Profile. Als er voor een veld een afwijking of versoepeling geldt, dan
is deze leidend ten opzichte van het NDE Application Profile. Bij
overlap tussen de twee profielen verwijst dit document door naar het NDE
Application Profile.

## 1.2.2 Overzichtstabel minimale velden

In de onderstaande tabel staat een overzicht van de verplichte velden
voor publicatie van een dataset op CollectieNederland.nl. Er zijn een
aantal keuzevelden opgenomen. Voor deze velden geldt:

\- Keuzeveld 1: er moet ten minste één veld aanwezig zijn wat kan
functioneren als titel.

\- Keuzeveld 2: er moet ten minste één veld aanwezig zijn wat kan
functioneren als datering.

\- Keuzeveld 3: er moet ten minste één veld aanwezig zijn wat iets
beschrijft van het werk (CreativeWork).

| *Entiteit* | *Veld* | *Betekenis* | *Verplicht* | *Type* |  |
|----|----|----|----|----|----|
| CreativeWork | schema:license | Rechtenstatement van het werk zelf | <span class="mark">Ja</span> | URI |  |
| MediaObject | Schema:licence | Rechtenstatement afbeelding | Ja, bij contentUrl | URI |  |
| CreativeWork | schema:copyrightNotice | Actuele juridische status | Ja, voor Rijksmusea\* | URI |  |
| CreativeWork | Schema:isPartOf\>schema:Dataset | Beschrijft van welke dataset het werk deel uitmaakt | Ja | URI |  |
| CreativeWork | schema:url | Link van het object op de website van de bronhouder | <span class="mark">Ja</span> | URI |  |
| CreativeWork | schema:sdDatePublished | Datum van publicatie metadata | Ja | date |  |
| CreativeWork | schema:name | Titel | Keuzeveld 1 | String |  |
| CreativeWork | schema:additionalType | Objecttype | Keuzeveld 1 | String of URI |  |
| CreativeWork | schema:temporal | Periode van vervaardiging | Keuzeveld 2 | String |  |
| CreativeWork | schema:dateCreated | Vervaardigingsdatum | Keuzeveld 2 | Date |  |
| CreativeWork | schema:description | Beschrijving van het werk | Keuzeveld 3 | String |  |
|  |  |  |  |  |  |
| CreativeWork | schema:material | Materiaal | Keuzeveld 3 | String/URI |  |
| CreativeWork | schema:size | Afmetingen | Keuzeveld 3 | String/QuantitativeValue |  |
| CreativeWork | schema:locationCreated | Plaats van productie of vervaardiging | Keuzeveld 3 | String/URI |  |

\*Verplicht voor de Rijksmusea volgens de Erfgoedwet.

## 1.2.3 Aanbevolen en optionele velden

In de onderstaande tabel staat een overzicht van de velden die worden
aanbevolen of optioneel zijn om toe te voegen. In sectie 1.3 worden de
velden toegelicht. In sommige gevallen is het zo dat als een optioneel
veld wordt aangeleverd, er een verplicht veld bijkomt – dat aan het
optionele veld verbonden is. Mocht dit zo zijn dan staat dit per veld
aangegeven in de kolom optioneel/aanbevolen.

## 1.2.4 Overzichtstabel aanbevolen en optionele velden

| **Entiteit** | **Veld** | **Inhoud van het veld** | **Verplicht** | **Type** | **NDE-profiel** |
|----|----|----|----|----|----|
| Schema:CreativeWork | schema:alternateName | alternatieve titel van het object | Optioneel | String | Nee, uitbreiding CNNL |
| Schema:CreativeWork | schema:creditText | geassocieerde persoon of organisatie | Optioneel | String/URI | Nee, uitbreiding CNNL |
| Schema:CreativeWork | schema:publisher | Uitgever object | Optioneel | String | Nee, uitbreiding CNNL |
| Schema:CreativeWork | schema:datePublished | datum van uitgeven | Optioneel | Date | Nee, uitbreiding CNNL |
| Schema:CreativeWork | schema:citation | Referentie naar uitgave of bron | Optioneel | String | Nee, uitbreiding CNNL |
| Schema:CreativeWork | schema:temporal | Tijdsaanduiding in platte tekst | Optioneel | String | Nee, uitbreiding CNNL |
| Schema:CreativeWork | schema:isPartOf/hasPart \>CreativeWork | Deelcollectie | Aanbevolen | URI | Nee, uitbreiding CNNL |
| Schema:CreativeWork | schema:genre | Onderwerp | Aanbevolen | String/URI | Ja |
| Schema:CreativeWork | schema:about | Geassocieerde persoon of concept | Aanbevolen | String/URI | Ja |
| Schema:CreativeWork | schema:identifier | Objectnummer | Aanbevolen | String/URI | Ja, CNNL is hier soepeler |
| Schema:CreativeWork | schema:creator | Vervaardiger | Aanbevolen | String/URI | Ja |
| Schema:MediaObject | schema:contentURL | Afbeelding | Aanbevolen | URI | Ja, CNNL is hier soepeler |
| Schema:MediaObject | schema:license | Rechtenstatement afbeelding | Ja, bij schema:contentURL | URI | Ja |
| Schema:MediaObject | schema:thumbnailUrl | Verkleinde afbeelding | Ja, bij schema:contentURL | URI | Ja |
| Schema:Person | schema:name | Vervaardiger persoon of organisatie | Aanbevolen | String/URI | Ja |
| Schema:Person | schema:hasOccupation | Rol van de vervaardiger | Aanbevolen | String/URI | Ja |
| Schema:Person | schema:birthDate | Geboortedatum vervaardiger | Optioneel | Date | Ja |
| Schema:Person | schema:BirthPlace | Geboorteplaats vervaardiger | Optioneel | String/URI | Ja |
| Schema:Person | schema:deathDate | Sterfdatum vervaardiger | Optioneel | Date | Ja |
| Schema:Person | schema: deathPlace | Sterfplaats vervaardiger | Optioneel | String/URI | Ja |
| Schema:Place | schema:latitude | Breedtegraad | Optioneel | Tekst | Ja |
| Schema:Place | schema:longitude | Lengtegraad | Optioneel | Tekst | Ja |
| Schema:Place | schema:adressRegion | Provincie | Optioneel | String/URI | Ja |
| <span class="mark">Schema:MediaObject</span> | <span class="mark">schema:encodingFormat</span> | Type media | <span class="mark">Optioneel</span> | <span class="mark">String/URI</span> | <span class="mark">Nee</span> |

## 1.2.5 Afwijkingen ten opzichte van het NDE applicatieprofiel

In de onderstaande tabellen zijn de verschillen terug te vinden tussen
het CollectieNederland.nl applicatieprofiel en het
NDE-applicatieprofiel. Het gaat hier in de eerste tabel om verschillen
in de aanwezigheid van Classes en Properties. In de tweede tabel worden
de verschillen aangegeven in Classes en Properties die zowel het NDE als
CNNL 2.0 kennen, maar waarbij CollectieNederland.nl een ander
verplichtingsniveau hanteert (bijv. Optioneel i.p.v. Verplicht) of een
andere invulling geeft.

<table>
<colgroup>
<col style="width: 41%" />
<col style="width: 11%" />
<col style="width: 23%" />
<col style="width: 23%" />
</colgroup>
<thead>
<tr>
<th colspan="4"><strong>CollectieNederland.nl ten opzichte van NDE —
toevoegingen</strong> <strong>in Classes en Properties</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Property/Class</strong></td>
<td><strong>In NDE profiel</strong></td>
<td><strong>In CN.NL 2.0 Datamodel en applicatieprofiel</strong></td>
<td><strong>Uitleg op toevoeging</strong></td>
</tr>
<tr>
<td>CreativeWork&gt;schema:publisher</td>
<td>Nee</td>
<td>Ja — optioneel</td>
<td>Publisher van een boek. Publisher, ofwel, bronhouder komt mee vanuit
de datasetbeschrijving van de dataset in het dataset register.</td>
</tr>
<tr>
<td>CreativeWork&gt;schema:temporal</td>
<td>Nee</td>
<td>Ja — optioneel</td>
<td>Vrije-tekst datering (bijv. “ca. 1650”) als aanvulling op
schema:dateCreated, voor onzekere of ongestructureerde dateringen.</td>
</tr>
<tr>
<td>MediaObject&gt;schema:copyrightNotice</td>
<td>Nee</td>
<td>Ja — verplicht (alleen Rijksmusea)</td>
<td>Toevoeging voor de Erfgoedwet-verplichtingen van Rijksmusea.</td>
</tr>
<tr>
<td>Place&gt;schema:addressRegion</td>
<td>Nee</td>
<td>Ja — optioneel</td>
<td>Coördinaten en provincie/regio, voor kaartweergave en filtering op
CNNL.</td>
</tr>
<tr>
<td>CreativeWork&gt;schema:isPartOf (hasPart)&gt;CreativeWork</td>
<td>Nee</td>
<td>Ja - optioneel</td>
<td>Relatie voor het aangeven van een deelcollectie binnen een
dataset.</td>
</tr>
<tr>
<td>CreativeWork&gt;schema:alternateName</td>
<td>Nee</td>
<td>Ja — optioneel</td>
<td>Alternatieve naam/titel van werk of maker.<mark></mark></td>
</tr>
<tr>
<td>CreativeWork&gt;schema:creditText</td>
<td>Nee</td>
<td>Ja — optioneel</td>
<td>Generieke attributie-/credittekst. Let op: voor het specifieke geval
van eigendomsgeschiedenis is dit veld juist afgeraden (te weinig
gestructureerd) — hier gaat het om een breder, algemeen gebruik.</td>
</tr>
<tr>
<td>CreativeWork&gt;schema:citation</td>
<td>Nee</td>
<td>Ja — optioneel</td>
<td>Verwijzing naar publicaties of bronnen waarin het werk wordt
beschreven.</td>
</tr>
<tr>
<td>CreativeWork&gt;schema:datePublished</td>
<td>Nee</td>
<td>Ja — optioneel</td>
<td><mark>Datum van publicatie, bijvoorbeeld van een boek.</mark></td>
</tr>
<tr>
<td><p>MediaObject-subklassen
(ImageObject/VideoObject/AudioObject/3DModel)</p>
<p>Of</p>
<p>MediaObject&gt;schema:encodingFormat</p></td>
<td>Ja — verplicht</td>
<td>Ja — sinds v2.2 (juli 2026)</td>
<td>Was een gat in het CN-model (alleen generiek MediaObject); sinds
v2.2 toegevoegd conform NDE. Geen verschil meer.</td>
</tr>
<tr>
<td>  CreativeWork&gt;schema:isPartOf
(hasPart)&gt;schema:CreativeWork</td>
<td>Nee</td>
<td>Ja – optioneel <mark>(besproken met Jonathan</mark></td>
<td>Veld voor deelcollecties die samen in één dataset zitten.</td>
</tr>
<tr>
<td>schema:administrativeArea</td>
<td>Nee</td>
<td></td>
<td><mark>Nog bespreken: wel in het NDE-profiel:
schema:addressRegion</mark></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 24%" />
<col style="width: 16%" />
<col style="width: 58%" />
</colgroup>
<thead>
<tr>
<th colspan="3"><strong>CollectieNederland.nl ten opzichte van NDE —
afwijkend verplichtingsniveau</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Property</strong></td>
<td><strong>NDE</strong></td>
<td><strong>CN</strong></td>
</tr>
<tr>
<td>CreativeWork&gt;schema:creator</td>
<td>Verplicht als de maker bekend is.</td>
<td>Aanbevolen</td>
</tr>
<tr>
<td>schema:license (CreativeWork + MediaObject)</td>
<td>Verplicht op MediaObject.</td>
<td>sh:Info, niet blokkerend — ook zo op CreativeWork.</td>
</tr>
<tr>
<td>MediaObject&gt;schema:thumbnailUrl</td>
<td>Verplicht op MediaObject.</td>
<td>Aanbevolen</td>
</tr>
<tr>
<td>CreativeWork&gt;schema:associatedMedia / afbeelding</td>
<td>Verplicht indien beschikbaar.</td>
<td>Aanbevolen</td>
</tr>
<tr>
<td>CreativeWork&gt;schema:identifier / PID</td>
<td>PID verplicht.</td>
<td>Aanbevolen</td>
</tr>
<tr>
<td>CreativeWork&gt;schema:name</td>
<td>Verplicht op CreativeWork</td>
<td>Aanbevolen. CollectieNederland.nl vraagt schema:name of
schema:additionalType, zie sectie 1.2.2.</td>
</tr>
</tbody>
</table>

## 1.2.6 Thesauri-gebruik

Wanneer er gebruikt gemaakt wordt van thesaurustermen dan worden de
volgende thesauri aangenomen, afhankelijk van metadata veld: CHT,
RKDArtists, Geonames en AAT. Bekijk hier een omschrijving van
thesaurustermen in het NDE
applicatieprofiel: [<u>https://docs.nde.nl/schema-profile/#reference-terms.</u>](https://docs.nde.nl/schema-profile/#reference-terms.)

# 1.3 CollectieNederland.nl applicatieprofiel

Afwijkingen van het NDE applicatieprofiel zijn gemarkeerd door middel
van een asterisk (\*) en zijn met uitleg terug te vinden in de
bovenstaande sectie 1.2.5.

## 1.3.1 Schema:CreativeWork

De centrale klasse in het CollectieNederland.nl-applicatieprofiel. Met
deze klasse worden cultuurhistorische objecten omschreven in dit
profiel.

### 1.3.1.1 schema:name (keuzeveld 1)

- Beschrijving: titel van het object

- Voorbeeld: De nachtwacht

- Verplicht: verplicht keuzeveld 1

- Technische verwijzing

  - Formaat: string

  - Kardinaliteit: 0..1

  - [<u>https://docs.nde.nl/schema-profile/#CreativeWork-name</u>](https://docs.nde.nl/schema-profile/).

### 1.3.1.2 schema:alternateName \*

- Beschrijving: alternatieve titel van het object

- Voorbeeld:

  - De scheeuw

  - Skrik

- Verplicht: optioneel

- Technische verwijzing

  - Formaat: string

  - Kardinaliteit: 0..1

  - <https://schema.org/alternateName>

    - Uitbreiding NDE-applicatieprofiel om musea de mogelijkheid te
      geven om objecten meerdere titels mee te geven zoals toegekende
      titel of originele titel.

### 1.3.1.3 Schema:creditText\*

- Beschrijving: geassocieerde persoon of organisatie die is gerelateerd
  aan het object.

- Voorbeeld:

  - name: Otto Frank

  - sameAs: <http://data.beeldengeluid.nl/gtaa/99929>

- Verplicht: optioneel

- Technische verwijzing:

  - Formaat: string

  - Kardinaliteit: 0..1

  - <https://schema.org/creditText>

    - Uitbreiding NDE-applicatieprofiel voor generieke
      attributie-/credittekst. Let op: voor het specifieke geval
      eigendomsgeschiedenis is dit veld juist afgeraden (te weinig
      gestructureerd) — hier gaat het om een breder, algemeen gebruik.

### 1.3.1.4 schema:publisher \*

- Beschrijving: uitgever van een boek, tijdschrift of artikel.

- Voorbeeld: Uitgeverij Noordzon

- Verplicht: optioneel

- Technisch:

  - Formaat: string

  - Kardinaliteit: 0.. 1

  - <https://schema.org/publisher>

    - Uitbreiding op het NDE-applicatieprofiel voor museumcollecties die
      ook boeken, artikelen of andere objecten hebben in de
      museumcollectie.

### 1.3.1.5 schema:datePublished\*

- Beschrijving: datum waarop het object is uitgegeven door de uitgever.

- Voorbeeld: 2010-11-02

- Verplicht: optioneel

- Technisch:

  - Formaat: date, conform ISO-8601

  - Kandinaliteit: 0..1

  <!-- -->

  - <https://schema.org/datePublished>

    - Uitbreiding op het NDE-applicatieprofiel voor museumcollecties die
      ook boeken, artikelen of andere objecten hebben in de
      museumcollectie.

### 1.3.1.6 Schema:citation\*

- Beschrijving: referentie naar een publicatie of boek.

- Voorbeeld: van den Boorn, G.P.F. and Van Es, M.J. (1989), Recent
  Acquisitions: II. The Near East. OMROL 69, blz. 13

- Verplicht: optioneel

- Technisch:

  - Formaat: string

  - Kardinaliteit: 0.. \*

  - <https://schema.org/citation>

    - Uitbreiding op het NDE-applicatieprofiel voor verwijzingen naar
      publicaties of boeken die aan een object gerelateerd zijn.

### 1.3.1.7 schema:dateCreated (keuzeveld 2)

- Beschrijving: vervaardigingsdatum van het object.

- Bijvoorbeeld

  - 1955-06-21

  - 1658-05

  - 1658

- Verplicht: verplicht keuzeveld 2

- Technische

  - Formaat: date, conform ISO-8601

  - Kandinaliteit: 0..1

  - <https://docs.nde.nl/schema-profile/#CreativeWork-dateCreated>

### 1.3.1.8 schema:temporal \*

- Beschrijving: onzekerheidsaanduiding datering als vrije tekst

- Bijvoorbeeld:

  - Ca.

  - Circa

  - Ongeveer

- Verplicht: optioneel

- Technisch:

  - Formaat: string

  - Kardinaliteit: 0..\*

  - <https://schema.org/temporal>

    - Toevoeging op het NDE-applicateiprofiel, vanwege collecties die
      geen datering hebben, maar uit een bepaalde periode komen zoals
      archeologische opgraven.

### 1.3.1.9 <span class="mark">schema:licence (verplicht)\*</span>

- Beschrijving: rechtenstatement van het object zelf (URI). Uitsluitend
  rechtenstatements van Rightstatements.org.

- Voorbeeld: http://rightsstatements.org/vocab/InC/1.0/

- Verplicht: ja

- Technisch:

  - Formaat: URL volgens Rightstatements.org

  - Kardinaliteit: 1..1

  - <https://schema.org/license>

    - <span class="mark">NDE heeft alleen een licentie als verplicht bij
      MediaObject. CN-extensie op CreativeWork-niveau.</span>

    - <span class="mark">In conflict met wat Maarten vertelde over
      rechten</span>

  - Let op: Als er een afbeelding (**schema:MediaObject**) aanwezig is,
    zijn de volgende velden verplicht: **schema.contenUrl,
    schema:licence**.

### 1.3.1.10 schema:description (keuzeveld 3)

- Beschrijving: beschrijving van het object.

- Voorbeeld: Schilderij van een ridderzaal met een tafel met buffet. Aan
  beide zijde van de tafel een ridder in harnas.

- Verplicht: verplicht keuzeveld 3.

- Technisch:

  - Formaat: string

  - Kardinaliteit: 0..1

  - <https://docs.nde.nl/schema-profile/#CreativeWork-description>.

### 1.3.1.11 schema:size (keuzeveld 3)

- Beschrijving: afmeting van het object in hoogte x breedte x diepte in
  cm als een waarde.

- Voorbeeld: 24,5 × 20,5 x 4 cm

- Verplicht: verplicht keuzeveld 3

- Technisch:

  - Formaat: string

  - Kardinaliteit: 0..1

  - [<u>https://docs.nde.nl/schema-profile/#CreativeWork-size</u>](https://docs.nde.nl/schema-profile/)

### 1.3.1.12 schema:url (verplicht)

- Beschrijving: link naar het object bij de website van de bronhouder.

- Voorbeeld:

  - [*http://hdl.handle.net/10934/RM0001.COLLECT.250239*](http://hdl.handle.net/10934/RM0001.COLLECT.250239)

  - <https://muiderslot.adlibhosting.com/details/museum/10000349>

- Verplicht: ja

- Technisch:

  - Formaat: URL

    - Valide URL

    - Bij voorkeur een PID

  - Kardinaliteit: 1..1

  - <https://docs.nde.nl/schema-profile/#CreativeWork-URI>

### 1.3.1.13 schema:isPartOf (\>Dataset of \>CreativeWork)

- Beschrijving: Dataset of deelcollectie waartoe het object behoort

- Voorbeeld: Rijksmuseum of NK-collectie

- Verplicht: Verplicht in het geval van de Dataset, aanbevolen voor een
  deelcollectie

- Technisch:

  - Formaat: Dataset (URI) or CreativeWork (URI)

  - Kardinaliteit: 1..\* en 0..\*

  - <https://docs.nde.nl/schema-profile/#CreativeWork-isPartOf>

### 1.3.1.14 Schema:sdDatePublished

- Beschrijving: de datum waarop de metadata is gepubliceerd

- Voorbeeld: 2026-01-30

- Verplicht: ja

- Technisch:

  - Format: date, conform ISO-8601

  - Kardinaliteit: 1..1

  - <https://docs.nde.nl/schema-profile/#CreativeWork-sdDatePublished>

### 1.3.1.15 schema:additionalType (Keuzeveld 1)

- Beschrijving: objecttype

- Voorbeeld:

  - tekening

  - sameAs:
    <https://data.cultureelerfgoed.nl/term/id/cht/eb9e1e5b-b319-4519-a4f5-0dd26dbf4524>

- Verplicht: verplicht keuzeveld 1

- Technische verwijzing

  - Formaat: term en/of URI

  - Thesauri: de CHT of AAT

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#CreativeWork-additionalType>

### 1.3.1.16 Schema:material (keuzeveld 3)

- Beschrijving: materiaal waaruit het object bestaat

- Voorbeeld:

  - metalen

  - sameAs:
    <https://data.cultureelerfgoed.nl/term/id/cht/b9fd0887-297b-4bab-bea5-cb288d068816>

- Verplicht: verplicht keuzeveld 3

- Technisch:

  - Formaat: term

  - Aanbevolen thesauri: CHT of AAT

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#CreativeWork-material>

### 1.3.1.17 schema:genre 

- Beschrijving: onderwerp van het afgebeelde op het object

- Voorbeeld:

  - bevrijding

  - sameAs:
    <https://data.cultureelerfgoed.nl/term/id/cht/ac43187b-02fa-45ab-b1d6-86a02860db1f>

- Verplicht: aanbevolen

- Technisch:

  - Formaat: term

  - Aanbevolen thesauri: CHT of AAT

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#CreativeWork-genre>

### 1.3.1.18 schema:about 

- Beschrijving: geassocieerde persoon of concept

- Voorbeeld:

  - Frank, Anne (1929-1945)

  - sameAs: <http://data.bibliotheken.nl/id/thes/p107412225>

- Verplicht: aanbevolen

- Technisch:

  - Formaat: term

    - Aanbevolen thesauri: CHT of AAT

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#CreativeWork-about>

### 1.3.1.19 schema:identifier 

- Beschrijving: identificatienummer of objectnummer.

  - Bij voorkeur een PID

- Bijvoorbeeld:

  - MA-2017-0054

  - Value: "http://identifiers.org/viaf:176354386

  - PropertyID:
    [*http://hdl.handle.net/10934/RM0001.COLLECT.250239*](http://hdl.handle.net/10934/RM0001.COLLECT.250239)

- Verplicht: aanbevolen

- Technisch:

  - Formaat: string

  - Kardinaliteit: 0..1

  - <https://docs.nde.nl/schema-profile/#CreativeWork-identifier>

    - Versoepeling, waardoor bronhouders een PID, URL of objectnummer
      kunnen aanleveren. Nog niet alle bronhouders hebben de financiële
      middelen om een PID module te implementeren.

### 1.3.1.20 schema:creator 

- Beschrijving: vervaardiger van het object

- Bijvoorbeeld:

  - Gogh, van Vincent

  - <https://data.rkd.nl/artists/351830>

- Verplicht: aanbevolen

- Technisch:

  - Formaat: term

  - Aanbevolen thesauri: RKD artist

  - Kandinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#CreativeWork-creator>

    - Versoepeling van het NDE-applicatieprofiel, vanwege collecties
      waarbij geen vervaardiger bekend is, zoals archeologische
      collecties.

### 1.3.1.21 schema:locationCreated (keuzeveld 3)

- Beschrijving: plaats van vervaardiging of productie.

- Voorbeeld:

  - Alkmaar

  - sameAs: <https://sws.geonames.org/2759899/>

- Verplicht: Aanbevolen

- Technisch:

  - Formaat: term

  - Aanbevolen thesauri: GeoNames

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#CreativeWork-locationCreated>

### 1.3.1.22 Schema:associatedMedia

- Beschrijving: Afbeeldingen (MediaObjects) die het CreativeWork
  representeren.

- Voorbeeld:
  <https://medialib.naturalis.nl/file/id/RMNH.ART.730/format/large>

- Verplicht: aanbevolen, let op: schema:licence is verplicht bij dit
  veld

- Technisch:

  - Format: URI

    - Valide URI.

    - Afbeelding, video, audio en/of 3D model

  - Kardinaltieit: 0..\*

  - <https://docs.nde.nl/schema-profile/#CreativeWork-associatedMedia>

<span class="mark">\
</span>1.3.2 Schema:MediaObject
-------------------------------

Afbeelding, video, audio en/of 3D model die het object of werk
representeert. Het aanleveren van afbeeldingen wordt sterk aanbevolen.

### 1.3.2.1 schema:contentUrl 

- Beschrijving: directe URI naar het mediabestand (afbeelding, video,
  audio en/of 3D model), verplicht als valide URI.

- Voorbeeld:
  <https://medialib.naturalis.nl/file/id/RMNH.ART.730/format/large>

- Verplicht: aanbevolen, let op: schema:licence en schema:thumbnailUrl
  zijn verplicht bij schema:contentUrl

- Technisch:

  - Format: URI

    - Valide URI.

    - Afbeelding, video, audio en/of 3D model

  - Kardinaltieit: 0..\*

  - <https://docs.nde.nl/schema-profile/#MediaObject-contentUrl>

### 1.3.2.2 schema:license (verplicht)

- Beschrijving: rechtenstatement van de afbeelding van
  rightsstatements.org

- Voorbeeld: <http://rightsstatements.org/vocab/InC/1.0/>

- Verplicht: ja, bij schema:contentUrl

- Technisch:

  - Format: URI van rechtenstatements.org

  - Kardinaliteit: 1..1

  - <https://docs.nde.nl/schema-profile/#MediaObject-license>

### 1.3.2.3 schema:thumbnailUrl (verplicht)

- Beschrijving: verkleind formaat van de afbeelding

- Voorbeeld:
  <https://collectie.wereldmuseum.nl/cc/imageproxy.ashx?filename=images/Images/TM//tm-30057342.jpg>

- Verplicht: ja, bij schema:contentUrl

- Technisch:

  - Format: URI

  - Kardinaliteit: 1..1

  - <https://docs.nde.nl/schema-profile/#MediaObject-thumbnailUrl>

### 1.3.2.4 schema:copyrightHolder\*

- Beschrijving: rechthebbende van de afbeelding.

- Voorbeeld: Collectie Centraal Museum Utrecht / foto Adriaan van Dam* *

- Voorbeeld URI: <https://rkd.nl/artists/527987>

- Verplicht: optioneel

- Technisch:

  - Format: string

  - SameAs: URI

  - Kardinaliteit: 0..\*

  - <https://schema.org/copyrightHolder>

###  Schema:encodingFormat\*

- Beschrijving: type media van MediaObject

- Voorbeeld: image/png* *

- Verplicht: optioneel

- Technisch:

  - Format: string

  - Kardinaliteit: 0..\*

  - <https://schema.org/encodingFormat>

###  schema:copyrightNotice

- Beschrijving: Rechtenstatement vanuit brondata

- Voorbeeld: *©* 2025 Collectie Museum Amsterdam, met toestemming van
  Foto graaf

- Verplicht: optioneel

- Technisch:

  - Format: string

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#MediaObject-copyrightNotice>

## 1.3.3 Schema:Person

### 1.3.3.1 schema:name

- Beschrijving: naam van vervaardiger als persoon of organisatie

- Voorbeeld:

  - name: Gogh, van V.

  - name: Gazelle b.v.

- Verplicht: aanbevolen

- Technisch:

  - Format: string

  - Kardinaliteit 0..1

  - <https://docs.nde.nl/schema-profile/#Person-name>

    - Afwijking van het NDE-applicatieprofiel. De meeste
      collectieinformatiesystemen registeren vervaardigers in hetzelfde
      veld, maar geven een extra waarde mee als rol van de vervaardiger.

    - Als er een persoon of organisatie
      (**schema:Person** en **schema:Organisation**) aanwezig is en
      geregistreerd in verschillende velden, zijn de volgende velden
      verplicht:

      - <https://docs.nde.nl/schema-profile/#Person-name>

      - <https://docs.nde.nl/schema-profile/#Organization-name>

### Schema:sameAs

- Beschrijving: relatie naar een thesaurusterm

- Voorbeeld: <https://data.rkd.nl/artists/351830>

- Aanbevolen thesauri: RKD artist, CHT, AAT, Geonames

- Verplicht: aanbevolen

- Technisch

  - Type: DefinedTerm

  - Format: URI

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#reference-terms>

### 1.3.3.3 Schema:hasOccupation

- Beschrijving: rol van de vervaardiger

- Voorbeeld:

  - ontwerper

  - sameAs:
    https://data.cultureelerfgoed.nl/term/id/cht/e8f8e3d0-761f-4dda-b846-64f860cdc670

- Verplicht: aanbevolen

- Technisch:

  - Format: URI

  - Aanbevolen thesauri: CHT of AAT

  - Kardinaliteit 0.. \*

  - <https://docs.nde.nl/schema-profile/#Person-hasOccupation>

### 1.3.3.4 Schema:birthDate

- Beschrijving: geboortedatum van de vervaardiger

- Voorbeeld: 1890-03-20

- Verplicht: optioneel

- Technisch:

  - Format: date, conform ISO-8601

  - Kardinalietit: 0..1

  - <https://docs.nde.nl/schema-profile/#Person-birthDate>

### 1.3.3.5 Schema:BirthPlace

- Beschrijving: geboorteplaats van de vervaardiger

- Voorbeeld:

  - Leiden

  - sameAs: <https://www.geonames.org/2751773/leiden.html>

- Verplicht: optioneel

- Technisch:

  - Format: string and URI

  - Kardinaliteit: 0..1

  - <https://docs.nde.nl/schema-profile/#Person-birthPlace>

### 1.3.3.6 Schema:deathDate

- Beschrijving: sterfdatum van de vervaardiger

- Voorbeeld: 1945-03-02

- Verplicht: optioneel

- Technisch:

  - Format: Date conform ISO-8601

  - Kardinaliteit: 0..1

  - <https://docs.nde.nl/schema-profile/#Person-deathDate>

### 1.3.3.7 Schema:Deathplace 

- Beschrijving: sterfplaats van de vervaadiger

- Voorbeeld:

  - Leiden

  - sameAs: <https://www.geonames.org/2751773/leiden.html>

- Verplicht: optioneel

- Technisch:

  - Format: string and URI

  - Kardinaliteit: 0..1

  - <https://docs.nde.nl/schema-profile/#Person-deathPlace>

## 1.3.4 schema:geoCoordinates

Geografische coördinaten van een plek. Onderstaande properties zijn
verplicht als geoCoordinates aanwezig is.

### 1.3.4.1 schema:latitude

- Beschrijving: breedtegraad van de vindplaats of locatie van
  vervaardiging

- Voorbeeld: 52.379189

- Verplicht: verplicht als geoCoordinates aanwezig is.

- Technisch:

  - Format: string

  - Kardinaliteit: 1..1

  - <https://docs.nde.nl/schema-profile/#GeoCoordinates-latitude>

### 1.3.4.2 schema:longitude

- Beschrijving: lengtegraad van de vindplaats of vervaardiging

- Voorbeeld: 4.899431

- Verplicht: verplicht als geoCoordinates aanwezig is.

- Technisch:

  - Format: string

  - Kardinaliteit: 1..1

  - <https://docs.nde.nl/schema-profile/#GeoCoordinates-longitude>

## 1.3.5. schema:administrativeArea\*

De provincie waarin de plek zich bevindt.

<https://schema.org/AdministrativeArea>

### 1.3.5.1 Schema:name

- Beschrijving: naam van de plek

- Voorbeeld: Zuid-Holland

- Verplicht: verplicht als schema:administrativeArea aanwezig is

- Technisch:

  - Format: string

  - Kardinaliteit 1..1

  - <https://docs.nde.nl/schema-profile/#Place-name>

### 1.3.5.2 Schema:sameAs

- Beschrijving: relatie naar een thesaurusterm

- Voorbeeld:
  <https://www.geonames.org/2743698/provincie-zuid-holland.html>

- Aanbevolen thesauri: Geonames (voor schema:administrativeArea)

- Verplicht: aanbevolen

- Technisch

  - Type: DefinedTerm

  - Format: URI

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#reference-terms>

## 1.3.6 <span class="mark">schema:PropertyValue</span>

IDs, bijvoorbeeld PIDs of IDs uit het collectiebeheersysteem die voor
context belangrijk zijn, kunnen worden toegevoegd door middel van deze
PropertyValue klasse.

<https://schema.org/PropertyValue>

### 1.3.6.1 ~~schema:conditionsOfAccess (verplicht voor Rijksmusea)~~

- ~~Beschrijving: juridische status voor collecties bij Rijksmusea.~~

- ~~Voorbeeld:~~ ~~*<span class="mark">Waarde moet nog bepaald
  worden</span>*~~

- ~~Status: alleen verplicht voor Rijksmusea volgens de Erfgoedwet. Dit
  veld wordt niet getoond op CollectieNederland.nl.~~

- ~~Technische verwijzing:~~

  - ~~Formaat: tekst~~

  - ~~Kardinaliteit: 1..1~~

  - ~~<https://schema.org/conditionsOfAccess>~~

### 1.3.6.1 schema:propertyID

- Beschrijving: gebruikelijk ID voor contextualisatie

- Voorbeeld:

- Verplicht: optioneel

- Technisch:

  - Format: string

  - Kardinaliteit: 0..1

  - <https://schema.org/propertyID>

### 1.3.6.2. schema:value

- Beschrijving:

- Voorbeeld:

- Verplicht: optioneel

- Technisch:

  - Format: string

  - Kardinaliteit: 0..1

  - <https://schema.org/value>

### 1.3.6.3 schema:description

- Beschrijving:

- Voorbeeld:

- Verplicht: optioneel

- Technisch:

  - Format: string

  - Kardinaliteit: 0..1

  - <https://schema.org/description>

## 1.3.7. schema:Place

### 1.3.7.1 Schema:adressRegion\*

- Beschrijving: provincie waar het object zich bevind.

- Voorbeeld:

  - name: Gelderland

  - sameAs: <https://www.geonames.org/2755634/provincie-gelderland.html>

- Verplicht: optioneel

- Technisch:

  - Format: string

  - Kardinaliteit: 0..1

  - <https://schema.org/AdministrativeArea>

  - <https://schema.org/addressRegion>

<span class="mark"></span>

### 1.3.7.2 Schema:name

- Beschrijving: naam van de plek

- Voorbeeld: Zuid-Holland

- Verplicht: verplicht als schema:Place aanwezig is

- Technisch:

  - Format: string

  - Kardinaliteit 1..1

  - <https://docs.nde.nl/schema-profile/#Place-name>

### 1.3.7.3 Schema:sameAs

- Beschrijving: relatie naar een thesaurusterm

- Voorbeeld:
  <https://www.geonames.org/2743698/provincie-zuid-holland.html>

- Aanbevolen thesauri: Geonames (voor schema:administrativeArea)

- Verplicht: aanbevolen

- Technisch

  - Type: DefinedTerm

  - Format: URI

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#reference-terms>

### 

## 1.3.8 schema:Occupation, schema:DefinedTerm

De rol van de maker van het werk, bv. ‘schilder’.

### 1.3.8.1 Schema:name

- Beschrijving: naam van de rol

- Voorbeeld: schilder

- Verplicht: verplicht als schema:Occupation aanwezig is

- Technisch:

  - Format: string

  - Kardinaliteit 1..1

  - <https://docs.nde.nl/schema-profile/#Person-hasOccupation>

### 1.3.8.2 Schema:sameAs

- Beschrijving: schilder

- Voorbeeld: <http://vocab.getty.edu/page/aat/300025136>

- Aanbevolen thesauri: AAT, CHT

- Verplicht: aanbevolen

- Technisch

  - Type: DefinedTerm

  - Format: URI

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#reference-terms>

## 1.3.9. schema:DefinedTerm

Aanvullende relevante termen via relaties genre en about.

<https://docs.nde.nl/schema-profile/#reference-terms>

### 1.3.9.1 Schema:name

- Beschrijving: naam van de plek (als voorbeeld)

- Voorbeeld: Zuid-Holland

- Verplicht: optioneel

- Technisch:

  - Format: string

  - Kardinaliteit 0..\*

  - <https://docs.nde.nl/schema-profile/#Place-name>

### 1.3.9.2 Schema:sameAs

- Beschrijving: relatie naar een thesaurusterm

- Voorbeeld:
  <https://www.geonames.org/2743698/provincie-zuid-holland.html>

- Aanbevolen thesauri: Geonames, AAT, CHT, RKDArtists

- Verplicht: aanbevolen

- Technisch

  - Type: DefinedTerm

  - Format: URI

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#reference-terms>

## 1.3.10 schema:Product\*

Materiaal dat bij de vervaardiging van het werk gebruikt is.

<https://docs.nde.nl/schema-profile/#CreativeWork-material>

### 1.3.10.1 Schema:name

- Beschrijving: naam van het material

- Voorbeeld: canvas

- Verplicht: verplicht als schema:material aanwezig is

- Technisch:

  - Format: string

  - Kardinaliteit 1..1

  - <https://docs.nde.nl/schema-profile/#CreativeWork-material>

### 1.3.10.2 Schema:sameAs

- Beschrijving: relatie naar een thesaurusterm

- Voorbeeld:
  <https://data.cultureelerfgoed.nl/term/id/cht/1040c581-3cbb-48c9-91b1-d529573bed98>

- Aanbevolen thesauri: CHT, AAT

- Verplicht: aanbevolen

- Technisch

  - Type: DefinedTerm

  - Format: URI

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#reference-terms>

### 

## 1.3.11 schema:Text\*, schema:DefinedTerm

Aanvullende tekstuele beschrijving, of categorisering van het werk.

### 1.3.11.1 Schema:name

- Beschrijving: Aanvullende tekstuele beschrijving, of categorisering
  van het werk.

- Voorbeeld: Canvas

- Verplicht: optioneel

- Technisch:

  - Format: string

  - Kardinaliteit 0..\*

  - <https://schema.org/name>

### 1.3.11.2 Schema:sameAs

- Beschrijving: relatie naar een thesaurusterm

- Voorbeeld:
  <https://data.cultureelerfgoed.nl/term/id/cht/1040c581-3cbb-48c9-91b1-d529573bed98>

- Aanbevolen thesauri: CHT, AAT

- Verplicht: aanbevolen

- Technisch

  - Type: DefinedTerm

  - Format: URI

  - Kardinaliteit: 0..\*

  - <https://docs.nde.nl/schema-profile/#reference-terms>
