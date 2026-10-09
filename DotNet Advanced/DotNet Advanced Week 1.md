## Week 1

### C# types

2 Categorien van  types:
	-Value type: bevat een instance van dat type. int, double, float, bool, DateTime, char,... zijn allemaal Value types. Deze staan in de stack van de memory.
	-Reference type: bevat een verwijzing naar een instantie van dat type. verwijzing is de memory address die in de heap staat.

Stack: 
	-verantwoordelijk voor wat er moet uitgevoerd worden in code
	-elke keer als er een methode of functie wordt aangeroepen wordt er een geheugenblok aan toegewezen. Deze bevat de parameter waarde of de waarden van de lokale variabelen
	-De echte waarde van de parameters of lokale variabelen hangt af van de soort type. Reference types hebben een copy van reference van de insantie(heap address). Value types hebben copy van de instantie zelf.
	-de stack werkt op basis van LIFO(last in first out). Alleen de bovenste blok is toegankelijk.
	-als een methode uitgevoerd is wordt de bovenste block weggegooid zodat de block eronder nu kan worden uitgevoerd.

Heap:
	-Verantwoordelijk voor het bijhouden van informatie of instanties
	-alle instanties kunnen altijd aangeroepen worden dus geen LIFO
	- Werkt met garbage collection zodat de heap schoon blijft.(verwijderen van niet meer gebruikte instanties)

Value types: 
	-Variabelen bevat de waarde
	-veel built-in types(Primitives) zijn value types
	-sommige types in de .net class library zijn value types zoals DateTime, KeyValuePair,...
	- je kan je eigen value type definieren met de struct keyword
	- deze types zijn snel te instantieren

struct:
	- value type maken met struct
	- zou 1 waarde moeten voorstellen
	- zou klein moeten zijn (omdat ze vaak worden gekopieerd).

Limieten van struct:
	- geen parameterloze constructor
	- velden niet initialiseren bij de declaratie
	- een constructer moet alle velden initialiseren
	- geen overerving maar welk interfaces implementeren

een andere manier om een value type aan te maken is een enum (hebben we vorig jaar gezien).

reference types:
	-variabele bevat een referentie(pointer, memory address) naar de instantie in de heap. Meerdere variabele kunnen naar dezelfde instantie verwijzen. Bij het aanmaken wordt er een copy van de referentie aangemaakt.
	-sommige built-in types (Primitives) zijn reference types zoals een object, string.
	-Meeste types van de .net class library zijn reference types zoals Dictionary, Random,List, Console,...
	-Je kan je eigen reference type definiëren met de class keyword.

### Property Accessibility

getters en setters zijn accessors en het is mogelijk om toegang tot een van de accessors te beperken.  Het is ook mogelijk om dit te doen bij  auto geïmplementeerde properties( private).

### Atrributes

Zorgt voor een manier om metadata aan code te koppelen en kan argumenten accepteren zoals een method.

Word geplaatst tussen [ vierkante haken ] net voor een stuk code waarvoor je dit wil doen.
Een voorbeeld hier is [obsolete(" een stuk tekst")] en dan de code.
vb:![[Pasted image 20261003132824.png]]

targets hiervoor zijn: 
	-Method, constructor
	-Type (class, struct, interface, enum of delegate)
	-Assembly (project)
	-Event
	-Field
	-Parameter
	-Property
	-ReturnValue
	-...

### Extension methods

Hiermee is het mogelijk om bij al een bestaande types methodes toe te voegen zonder dat je het originele type verandert of een afgeleide type maakt. Het zijn static methods maar worden aangeroepen alsof het instantie methods zijn. dwz je kan het gebruiken met . notatie van een object.

extension method:
	-moet in een static class
	-moet gebruik maken van de keyword extension
	-en tussen haken zet je na de extension keyword the type 
	-kan meerdere methoden in staan en kan ook parameters hebben
	-moeten in dezelfde namespace zitten of anders moet je een using gebruiken.

![[Pasted image 20261003134719.png]]

![[Pasted image 20261003134849.png]]

![[Pasted image 20261003135458.png]]
![[Pasted image 20261003135504.png]]

er is ook een oude methode ziehieronder voorbeeld:
	-ook in een static class
	-method moet ook static zijn
	-met this zeg je welke instantie van de class moet worden uitgebreid.
![[Pasted image 20261003135552.png]]

### Null-conditional operator

syntax:
	-?.
	-dus het voert alleen iets uit als het niet null is anders is het null.
	
![[Pasted image 20261003140006.png]]

dit is hetzelfde als:
![[Pasted image 20261003140023.png]]

### Nullable Reference Type

dezelfde syntax als de nullable value type ?. : string? lastName = null; (hier mag lastName null zijn). Ook goed voor het minimaliseren van nullreferenceexception.

Het toewijzen van een null-reference type aan een nullable reference (en andersom) levert waarschuwingen op.

![[Pasted image 20261003143436.png]]

waarom Nullable reference types?
	-Minder null checks (compiler doet al het werk)
	-compiler vindt alle potentiële null-references ipv ze te vinden @runtime.
	-maakt de code meer expressief

### IS operator

checkt als het resultaat van een expressie compatibel is met een gegeven type.
![[Pasted image 20261003155719.png]]
![[Pasted image 20261003155725.png]]

om te checken als een expressie aan een patroon voldoet

![[Pasted image 20261003155854.png]]

nagaan als er elementen in een list of array zitten

![[Pasted image 20261003155933.png]]

om het runt-time type van een expressie te controleren

![[Pasted image 20261003160043.png]]

### Readonly 

Keyword dat gebruikt wordt bij een veld declaratie. Toewijzen gebeurt alleen bij de declaratie of in een constructor. Een readonly veld kan niet meer gewijzigd worden nadat de constructor klaar is. Dus zodra het object aangemaakt is, is de waarde vastgezet.

![[Pasted image 20261004150524.png]]

### Field backed property declarations

Hier wordt de field keyword gebruikt. Bij een property-accessor wordt er automatisch een achterliggende veld(backing field) gegenereerd en je kan deze dan ook gebruiken zonder dat je dat veld zelf hoeft te declareren.
![[Pasted image 20261004151112.png]]

oude manier:
![[Pasted image 20261004151128.png]]
met field keyword:
![[Pasted image 20261004151142.png]]

### Anonymous types

een object met alleen read-only properties zonder dat er eerst een type moet gedefinieerd worden. Je kan deze maken door gebruik te maken van de new operater samen met een object initialzer(accolades).

![[Pasted image 20261004152445.png]]

De typenaam wordt door de compiler gegenereerd en is niet beschikbaar in je broncode. Ook wordt het type van elke property door de compiler afgeleid en wordt ook meestal gebruikt in de select clause van een LINQ query.

![[Pasted image 20261004152653.png]]

### Lambda's

Dit is een inline method: 
	-parameter namen tusssen haken ()
	-lambda seperator =>
	-method body
	-parameter types en return type worden afgeleid door de compiler
	
![[Pasted image 20261004152957.png]]

Wil je meer code in de body moet je accolades gebruiken.

![[Pasted image 20261004153046.png]]

zijn er geen parameters kan je alleen haken gebruiken ().

![[Pasted image 20261004153146.png]]

