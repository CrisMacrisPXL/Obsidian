## LINQ

### What is LINQ

Language Integrated Query: een c# feature om query's uit te voeren en om data sequences te manipuleren. De data source moet een object zijn dat IEnumerable<> implementeert.
	vb: 
	-In-memory list(List<string>)
	-een object dat een database tabel representeert (DbSet<Person>)
	-een object dat een XML document representeert (XDocument)
	-...
Linq maakt gebruik van een SQL-like syntax of je kan direct gebruik maken van extension methods van IEnumerable<T>

### De 3 delen van een LINQ query operatie

1. De data source: een sequentie van data dat IEnumerable<T> implementeert
2. Maak de query: definieert een filter, sorteer, projectie op de sequentie maar wordt nog niet uitgevoerd
3. De query uitvoeren: Je moet itereren over de query variabel bv in een for loop om het resultaat van de query te krijgen.

![[Pasted image 20261004155454.png]]

### LINQ Providers

Vertaalt LINQ queries in commandos die de datasource begrijpt. Veel gebruikte linq providers zijn:
	-Linq to objects: maakt queries van in-memory collections zoals arrays, lists of dictionaries
	-Linq to entities: vertaal Linq naar sql om een queries te maken in een database
	-Linq to XML: vertaalt Linq naar Xpath om queries te maken in een XML document
Maakt niet uit welke data source, de syntax van een Linq query blijft altijd hetzelfde!

### Syntax

Er zijn 2 Linq syntaxen:
	-query syntax: is net als een sql query en wordt gebruikt voor zeer complexe queries
	
	![[Pasted image 20261004160748.png]]
	-method syntax: maakt gebruik van extension methods van IEnumerable<T> en wordt meestal gebruikt voor simpele queries. 
	
	![[Pasted image 20261004160756.png]]

### Query syntax

Query syntax -From

De query moet beginnen met een from clause en heeft 2 componenten: De data source en de range variable.

![[Pasted image 20261004161006.png]]

Query syntax - Where

where is een filter die bepaalt welke elementen er uit de data source worden teruggegeven. Maakt gebruikt van een true-false conditie op elke data source element. Kan ook range variabele gebruiken van in de from of join en kan methoden aanroepen. Je kan ook meerdere voorwaarden koppelen met  && of ||.

![[Pasted image 20261004161614.png]]

Query syntax - Select

Het laatste deel van een Linq query. De select specificeert het type van het resultaat van de sequence maar kan ook  source sequence omzetten in een nieuwe type.

![[Pasted image 20261004161920.png]]

Query syntax - Orderby

sorteert data oplopend of aflopend(ascending is standaard, descending keyword erbij zetten voor aflopend sorteren)

![[Pasted image 20261004162100.png]]

Query syntax - Join

Voegt 2 data sequences samen net zoals in sql en hier maakt men gebruik van de keyword equals en niet ==.

![[Pasted image 20261004162226.png]]

Er zijn nog andere syntaxen maar die zijn out of scope voor deze cursus. ander zijn : let, group en into.

### Method syntax

Hiermee roep je de Linq extension methods rechtstreeks aan en is beschikbaar als je de volgende namespace gebruikt: using System.Linq

### Welke method?

Welke methode wordt er dan gebruikt? Ze zijn beide functioneel identiek en ook beide even performant. Kies dus het duidelijkste syntax, dus zoals eerder gezegd simpele queries gebruik dan de method syntax en anders de query syntax.

![[Pasted image 20261004162933.png]]

### Query Execution

Hier is sprake van deferred execution wat wil zeggen dat het niet wordt uitgevoerd wanneer je de query maakt maar als je ze itereert door een loop.
Linq komt ook met execution methods zoals ToList() waardoor je onmiddelijk de query uitvoert(under the hood execution). Execution methods geven 1 enkele waarde terug of een collection.

![[Pasted image 20261004163314.png]]

### Execution methods

Er zijn verschililende execution methods:
	-Tolist()
	-ToArray()
	-ToDictionary(keySelector, elementSelector)
	-First(): geeft het 1ste element trg maar een exception als deze leeg is.
	-FirstOrDefault(): geeft het 1ste element trg of default(null of 0) als deze leeg is
	-Single(): Als je maar 1 resultaat wil hebben of anders een error trg geeft
	-SingleOrDefault():Als je geen of 1 resultaat wil hebben maar meerdere geeft een error
	-Count()
	-Any()
	-All(predicate)

![[Pasted image 20261004163811.png]]

![[Pasted image 20261004163827.png]]