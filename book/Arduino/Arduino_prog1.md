# Programmeren deel 1

Arduino heeft een eigen programma dat gebaseerd is op C++. Heb je al ervaring met programmeren en/ of met C++ (of java), dan is het programmeren heel makkelijk. Heb je geen ervaring met programmeren? Het is veel minder moeilijk dan je misschien wel denkt!

Bovenaan het script Blink staat /* dit betekent dat alles na dit beginteken en voor het afsluitteken */ commentaar is. Hier zet je neer hoe het programma heet, wat het doet, wie het gemaakt heeft en wanneer je het voor het laatst hebt veranderd.

Een tweede mogelijkheid om commentaar toe te voegen is met behulp van //. Alles op dezelfde regel na // is commentaar. Zo kun je bijhouden wat de code op die regel doet. Met behulp van de snel code ctrl / kun je code snel omzetten naar commentaar.

Voordat de belangrijkste code wordt uitgevoerd moet je zeggen wat er precies aangestuurd wordt. We geven aan dat in pin 13 iets zit en dat de Arduino daar een output (spanning) geeft als jij dat wilt. Iets netter zou zijn om nog voor de setup aan te geven hoe pin 13 heet: je geeft de pin een naam (int LEDrood = 13;). Wil je pin 13 vervolgens aansturen, dan kan je dat doen met de naam LEDrood.

Alles wat tussen de accolades {} van de loop staat wordt continu herhaald. Eerst wordt pin 13 hoog (5,0 V) gemaakt met behulp van de code digitalWrite (digitalWrite kan alleen aan of uit). Daarna moet het programma 1000 ms wachten (delay) voordat de volgende regel code wordt uitgevoerd.

De volgende regel code maakt pin 13 weer laag (0,0 V). De pin wordt aangestuurd met een hoog of met een laag signaal. Zit daar nog iets tussen? Ja en nee… De output is altijd 0,0 V of 5,0 V. Maar je kunt de LED wel dimmen door maar een bepaalde tijd de LED aan te zetten. Als de LED snel genoeg knippert zie je niet dat de LED knippert, het lijkt er alleen op dat de LED minder fel brandt. Wanneer je een LED wilt dimmen gebruik je een output met het symbool ~. Dit is een Puls Width Modulation (PWM). De waarde van de PWM zit tussen de 0 (geheel uit) en 255 (geheel aan).

**Opdracht 3 Een LED dimmen**

a) Bouw de opstelling die hiernaast staat. Gebruik bij de output een PWM pin, bijvoorbeeld Pin 9 (let op, de LED hoeft niet aangesloten te worden aan de constante spanning, de spanning wordt nu geleverd door pin 9).

b) Open het script Fade in de voorbeelden/basis en upload het script.

c) Beschrijf wat je ziet en probeer met behulp van de code een te verklaren wat er gebeurt.

d) Verander de code zodat de LED sneller volledig brandt en sneller uit is. Let op, er zijn twee manieren! Probeer ze allebei uit.

e) In de code staat analogWrite. Voorheen hebben we digitalWrite gebruikt. Leg uit waarom
dat nu niet kan.

**Opdracht 4 Een aan en uit knop voor de LED**
We kunnen nu de LED met behulp van de code aan en uit zetten en zelfs dimmen. Maar vaak wil je ook een schakeling handmatig aan en uit kunnen zetten. Daarvoor hebben we een drukknop nodig.

a) Bouw de schakeling die hiernaast staat. Let op dat je een grote weerstand gebruikt zodat de te leveren stroom niet te groot is, een Arduino is namelijk slecht in het leveren van grote stroomsterktes.

Het idee is nu dat we pin 2 gebruiken als INPUT. Pin 2 meet de spanning op dat punt (vergelijkt deze met 0,0 V). Dit gebeurt met de code digitalRead(). Deze kan nu een hoog (5,0 V) of laag (0,0 V) signaal meten (met een analoge pin, A0 t/m A5, kunnen ook tussen gelegen waardes (10 bits) gemeten worden). Pin 2 meet alleen een spanning als de knop (button) ingedrukt wordt.

b) Open het script Button via voorbeelden/digitaal en upload het script.

c) Druk op de knop en controleer wanneer de LED uit is en wanneer deze aan is.

d) Pas het script aan zodat de functie van de knop precies omgedraaid wordt.

```{note}
Met de button is er iets bijzonders aan de hand. Deze heeft namelijk een zogenaamde Bounce. Dit betekent dat de spanning niet direct van 0 naar 5V gaat maar, nog een keer op en neer gaat. Dit komt omdat er in de button een veer zit die op en neer gaat. Bij het gebruik en uitlezen van de button is het dus handig om een delay in te bouwen…
```