# GWSW Gemalen

<style>
  .symbolSmall{width:20px;height:20px;margin-right:1em;vertical-align:middle}
  .symbol{width:30px;height:30px;margin-right:1em;vertical-align:middle}
</style>


Stichting RIONED is initiatiefnemer en eigenaar van dit GitHub-project. 
Vragen over deze website en het GWSW kunt u stellen via gwsw@rioned.org. 

De module GWSW Gemalen is ontwikkeld door een werkgroep die momenteel bestaat uit:

- Alexander Odijk (Netwerk Afvalwaterketen Delfland (NAD))
- Alfred van Mourik (Waterschap Rivierenland)
- Arno van Geffen (Xylem)
- Audrey Verbeek (Waterschap Aa en Maas / Het Waterschapshuis)
- Erik Blokzijl (Gemeente Almere)
- Freek Verhoef (Gemeente Den Haag)
- Gerard Slob (SENCON/SAM)
- Hans Teunissen (Kennis van Pompen)
- Harm Klopman (Gemeente Groningen)
- Jan Peppelman (Gemeente Utrecht)
- Jeroen Oldenhof (Gemeente Alphen aan den Rijn)
- Klaas Jan Dijkstra (Mous)
- Marcel Krabbenborg (InterAct / I-Real)
- Marc van der Wulp (Waterschap Hollandse Delta)
- Michel de Groot (Mous)
- Michel Wijbrants (Techniek Nederland)
- Robert Verel (Remondis)
- Siebrand vd Hoeven (Netwerk Afvalwaterketen Delfland (NAD))
- Wilbert Banen-Vermeulen (Netwerk Afvalwaterketen Delfland (NAD))

En vanuit Stichting RIONED zijn de volgende personen betrokken:

- Eric van Gorkum (GWSW Modelleerteam)
- Eric Oosterom (Projectmanager)
- Jordie Netten (Projectleider)

Gelieve de inhoudsopgave als leeswijzer te beschouwen.

# Inleiding

Gemalen zijn belangrijke objecten in de afvalwaterketen. Ze verpompen het afvalwater via aangesloten persleidingen tussen verschillende rioleringsgebieden en uiteindelijk naar de rioolwaterzuiveringinrichting (RWZI). Ze moeten dan ook goed worden beheerd.

Waar het beheer van vrijverval rioolstelsels doorgaans is geregistreerd in één beheerpakket, is het gemalenbeheer vaak op meerdere plekken geregistreerd en worden de gegevens op verschillende manieren opgeslagen. Daardoor is het lastig om gegevens te combineren en uit te wisselen met interne en externe partijen. Het kost vaak veel tijd en is foutengevoelig. Door gebruik te maken van een eenduidige terminologie is het mogelijk om op een efficiënte en vergelijkbare wijze de gegevens van gemalen vast te leggen en uit te wisselen. Dit vereenvoudigt en verbetert het gemalenbeheer. De gemalenbeheerder wordt ontzorgd, de dienstverlening door bedrijven wordt verbeterd en innovaties kunnen breder toepasbaar worden gemaakt.

De afkorting GWSW staat voor GegevensWoordenboek Stedelijk Water, de open standaard waar Stichting RIONED met alle relevante partijen aan werkt. Met het GWSW worden komende jaren alle objecten en hun gegevens, hun onderlinge relaties, en de beheeractiviteiten binnen het domein stedelijk water eenduidig gedefinieerd en vastgelegd ten behoeve van soepele gegevensuitwisseling en beter beheer. Meer informatie daarover vindt u via [www.riool.net/gwsw](https://www.riool.net/gwsw).

De algemene beschrijving van het GWSW model vindt u op [data.gwsw.nl](https://data.gwsw.nl/). De datamodellen GWSW-Basis (operationeel beheer), GWSW-Rib (inspectie en reiniging van leidingen, putten en kolken), GWSW-Hyd (hydraulische modellering) en GWSW-Kengetallen (afvalwaterprognoses) zijn al eerder vastgestelde onderdelen van het GWSW. De tools rondom GWSW vindt u op [apps.gwsw.nl](https://apps.gwsw.nl).

Een groot deel van de riolering en de afvalwaterketen kan al worden beschreven met het GWSW. Gemalen zijn hierin al opgenomen, maar de benodigde detaillering voor goed beheer en uitwisseling ontbreekt nog. Dit wordt beschreven in GWSW Gemalen.

# GWSW Gemalen

## Inleiding

In 2018 is Stichting RIONED samen met een werkgroep begonnen aan de ontwikkeling van GWSW Gemalen. De samenstelling van de projectgroep en de werkgroep is over de tijd veranderd, door onder andere functiewisselingen van de deelnemers bij hun werkgevers. Daarnaast heeft de ontwikkeling van het GWSW ook niet stilgestaan en zijn er een groot aantal verbetervoorstellen uit de werkgroep reeds verwerkt in nieuwere versies van het GWSW.

De vigerende versie is GWSW 1.6. Ten behoeve van de leesbaarheid van voorliggende pagina (gegevensspecificatie) en het datamodel is ervoor gekozen om het advies voor GWSW Gemalen op deze versie aan te sluiten. Eventuele keuzes en inbreng van de werkgroep die betrekking hebben op eerdere versies van het GWSW zijn niet meegenomen in dit document, maar zijn afzonderlijk verwerkt.

## Doel

Het uiteindelijke doel van GWSW Gemalen is een breed gedragen standaard voor het vastleggen en uitwisselen van gegevens van:

1)	Objecten
2)	Conditie
3)	Meet- en stuurdata

De voorliggende versie van GWSW Gemalen richt zich op punt 1: **Het vastleggen en uitwisselen van objectinformatie ten behoeve van gemalenbeheer in de riolering.** Dit sluit aan op de primaire behoefte van de gemalenbeheerder namelijk het eenduidig vastleggen en uitwisselen van de informatie in een (gemalen-)paspoort.

Bij de doorontwikkeling van GWSW Gemalen zal deze module uitgebreid kunnen worden voor de beschrijving van de punten _2) Conditie_ en _3) Meet- en stuurdata_ . Hiervoor is reeds een basis beschikbaar uit het eerdere traject van de werkgroep. Deze zal dan verder kunnen worden uitgewerkt.

## Gegevensstromen en gereedschappen rond het GWSW

Nu al worden door veel gemeenten en waterschappen de gegevens van rioolstelsels en afvoersystemen op de GWSW Server [apps.gwsw.nl](https://apps.gwsw.nl) gepubliceerd. Deze gegevens komen 1) via de upload functionaliteit van de GWSW Server middels een OroX (.ttl) bestand vanuit het gemeentelijke beheerpakket of 2) via het GegevensKnooppunt Waterschappen (Het Waterschapshuis) terecht in de dataomgeving van de betreffende organisatie op de GWSW Server. 

De module GWSW Gemalen ondersteunt in de gegevensuitwisseling ten behoeve van gemalenbeheer. Het is dus van belang dat de beheerpakketten deze gegevens conform het datamodel GWSW-Gemalen aan kunnen leveren. Dit zal via een uitwisselprotocol conform de wereldwijde linked data taal RDF/RDFS/OWL-2/Turtle worden gerealiseerd.

# Advies voor datamodel

## Inleiding

Een gemaal bestaat uit bouwkundige, mechanische en elektrische onderdelen. Al deze onderdelen moeten in meer of mindere mate worden beschreven in het GWSW. Een groot deel daarvan is reeds opgenomen in GWSW 1.6. Hieronder staat de door de werkgroep GWSW Gemalen voorgestelde uitbreiding en aanpassing van het GWSW toegelicht. 

## Algemene aanpassingen

Voor gemalenbeheer is het belangrijk om de kenmerken Bouwjaar en Theoretische levensduur van een gemaal vast te kunnen leggen. Daarnaast is het belangrijk om vast te kunnen leggen wie met de informatie aan de slag gaat. De uitvoerder of het onderhoudsbedrijf is daarom een noodzakelijke uitbreiding van het GWSW. Gezien de breedte van de toepasbaarheid, adviseert de werkgroep deze kenmerken toe te kennen aan een fysiek object, en niet enkel aan een gemaal of bouwwerk.

## Bouwkundige onderdelen (VANAF HIER NOG TEKSTUEEL AANPASSEN)

Een beheerder (of uitvoerder) moet bij een gemaal kunnen komen om zijn of haar werkzaamheden te verrichten. Een gemaal kan in een gebouw zitten en/of achter een hekwerk zitten. Beiden zijn voorzien van een slot, waarvoor een sleutel nodig is. Het sleutelnummer wordt vastgelegd in een gemaalpaspoort.

Een Elektriciteitskast maakt onderdeel uit van een gemaal. Welke informatie daarvan voor een gemalenbeheerder relevant is om vast te leggen, staat in Paragraaf 3.5.

Een gemaal heeft verder een (pomp)put die bestaat uit één of meerdere compartimenten of kelders. Dit kunnen zijn: Natte pompkelder, droge pompkelder, ontvangstkelder, XXX. Dit is voor het beheer belangrijk om vast te leggen. Om de putvulling in procenten te kunnen uitrekenen en om het nulpunt van niveaumetingen te valideren, is het niveau van de bovenkant van de putbodem een relevant gegeven om vast te leggen.

Het onderscheid tussen het soort pompput is niet alleen belangrijk voor het beheer (en risicomanagement), maar is ook een relevant gegeven voor hydraulische berekeningen. Daarom wordt voorgesteld om:
Put > Rioolput > Pompput te gebruiken voor rioolgemalen in vrijverval stelsels
Put > Rioolput > Pompunit is een pompput in mechanische stelsels > Of is er een betere naam voor deze put? E.g. Drukrioleringsput.

 
Voor een beheerder is het belangrijk om vast te leggen wat voor soort rioolgemaal het betreft. Dit kunnen de volgende soorten zijn: Boostergemaal, gemaal droge opstelling, gemaal natte opstelling, luchtpersgemaal, minigemaal[^1], opvoergemaal, riooleindgemaal, tussengemaal, vacuümpompstation en vijzelgemaal. 

De verschillende soorten onderscheiden zich door hun functie in het grotere geheel of door de toegepaste wijze van verplaatsing van het afvalwater.

[^1]: Naast het toevoegen van concepten en aanpassen van definities, moet het GWSW worden aangepast voor het concept Minigemaal. Minigemaal is in GWSW 1.6 een synoniem van pompunit, een concept dat onder Rioolput zit en niet bij Rioolgemaal.

## Mechanische onderdelen

Een rioolgemaal kan het afvalwater verplaatsen met een pomp, een vacuümpomp, een vijzel of een compressor. Dit zijn mechanische onderdelen van een gemaal.

### Pomp

Een boostergemaal, gemaal droge opstelling, gemaal natte opstelling, opvoergemaal, riooleindgemaal, tussengemaal en minigemaal hebben als onderdeel een pomp. Een pomp in de riolering is altijd een centrifugaalpomp[^2], waarbij de vloeistof wordt verpompt door middel van centrifugaal krachten veroorzaakt door een draaiende waaier. Van de pomp is het merk, type en serienummer relevant om vast te leggen voor het beheer, alsook de hoogte van het pomphart en de pompplaatsing. De meeste relevante kenmerken voor beheer zijn af te leiden uit het merk en type van de pomp.

Een pomp bestaat uit de volgende onderdelen: Pompwaaier, pomphuis, pompklauw, pompmotor, pompsnijplaat, pompmes, geleidestang, ketting/hijsinrichting en voetbocht. Van de voetbocht is de doorlaatdiameter en het type relevant. Van de geleidestang is de diameter en lengte relevant. Van de ketting/hijsinrichting is het van belang of deze wel/niet gecertificeerd is en tot wanneer. Een hijskabel hoeft niet te zijn gecertificeerd een hijsketting moet dat wel zijn. 

[^2]: Pompen, zoals een Schroefcentrifugaalpomp of een Schroefpomp, met verschillende type waaiers werken allemaal volgens het principe van de centrifugaalpomp.

### Vacuümpomp

Een vacuümpompstation heeft als onderdeel een vacuümpomp, die het stelsel vacuüm zuigt, waardoor het afvalwater de leidingen in gaat. Een vacuümpomp bestaat uit de volgende onderdelen: XXX

### Vijzel

Een vijzel is een onderdeel van een vijzelgemaal waarvan de volgende kenmerken relevant zijn om vast te leggen: Diameter, lengte, type onderlager, hellingshoek, type vertragingskast, toerental ingaand, toerental uitgaand en serienummer. Een vijzel is géén pomp.

### Compressor

Een compressor is een onderdeel van een luchtpersgemaal waarvan de volgende kenmerken relevant zijn om vast te leggen: Type rotor, type luchtklepje, luchtcapaciteit, luchtdruk, type compressor en serienummer.

## Elektrische onderdelen

### Algemeen

Kasten, zoals elektriciteitskasten worden in IMBOR opgenomen. Het detailniveau dat gevraagd is in de totstandkoming van GWSW-Gemalen zal binnen het IMBOR worden meegenomen. Daarom is voor GWSW-Gemalen gekozen voor een beperking in de detaillering van elektriciteitskasten.

Het concept ‘Elektriciteitskast’ valt nu onder het concept ‘Apparatuur’. De werkgroep GWSW-Gemalen adviseert om ‘Elektriciteitskast’ te laten vallen onder het concept ‘Kast’ en ‘Kast’ te laten vallen onder het concept ‘Constructieonderdeel’ (zoals in IMBOR).

### Energievoorziening

In Paragraaf 3.3 staat opgenomen dat een elektriciteitskast een onderdeel is van het gemaal. Een pomp, vacuümpomp en een compressor, maar ook de verlichting van het gebouw en het terrein bij het gemaal krijgen hun energievoorziening vanuit die elektriciteitskast. 

Het is voor een beheerder belangrijk om te weten wat de primaire, secundaire en nood energievoorziening van een gemaal is. Het advies van de werkgroep GWSW-Gemalen is om deze informatie te koppelen aan de elektriciteitskast. De energievoorziening kan afkomstig zijn van het elektriciteitsnet, watermodel, windmodel, zonnepanelen, batterij, aggregaat, XXX.

### Type

Voor goed beheer is het belangrijk om vast te leggen wat vanaf welk type elektriciteitskast het gemaal de energievoorziening krijgt. Hiervoor kan gekozen worden uit de volgende typen: Centrale besturingskast, Centrale verdeelkast, Centrale voedingskast, Centrale moederkast, Decentrale besturingskast of Decentrale verdeelkast.
BESPREKEN

# Vervolg

## GWSW versie 1.7
GWSW Gemalen bevat in deze fase enkel de beschrijving van de fysieke objecten. De uitwerking voor _Conditie_ en _Meet- en stuurdata_ zal op een later (nog te bepalen) moment verder worden opgepakt.
Er wordt beoogd een conceptversie van GWSW Gemalen op te nemen in GWSW 1.7 (planning publicatie in zomer 2024). Mochten er zaken toch niet diep of breed genoeg zijn opgenomen, dan kan dit ook nog in toekomstige versies. Hoe de zaken worden opgenomen in het GWSW is aan het modelleerteam.

## Proeftuinen

Na de opname van GWSW Gemalen in GWSW 1.7 zal er gestart worden met proeftuinen, die als validatie en optimalisatie gaan dienen voor GWSW Gemalen. Meer informatie over deze proeftuinen volgt later.
