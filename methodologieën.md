**Waterfall**
Een lineaire aanpak van projectmanagement waarbij een project stap voor stap in vaste fasen wordt doorlopen en het eindproduct pas op einde wordt voorgesteld en is dus predictive.
Er zijn 7 fasen: 
	-Analyse
	-Ontwerp
	-Implementatie/bouw
	-Testen
	-Oplevering
	-onderhoud
Wordt het meeste gebruikt bij industriële projecten maar wordt nu ook toegepast bij softwarebedrijven. 
Wordt het best gebruikt bij projecten die vaste, onveranderde requirements hebben.
Voordelen: 
	-Duidelijk structuur: doel, planning en taken zijn vooraf duidelijk
	-eenvoudig te beheren: voortgang is goed te volgen
	-Goede vastlegging: elke fase lever duidelijke documentatie op.
Nadelen:
	-Men kan niet naar een vorige fase terugkeren waardoor fouten in het begin pas later uitkomen.
	-Testen gebeurt ook helemaal op einde.
	-Veranderingen tijdens het project zijn moeilijk door te voeren.

**V-model(uitbreiding waterval methode)**
Ook een lineaire projectmanagement methode die het project een V vorm geeft. Linkerzijde draait om ontwerpen en specificeren. De rechterzijde om testen en valideren. Deze is ook predictive.

2 Takken die samenkomen in de punt waarbij de punt de implementatie of bouw is van het product.

linkerzijde(verificatie):
	-behoeften en vereisten: wat vraagt de klant of de markt?
	-systeemontwerp: Globale architectuur van het systeem.
	-Architectonisch ontwerp: specificaties van de onderlinge componenten(highlevel design)
	-Module-ontwerp: gedetailleerde technische ontwerp per onderdeel(lowlevel design)
	-Coderen/implementatie
Rechterzijde(validatie):
	-unit-testen
	-integratietesten
	-systeemtesten
	-acceptatietesten

**Spiral Model**

wordt op een itererende manier door 4 stappen gegaan: 
	1 doelstellingen vaststellen
	2 risico's vaststellen en oplossen
	3 development en testen
	4 de output wordt geëvalueerd en plannen van de volgende iteratie
voordelen:
	-minder risico's
	-er kan altijd functionaliteit worden bijgevoegd
	-de software kan al in een vroeg stadium worden getoond dus ook een vroege feedback van de klant
nadelen:
	- de risico analyse vereist een hoge expertise
	- alles hangt eigenlijk af van een goede risicoanalyse

**Rational Unified Process(RUP)**

werkt op een itererende manier en is opgebouwd uit 2 dimensies:
	-de horizontale as: tijdsdimensie met fasen en iteraties
	-de verticale as: procesdimensie met discipline en activiteiten

4 fasen van RUP:
	1. Inception(start): bepalen van de basisvisie, de scope en de haalbaarheid van het project
	2. elaboration(verkenning): analyseren van de exacte systeemvereisten en het ontwerpen van de basisarchitectuur. Hier worden de grootste risico's bepaald en aangepakt.
	3. construction(bouw): bouwen en programmeren van het softwaresysteem in opeenvolgende iteraties.
	4. transition(overdracht): overdragen van het eindproduct naar de klant inclusief testen, trainen en uitrol

kenmerken:
	-iteratief
	-use-case gedreven
	-aanpasbaar
	-model gebaseerd: er wordt veel gebruik gemaakt van visuele uml-diagrammen

|**Voordelen**|**Nadelen**|
|---|---|
|**Sterk risicobeheer:** Grote risico's worden vroegtijdig (al in de _Elaboration_-fase) geïdentificeerd en aangepakt.|**Hoge administratieve druk:** Er is een sterke focus op het bijhouden van uitgebreide documentatie en formele _artifacts_.|
|**Voorspelbare kwaliteit:** Door de iteratieve aanpak en constante tussentijdse testen blijft de softwarekwaliteit hoog.|**Minder flexibel bij wijzigingen:** Het proces is minder adaptief dan pure Agile-methoden wanneer klantwensen laat in het project veranderen.|
|**Duidelijke structuur en rollen:** Iedereen in het team weet exact wat de verantwoordelijkheden, taken en mijlpalen zijn.|**Compleet en complex:** Het raamwerk is zo omvangrijk dat het voor kleine teams of projecten vaak te 'zwaar' (_overhead_) is.|
|**Herbruikbaarheid van code:** De focus op een solide softwarearchitectuur zorgt voor modulaire en herbruikbare componenten.|**Hoge leercurve:** Het vereist diepgaande expertise en training (bijvoorbeeld in UML) om RUP succesvol te implementeren.|
- **Wel geschikt voor:** Grote, complexe enterprise-projecten met een hoog risicoprofiel, waarbij de eisen vooraf grotendeels bekend zijn en waar strenge compliance- of documentatie-eisen gelden (zoals in de luchtvaart, bankensector of overheid).
- **Niet geschikt voor:** Kleine teams, startups, of projecten met zeer dynamische, snel veranderende functionele eisen.

**Scrum**
populaire agile methode om op een flexibele, snelle en productieve manier software of andere producten te ontwikkelen. Scrum werkt in korte vaste periodes van 1 tot 4 weken. dit zijn sprints en aan het einde van elke sprint levert het team een werkend en getest productonderdeel op.

Het proces heeft 3 vaste rollen en 1 vaste cyclus:
	-de rollen: 
		-De product owner die de prioriteiten beheert in de product backlog
		-De scrum master begeleidt het proces en neemt hindernissen weg
		- Developers of scrum team bouwen het product zelfsturend
	-de cyclus: elke sprint begint met een sprint planning en eindigt met een sprint review en een retrospective. Dagelijks houdt het team ook en korte scrum van 15 minuten om de voortgang aft te stemmen

|**Voordelen**|**Nadelen**|
|---|---|
|**Hoge flexibiliteit:** Het team kan snel inspelen op veranderende wensen van de klant of de markt na elke Sprint.|**Minder voorspelbaar op lange termijn:** Omdat de scope flexibel is, is het lastig om vooraf een harde einddatum of exact budget vast te leggen.|
|**Snelle waarde (Time-to-market):** De klant ziet al na enkele weken werkende software en kan direct feedback geven.|**Hoge tijdsintensiteit:** De vaste overleggen (_Scrum events_) vragen veel tijd en discipline van het team en de stakeholders.|
|**Hoge teamspirit:** Teams zijn zelfsturend en dragen gezamenlijk de verantwoordelijkheid, wat motivatie en eigenaarschap vergroot.|**Kans op 'Scope Creep':** Zonder een sterke Product Owner kunnen er steeds nieuwe eisen worden toegevoegd, waardoor het project nooit eindigt.|
|**Transparantie:** Door dagelijkse updates en visuele Scrum-borden is voor iedereen direct duidelijk waar eventuele knelpunten liggen.|**Minder focus op documentatie:** De nadruk ligt op werkende software, waardoor de documentatie voor later beheer soms achterblijft.|
- **Wel geschikt voor:** Projecten waarbij de einddoelen of functionele eisen vooraf nog **niet 100% helder** zijn, innovatieve trajecten (startups/nieuwe producten), en omgevingen die snel veranderen en vragen om directe feedback van eindgebruikers.
- **Niet geschikt voor:** Projecten met een vastomlijnde, onveranderlijke scope en een keiharde deadline/budget (zoals infrastructurele bouwprojecten), of bij teams waar micro-management heerst en zelfsturing niet wordt losgelaten.

**Extreme Programming(XP)**

een agile methode dat de focus volledig legt op technische en code kwaliteit. xp gaat vooral over de praktijk van het programmeren zelf.
Programmeerpraktijken worden naar het extreme niveau getrokken . Als de code reviews goed zijn, reviewen we code continu (pair programming) en als testen goed zijn, testen we altijd(test-driven development).

XP kenmerken:
	-Pair programming: 2 programmeurs werken tegelijk aan het zelfde
	-Test-driven Development: devs schrijven eerst een geautomatiseerde test en pas daarna de code om die test te laten slagen.
	-Continuous Integration: wijzigingen worden meerdere keren per dag samengevoegd in de hoofdcode en automatisch getest om integratiefouten te voorkomen.
	-On-site Customer: een vertegenwoordiger van de klant zit fysiek bij het ontwikkelteam om direct vragen te beantwoorden en feedback te geven.

| **Voordelen**                                                                                                                                        | **Nadelen**                                                                                                                                     |
| ---------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| **Extreem hoge codekwaliteit:** Door de constante tests en reviews bevat de software nauwelijks bugs of fouten.                                      | **Zeer intensief en vermoeid:** Hele dagen in tweetallen programmeren (Pair Programming) eist mentaal veel van ontwikkelaars.                   |
| **Hoge klanttevredenheid:** De klant is nauw betrokken en ziet het product continu verbeteren en veranderen op basis van feedback.                   | **Duur op korte termijn:** Het schrijven van dubbele code (tests + software) en het werken in duo's kan in het begin aanvoelen als tijdverlies. |
| **Geen verspilling (Lean):** Er wordt alleen code geschreven die _nu_ nodig is, zonder complexe architecturen voor "toekomstige" functies te bouwen. | **Cultuurclash:** Ontwikkelaars moeten hun ego opzij kunnen zetten; code is van het hele team, niet van een individu (_Collective Ownership_).  |
| **Flexibel bij verandering:** Code is zo modulair en goed getest dat aanpassingen laat in het project heel veilig gedaan kunnen worden.              | **Minder focus op design/architectuur:** Door de focus op directe code kan de langetermijnvisie van het systeemontwerp soms ondersneeuwen.      |
**Wel geschikt voor:**

- **Cruciale software:** Systemen waar fouten fataal zijn (medisch, banken, beveiliging).
- **Onvoorspelbare projecten:** Projecten met wekelijks veranderende eisen.
- **Kleine teams:** **3 tot 12 ontwikkelaars** die intensief samenwerken.
- **Betrokken klanten:** Klanten die dagelijks bereikbaar zijn voor directe feedback.

**Niet geschikt voor:**

- **Grote teams:** Grote groepen verspreid over verschillende tijdzones.
- **Afwezige klanten:** Klanten die geen tijd hebben voor tussentijdse feedback.
- **Simpel werk:** Standaard projecten met een vaste, eenvoudige scope.
- **Individuele culturen:** Teams waar ontwikkelaars liever alleen op hun eigen eilandje werken.


**LEAN**

Een methode waar er minder tijd wordt gespendeerd aan development voor betere resultaten te bekomen.
Dit gebeurt door op voorhand belangrijke data te verzamelen van gebruikers. De kunst is hier om te weten te komen wat de klanten echt willen en hoeveel ze ervoor bereidt zijn te betalen.
Voor developers is zo'n set van user stories makkelijker te programmeren en te implementeren.

Hoe werkt dit dan:
je gaat de gebruikers vragen stellen om zo data te verzamelen en maakt er user stories van om zo te weten wat het uiteindelijk product moet worden. Dit wordt dan via 2 tot 3 korte iteraties wordt het product gebouwd. gebruikers gebruiken dan het product en zorgen voor feedback en zo wordt dan het product geevolueerd en worden er features toegevoegd zodat het goed werkt en gemakkelijk te gebruiken is. Er wordt veel waarde geleverd terwijl er weinig tijd voorbij gaat.

7 principes:
- **1. Verspilling elimineren:** Schrap alles wat geen waarde toevoegt voor de klant.
- **2. Leren versterken:** Verbeter constant door snelle feedback en kortcyclisch testen.
- **3. Beslissingen uitstellen:** Maak belangrijke keuzes zo laat mogelijk op basis van feiten.
- **4. Snel leveren:** Breng updates snel naar de klant voor directe feedback.
- **5. Teams motiveren:** Geef de werkvloer de autoriteit om zelf beslissingen te nemen.
- **6. Kwaliteit inbouwen:** Voorkom fouten vooraf in plaats van ze achteraf te repareren.
- **7. Het totaalplaatje zien:** Optimaliseer het hele proces, niet slechts één klein onderdeel.


| Voordelen                                                                                                   | Nadelen                                                                                                                     |
| ----------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| **Lagere kosten:** Minder verspilling betekent direct minder onnodige kosten.                               | **Hoge discipline vereist:** Het succes valt of staat met een zeer strakke zelforganisatie van het team.                    |
| **Kortere time-to-market:** Producten en updates zijn veel sneller klaar voor de klant.                     | **Slecht bestand tegen rigiditeit:** Werkt niet in bedrijven waar managers alles van bovenaf willen controleren.            |
| **Hogere kwaliteit:** Door continue kwaliteitscontrole zijn er minder fouten in het eindproduct.            | **Risico op scope creep:** Zonder duidelijke focus kan het continu aanpassen leiden tot een product dat nooit écht 'af' is. |
| **Gemotiveerd team:** Medewerkers krijgen veel eigen verantwoordelijkheid, wat zorgt voor meer werkplezier. | **Documentatie-tekort:** Door de focus op snelheid kan belangrijke documentatie soms verwaarloosd worden.                   |
Wel geschikt voor:

- **Software- en app-ontwikkeling:** Dit is de bakerbak van deze 7 principes (veelal gecombineerd met Scrum of Agile).
- **Startups en scale-ups:** Bedrijven die snel moeten innoveren en hun product moeten testen in een veranderende markt.
- **R&D (Research & Development):** Afdelingen die nieuwe, innovatieve fysieke of digitale producten ontwerpen.

Niet geschikt voor:

- **Strikte bouw- en infrastructuurprojecten:** Bij het bouwen van een brug of tunnel kun je beslissingen (zoals de fundering) niet uitstellen. Alles moet vooraf exact vaststaan.
- **Zwaar gereguleerde sectoren (bv. farmacie of luchtvaart):** Hier zijn wetgeving, dikke documentatiepakketten en vooraf vastgelegde protocollen verplicht om de veiligheid te garanderen.
- **Repetitief lopendebandwerk:** Voor puur herhalende fabrieksproductie gebruikt men de _klassieke_ Lean Manufacturing, niet deze specifieke ontwikkelingsvariant.

**KANBAN**

Dit is een visuele methode om werk te plannen, te beheren en continu te verbeteren. Het is oorspronkelijk ontwikkeld door **Toyota** om de productie in fabrieken soepel te laten verlopen, maar het wordt tegenwoordig wereldwijd gebruikt op kantoren, in de IT en voor persoonlijke productiviteit.

De kern van Kanban is het **Kanban-bord**. Dit bord is opgedeeld in kolommen die de stappen in het werkproces voorstellen. De meest simpele vorm heeft drie kolommen:

```
[ Te doen (To Do) ] -> [ Mee bezig (In Progress) ] -> [ Klaar (Done) ]
   [ Taak A ]                 [ Taak C ]                 [ Taak E ]
   [ Taak B ]                 [ Taak D ]
```

Elke taak staat op een losse kaart (bijvoorbeeld een Post-it of een digitale kaart in tools zoals **Trello** of **Jira**). Naarmate het werk vordert, schuiven de kaarten van links naar rechts over het bord.

**Kanban** beheert werkprocessen effectief via **vier centrale basisprincipes**.

- **Maak werk visueel:** Toon alle taken op een bord.
- **Beperk onderhanden werk:** Werk aan maximaal een paar taken tegelijk.
- **Focus op doorstroming:** Los opstoppingen in het werkproces direct op.
- **Continu verbeteren:** Evalueer en optimaliseer de werkwijze regelmatig.

|Voordelen|Nadelen|
|---|---|
|**Maximale flexibiliteit:** Prioriteiten kunnen dagelijks veranderen.|**Minder voorspelbaar:** Lastig om harde deadlines op lange termijn te plannen.|
|**Direct overzicht:** Status en bottlenecks zijn direct visueel zichtbaar.|**Disciplinegevoelig:** Werkt alleen als iedereen het bord direct bijwerkt.|
|**Snellere oplevering:** Focus op afronden in plaats van constant starten.|**Risico op chaos:** Zonder beheer wordt het bord snel vol en onoverzichtelijk.|
|**Minder stress:** Voorkomt dat medewerkers te veel taken tegelijk oppakken.|**Complexe koppelingen:** Minder geschikt voor taken die sterk van elkaar afhangen.|
Wel geschikt voor:

- **Continu binnenkomend werk:** Ideaal voor helpdesks, klantenservice en IT-support waar taken ad-hoc binnenrollen.
- **Snel veranderende omgevingen:** Perfect voor startups of marketingteams die direct moeten kunnen inspelen op de waan van de dag.
- **Projecten zonder harde deadlines:** Geschikt voor teams die focussen op een constante, stabiele stroom van opleveringen in plaats van vaste opleverdata.
- **Individuele productiviteit:** Heel handig om je eigen dagelijkse taken en planning visueel overzichtelijk te houden.

Niet geschikt voor:

- **Grote projecten met harde deadlines:** Onveilig voor projecten die maanden vooruit gepland moeten worden met een vaste einddatum.
- **Complexe, opeenvolgende taken:** Ongeschikt voor de traditionele bouw of productie, waar taak B absoluut niet kan starten voordat taak A 100% klaar is.
- **Teams met weinig discipline:** Werkt niet als teamleden het bord niet dagelijks bijwerken of de limieten voor lopend werk negeren.
- **Grote, onverdeelbare taken:** Als taken niet opgeknipt kunnen worden in behapbare kaarten, loopt het bord direct vast.