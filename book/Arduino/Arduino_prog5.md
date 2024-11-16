# Programmeren deel 5

## Random
Voor bijvoorbeeld het maken van spelletjes met Arduino wil je random getallen gebruiken. De Arduino heeft ook de mogelijkheid voor een random getallen generator. Deze functie print willekeurig getallen. De functie Random is echter niet geheel random. Elke keer dat je de Arduino start zal dezelfde getallen reeks verschijnen. Om dit te voorkomen kun je gebruik maken van ruis, dat is immers altijd random. Door pin A0 uit te lezen (als er niets is aangesloten) kun je dit als input gebruiken om een reeks getallen random te krijgen. De code hiernaast kan daarvoor gebruikt worden.

## Programmeren met Arrays
Een serie getallen kun je in een rij (array) zetten. Daarmee kan een stuk code overzichtelijker worden. Een voorbeeld is: 
int ledgroen[] = {6,7,8,9};
Deze code kun je gebruiken om 4 ledjes aangesloten op pinnen 6,7,8 en 9 aan te sturen. De code: digitalWrite(ledgroen[0],HIGH); zal de led op pin 6 aan zetten. 
Je kunt een array ook langer maken in een loop. Wel moet de Arduino de totale lengte van de rij van te voren weten. Een mogelijke start voor je code van Simon says staart hiernaast.

## Functies programmeren
Voor een code die vaak herhaald wordt kun je een functie aanmaken. Functies zijn kleine stukjes code die aangeroepen kunnen worden. In onderstaande code wordt gebruik gemaakt van een functie die een led aan en uit zet. Nevenstaande code kan gebruikt worden voor een verkeerslicht.

De functie heet aanuit en vraagt twee dingen, een pinnummer en een wachttijd. Deze worden in het script gebruikt. Bij het aanroepen van de functie kun je die twee waarden geven.
Bij robotica is het handig om te werken met functies, bijvoorbeeld voor vooruit/achteruit/bocht om.

## Switch case
Je kunt met Arduino een soort keuzemenu maken waar je doorheen kunt lopen. Dit wordt een switch case genoemd. Het idee is dat je een genummerd keuze menu maakt waarbij een variabele  (hier var) aangeeft waar je in het keuze menu bent. Een eenvoudig voorbeeld van een case switch:

Je kunt eenvoudig switchen van menu door bijvoorbeeld een counter te maken. var = counter%2 geeft nu de waarde 0 bij een even getal en 1 bij een oneven getal.



## Simultaan werken
De Arduino kan geen twee dingen tegelijkertijd (er is wel een truc genaamd interrupts). Om toch twee dingen tegelijk uit te voeren kun je werken met timers. Daarbij is het belangrijk om geen delay te gebruiken in je script. Deze stopt namelijk het hele proces. In de voorbeeldscripts van Arduino vind je het programma Blinkwithoutdelay waarin het eenvoudige programma Blink is herschreven.
Bovenaan wordt een tijdsinterval gekozen. Als er een seconde voorbij is moet de LED wisselen van status. Dit wordt gedaan door de tijd op te vragen (millis()) en te vergelijken met de tijd van de vorige keer dat de led gewisseld is van status. Is de voorbije tijd nog niet groter dan het gekozen tijdsinterval wordt de rest van de loop afgedraaid (deze is in dit voorbeeld leeg). 
Op deze wijze kun je de status van de LED wijzigen en de gehele tijd letten op bijvoorbeeld een drukknop en of deze wordt ingedrukt. 
Het programma kan ook korter geschreven worden.
