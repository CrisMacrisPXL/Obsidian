Een besturingssysteem of operating system (OS) is software dat computer hardware gaat managen en diensten aanbiedt voor andere programma's. (basisprogramma v/e computer)
In ons geval Windows, andere zijn linux, macos,...

## 1.1 Wat is een OS?

Verbinding tussen hardware , software en tools (randapparatuur, opslagapparaten, wifi-adapters, beeldschermen). Tools maken gebruik van drivers die door de fabrikant zijn geschreven om met hun apparaten te communiceren.

Belangrijkste verantwoordelijkheid is de interface tussen de gebruiker en de hardware. Dit gebeurt via CLI of via GUI.
Andere verantwoordelijkheden:
	-Software bronnen
	-Geheugentoewijzing en system resources
	-Data opslag
	-Drivers
	-Gebruikers
	-Security
	-Networking
	-File systems

## 1.2 Basis functionaliteiten van een OS

Alle besturingssystemen voeren dezelfde basisfuncties uit:
	-Beheren van de toegang tot hardware
	-Beheren van bestanden en mappen
	-Zorgen voor een gebruikersinterface
	-Applicaties beheren

### 1.2.1 Hardware toegang

interactie tussen programma's en hardware (I/O System Management). Hiervoor gebruikt het OS stuurprogramma(driver) van de hardware om te communiceren met de hardware.
Systeembronnen toewijzen en stuurprogramma's installeren gebeurt met een plug and play (pnp) process. Vindt het OS de stuurprogramma niet moet dit handmatig gebeuren. Het OS configureert het apparaat en werkt de register bij.

### 1.2.2 Bestands- en mappenbeheer (file management)

File management  beheert alle bestandsgerelateerde activiteiten (opslaan, ophalen, benoemen, delen en beschermen).
Het OS maakt een bestandsstructuur op de harde schijf om gegevens op te slaan. Een bestand is een blok van gegevens dat 1 naam krijgt en ook als 1 eenheid behandeld wordt. Directories worden beschouwd als mappen. Mappen in mappen zijn subdirectories.

### 1.2.3 Gebruikersinterface

Interactie tussen software en hardware. 2 Soorten:

#### 1.2.3.1 Command Line Interface (CLI)

Manier om met computerprogramma's te communiceren door commando's in te geven als 1 of meerdere regels tekst. VB CLI zijn MS-DOS, Windows Command Prompt, Powershell, terminal en Linux commandoregel..

Voordelen:
	-Snelheid
	-Scriptability (voor zaken die zich veel herhalen)
	-Consistente interface
Nadelen:
	-Computers doen wat je typt 
	-Ervaring en kennis is nodig

#### 1.2.3.2 Grafischie gebruikersinterface (GUI)

Gebruikers communiceren met menu's en pictogrammen. GUI's zijn gebruiksvriendelijker dan CLI dat text-based is.
	-gebruiksvriendelijk
	-minder complex
	-GUI's kunnen crashen

### 1.2.4 Applicatiebeheer

Het besturingssysteem beheert de uitvoering van programma’s door ze in het geheugen te laden en systeembronnen toe te wijzen.
Programmeurs gebruiken API’s om toepassingen te laten communiceren met het besturingssysteem op een gestandaardiseerde en veilige manier.
API = Application Programming Interface dwz een verzameling definities op basis waarvan een computerprogramma kan communiceren met een andere programma of onderdeel. (Meestal in de vorm van bibliotheken)

### 1.2.5 Andere functionaliteiten

Functionaliteiten:
	-Process management: helpt het OS bij creëren en verwijderen van processen. 
	-Memory management: toewijzen en terug vrijmaken van geheugen voor programma's die het nodig hebben.
	-Device management: apparaatbeheer en de module die hier verantwoordelijk voor is is de I/O-controller.
	-Security: beschermen van gegevens en informatie.

## 1.3 Begrippen m.b.t. OS

applicatie: software om specifieke taken en functies uit te voeren. Meestal een GUI en wordt gestart en uitgevoerd door de gebruiker.
Service: software dat op de achtergrond draait voor een functie of een taak aan te bieden aan een andere programma of systeem. Draait op de achtergrond en wordt vaak automatisch gestart.
Proces: Onderdeel van een applicatie. Een applicatie bestaat uit 1 of meerdere processen.
Thread: Onderdeel van een proces en is een uitvoeringseenheid binnen een proces.
### 1.3.1 Kernel

De kern van een OS is de kernel. De kernel heeft 1 taak en dat is het beheren van de communicatie tussen software en hardware. Kernel is het binneste deel van het OS, de shell is het buitenste deel. De kernel is een van de 1ste dingen die geladen wordt wanneer het OS opstart en wordt uitgevoerd in een geisoleerd gebied om te voorkomen dat ermee geknoeid wordt door andere software.

### 1.3.2 Multi-user

Meerdere gebruikers die individuele accounts hebben waarmee ze tegelijkertijd met programma's en randapparatuur kunnen werken.

### 1.3.3 Multiprocessing

Het OS kan twee of meerdere instructies tegelijk ondersteunen. Het gebruiken van meerdere CPU's of CPU cores.

### 1.3.4 Multitasking

Meerdere toepassingen tegelijk bedienen. Hier zijn meerdere processen tegelijk actief.  Bij systemen met 1 core is er maar 1 proces werkelijk actief. Maar omdat cores vaak van proces wisselen lijkt het alsof de processen tegelijk draaien.  

Het computergeheugen bevat meer processen die in verschillende toestanden kunnen zijn:
	-running: het proces wordt daadwerkelijk uitgevoerd.
	-ready to run: het proces kan draaien, maar is nog niet aan de beurt;
	-waiting: het proces kan niet verder omdat het op een gebeurtenis (event) wacht. 

### 1.3.5 Multithreading

Een programma kan worden opgesplitst in kleinere onderdelen die worden geladen als dat nodig is door het OS.  Bij multithreading kunnen verschillende delen van een programma tegelijkertijd uitgevoerd worden.

### 1.3.6 Process table en scheduler

De kernel houdt procesgegevens bij in de process table. De gedeelte dat een nieuw proces uitkiest om uit te voeren (proces runable maakt) heet de scheduler. Deze kiest een ready-to-run proces uit de process table. 2 schedulers:
	-pre-emptive scheduler: geeft een timeslice (hardwaretimer) aan een proces die na de timer een interrupt genereert. De interrupt afhandeling gebeurt door de kernel en de scheduler kiest een nieuw proces en geeft deze een timeslice. Dus een proces kan nooit het hele systeem voor zichzelf gebruiken.
	-non pre-emptive scheduler: laat het aan de proces zelf over wanneer een volgend proces aan de beurt is. Hier is het probleem dat als er een ingewikkelde rekenpartij moet worden uitgevoerd, het proces de CPU blijf gebruiken. Nog een probleem is als er bij een programmeerfout een eindeloze lus is, andere processen niet meer aan bod komen en er een reset nodig is.

### 1.3.7 Interrupt en event

Een waiting-process wacht op een event. Dit kan vanalles zijn, een character op het toetsenbord dat binnekomt, binnekomen van data via netwerk,... dit zijn allemaal events. Dit gaat gepaard met een interrupt.

### 1.3.8 Drivers

Drivers zijn stukken code dat aan de kernel wordt toegevoegd om te communiceren met randapparatuur. Deze wordt door de fabrikant geleverd.

![[Pasted image 20260215113145.png]]

### 1.3.9 Firmware

Firmware is een beperkt besturingssysteem dat enkele taken kan uitvoeren en is meestal geprogrammeerd in een vast geheugen met een beperkte CPU en zit in de hardware. Bij het opstarten van een pc laadt het moederbord UEFI-firmware. Deze is low-level software dat snel de hardware van u pc initialiseert.

### 1.3.10 Firmware vs OS + 1.3.11 Verschillen

|                                                                                                                          |                                                                                             |
| ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------- |
| Firmware                                                                                                                 | OS                                                                                          |
| Firmware is een soort van programmering embedded op een chip die specifieke taken op apparaat bestuurt.                  | OS biedt functionaliteit dat verder gaat dan deze door de firmware wordt geleverd.          |
| De  programma's binnen een firmware zijn specifiek ontworpen door de chipfabrikant voor specifieke taken of handelingen. | OS is een programma dat door de gebruiker kan worden geïnstalleerd en kan worden gewijzigd. |
| Opgeslagen op een niet-vluchtig geheugen.                                                                                | Opgeslagen op de harde schijf.                                                              |
### 1.3.12 EOS (End of Sale)

Wanneer een product wordt gestopt met verkopen (bij een OS) spreken we van End Of Sale. Support blijft wel doorlopen. Meestal stopt het ontwikkelen van applicaties en drivers dan ook voor een OS.

### 1.3.13 EOL (End of Live)

Bij End of Live stopt ook de ondersteuning van het OS, dus geen updates en patches meer.

### 1.3.14 Updates

Het aanpassen van bestaande code met doel om de code te verbeteren of te beveiligen.  Een update is ook uitgebreider dan een patch. 

### 1.3.15 Patch

Een stukje software dat wordt uitgevoerd om fouten op te lossen. Meestal bij bugs of tekortkomingen van de software.

### 1.3.16 Filesystem

Filesystem bepaalt de methode van het organiseren van data op een opslagmedium en bepaalt hoe de data wordt opgeslagen en opgehaald. Zorgt ook voor een goede hiërarchie en structuur. Vanuit de computer hardware standpunt bestaat er geen file of directory. Het is de file manager die ervoor zorgt dat we dit zo zien als files en folders.

## 1.4 Types of OS

Operating Systems kunnen verschillende doelen hebben.

### 1.4.3 Desktop OS

Heeft als doel dat de gebruiker programma's en tools kan gebruiken bovenop het OS. Deze wordt meestal geïnstalleerd op een laptop of home computer. Er zijn verschillende bekende desktop OS zoals windows, MacOs, CentOs, Ubuntu,...

Bij het kiezen van een OS is het belangrijk om te weten waar het voor gebruikt zal worden.
### 1.4.4 Server OS

Bevat functies die functionaliteiten aanbiedt en services verleend aan andere systemen.
	-ondersteunt meerdere gebruikers
	-draait toepassingen voor meerdere gebruikers
	-levert diensten aan eindgebruikers of andere systemen

voorbeelden hiervan zijn Windows Server, Ubuntu Server

### 1.4.5 Mobile OS

Nadruk op draagbaarheid, gemak en mobiele communicatie. Prioriteiten zijn touchscreen, kleinere schermgrootte , batterij verbruik,...

## 1.5 Verschillende desktop OS

Windows, Linux en MacOs