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

De voorliggende versie van GWSW Gemalen richt zich op punt 1: **Het vastleggen en uitwisselen van _fysieke objectinformatie_ ten behoeve van gemalenbeheer in de riolering.** Dit sluit aan op de primaire behoefte van de gemalenbeheerder namelijk het eenduidig vastleggen en uitwisselen van de informatie in een (gemalen-)paspoort.

De uitwerking voor _Conditie_ en _Meet- en stuurdata_ zal op een later (nog te bepalen) moment verder worden opgepakt. Hiervoor is reeds een basis beschikbaar uit het eerdere traject van de werkgroep. Deze zal dan verder kunnen worden uitgewerkt.

## Gegevensstromen en gereedschappen rond het GWSW

Nu al worden door veel gemeenten en waterschappen de gegevens van rioolstelsels en afvoersystemen op de GWSW Server [apps.gwsw.nl](https://apps.gwsw.nl) gepubliceerd. Deze gegevens komen 1) via de upload functionaliteit van de GWSW Server middels een OroX (.ttl) bestand vanuit het gemeentelijke beheerpakket of 2) via het GegevensKnooppunt Waterschappen (Het Waterschapshuis) terecht in de dataomgeving van de betreffende organisatie op de GWSW Server. 

De module GWSW Gemalen ondersteunt in de gegevensuitwisseling ten behoeve van gemalenbeheer. Het is dus van belang dat de beheerpakketten deze gegevens conform het datamodel GWSW Gemalen aan kunnen leveren. Dit zal via een uitwisselprotocol conform de wereldwijde linked data taal RDF/RDFS/OWL-2/Turtle worden gerealiseerd.

# Advies voor datamodel

## Inleiding

Een gemaal bestaat uit bouwkundige, mechanische en elektrische onderdelen. Al deze onderdelen moeten in meer of mindere mate worden beschreven in het GWSW. Een groot deel daarvan is reeds opgenomen in GWSW 1.6. Hieronder staat de door de werkgroep GWSW Gemalen voorgestelde uitbreiding en aanpassing van het GWSW toegelicht. 

## Algemene aanpassingen

Voor een beheerder is het belangrijk om vast te leggen wat voor soort rioolgemaal het betreft. Dit kunnen de volgende soorten zijn: Boostergemaal, Gemaal droge opstelling, Gemaal natte opstelling, Luchtpersgemaal, Drukrioolgemaal, Opvoergemaal, Riooleindgemaal, Tussengemaal, Vacuümpompstation en Vijzelgemaal. De verschillende soorten onderscheiden zich door hun functie in het grotere geheel of door de toegepaste wijze van verplaatsing van het afvalwater. 

Drukrioolgemaal heeft als synoniemen Minigemaal en Drukrioleringsunit. 

Een onderscheid tussen het soort pompput is niet alleen belangrijk voor het beheer en risicomanagement, maar is ook een relevant gegeven voor hydraulische berekeningen. Daarom wordt voorgesteld om de term Pompput te gebruiken voor rioolgemalen in vrijverval stelsels en de term Drukrioleringsput te gebruiken voor rioolgemalen in mechanische stelsels.

Voor gemalenbeheer is het belangrijk om de kenmerken Bouwjaar en Theoretische levensduur van een gemaal vast te kunnen leggen. Daarnaast is het belangrijk om vast te kunnen leggen wie met de informatie aan de slag gaat. De uitvoerder of het onderhoudsbedrijf is daarom een noodzakelijke uitbreiding van het GWSW. Gezien de breedte van de toepasbaarheid, adviseert de werkgroep deze kenmerken toe te kennen aan een fysiek object, en niet enkel aan een gemaal of bouwwerk.

## Bouwkundige onderdelen

Een beheerder (of uitvoerder) moet bij een gemaal kunnen komen om zijn of haar werkzaamheden te verrichten. Een gemaal kan in een gebouw zitten en/of achter een hekwerk zitten. Beiden zijn voorzien van een slot, waarvoor een sleutel nodig is. Het sleutelnummer wordt vastgelegd in een gemaalpaspoort.

Een elektriciteitskast maakt onderdeel uit van een gemaal. Welke informatie daarvan voor een gemalenbeheerder relevant is om vast te leggen, staat bij de [Elektrische onderdelen](#elektrisch) beschreven.

Een gemaal heeft een pompput die bestaat uit één of meerdere compartimenten of kelders. Dit kunnen zijn: Natte pompkelder, Droge pompkelder en Ontvangstkelder. Dit is voor het beheer belangrijk om vast te leggen. Om de putvulling in procenten te kunnen uitrekenen en om het nulpunt van niveaumetingen te valideren, is het niveau van de bovenkant van de putbodem een relevant gegeven om vast te leggen.

## Mechanische onderdelen

Een rioolgemaal kan het afvalwater verplaatsen met een centrifugaalpomp, een vacuümpomp (in vacuümpompstation), een vijzel (in vijzelgemaal) of een compressor (in luchtpersgemaal). Dit zijn mechanische onderdelen van een gemaal.

### Centrifugaalpomp

Een boostergemaal, gemaal droge opstelling, gemaal natte opstelling, opvoergemaal, riooleindgemaal, tussengemaal en drukrioolgemaal hebben als onderdeel een pomp. Een pomp in de riolering is altijd een centrifugaalpomp, waarbij de vloeistof wordt verpompt door middel van centrifugaal krachten veroorzaakt door een draaiende waaier. Pompen, zoals een schroefcentrifugaalpomp of een schroefpomp, met verschillende type waaiers werken allemaal volgens het principe van de centrifugaalpomp.

Van de pomp is het pompfabrikaat (synoniem is pompfabrikant), pomptype, serienummer en bouwjaar relevant om vast te leggen voor het beheer, alsook de hoogte van het pomphart en de pompplaatsing. De meeste relevante kenmerken voor beheer zijn af te leiden uit het pompfabrikaat en pomptype. Bij de pompplaatsing kan gekozen worden uit Horizontaal of Verticaal. Daarnaast kan worden vastgelegd of het een vaste opstelling is of in een slede.

Een pomp bestaat uit de volgende onderdelen: Pomphuis, pompmotor, pompwaaier, pompsnijplaat, pompmes, pompklauw, aansluiting, geleidestang en hijsketting. 
- Van de pompmotor is de I nominaal, max. toerental, gewicht, typeaanduiding, begindatum, motorvermogen, asvermogen, serienummer en voltage relevant.
- Er zijn op hoofdlijnen twee type pompwaaiers: 1) Vortexwaaier en 2) Centrifugaalwaaier. Een centrifugaalwaaier heeft de volgende subtypen: Gesloten kanaalwaaier, Open kanaalwaaier, Schroefwaaier, N-waaier, Snijwaaier en S-tubewaaier. Bij de pompwaaier is het daarnaast belangrijk het materiaal vast te leggen. Dit kan zijn: Gietijzer, RVS, Chroomstaal (synoniem is Hard iron) of Gehard staal.
- Omdat een pompklauw losgeleverd kan worden van de pomp, is het belangrijk om vast te leggen wat de doorlaatdiameter is en bij welke voetbocht de pompklauw hoort.
- De aansluiting kan zijn aan de onderkant via een voetbocht of aan de bovenkant via een hangkoppeling (synoniem is bovenwaterkoppeling)
 - Van voetbocht is de fabrikant, typeaanduiding, doorlaatdiameter in, doorlaatdiameter uit en het materiaal relevant. Met diameterdoorlaat in en uit kan worden aangegeven dat de voetbocht conisch van vorm is.
 - Van hangkoppeling is de diameter van de slag relevant.
- Van de geleidestang is de diameter en lengte relevant.
- Van de hijsketting is het relevant of deze wel/niet gecertificeerd is, tot wanneer de certificering geldig is, de lengte van de ketting en of deze weg/geen overnameoog (synoniem is overnameschalm) heeft.

### Vacuümpomp

Een vacuümpompstation heeft als onderdeel een vacuümpomp, die het stelsel vacuüm zuigt, waardoor het afvalwater de leidingen in gaat. Van een vacuümpomp is het pompfabrikaat (synoniem is pompfabrikant), pomptype, serienummer en bouwjaar relevant om vast te leggen voor het beheer. 

<a title="Srstevens3, CC BY-SA 4.0 &lt;https://creativecommons.org/licenses/by-sa/4.0&gt;, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Vacuum_Station_Layout.jpg"><img width="null" alt="Vacuum Station Layout" src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f4/Vacuum_Station_Layout.jpg/nullpx-Vacuum_Station_Layout.jpg"></a>

### Vijzel

Een vijzel is een onderdeel van een vijzelgemaal waarvan de volgende kenmerken relevant zijn om vast te leggen: Diameter, lengte, type onderlager, hellingshoek, type vertragingskast, toerental ingaand, toerental uitgaand en serienummer. Een vijzel is géén pomp.

### Compressor

Een compressor is een onderdeel van een luchtpersgemaal waarvan de volgende kenmerken relevant zijn om vast te leggen: Type rotor, type luchtklepje, luchtcapaciteit, luchtdruk, type compressor en serienummer.

<a id="elektrisch">## Elektrische onderdelen</a>

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
