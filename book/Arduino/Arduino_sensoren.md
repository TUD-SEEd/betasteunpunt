# Sensoren

## Praten met de Arduino
Via de seriële monitor kun je twee kanten op praten met je Arduino. Je kunt informatie opvragen maar ook informatie geven. Getallen, letters, of woorden invoeren is vrij eenvoudig. In het voorbeeld hiernaast wordt een getal gevraagd en gebruikt. Denk wel altijd aan het type variabele wat je wilt verkrijgen! In de voorbeeld code gebruiken we een integer.

## Bluetooth module 
Met de bluetooth module wordt het mogelijk om je Arduino aan te sturen met behulp van je telefoon. Je stuurt dan een stukje tekst (String) naar de Arduino. Er is niet veel code nodig om dit te verwezenlijken. Het lijkt op praten met de Arduino via de seriële monitor. Alleen heb je geen kabel meer nodig. Zo kun je een afstandbestuurbare auto maken. 
De basiscode voor communicatie met de bluetooth module staat hiernaast. Anders dan in het voorbeeld hierboven lezen we nu een karakter (ander datatype) uit. Er zijn wel mogelijkheden om waarden om te zetten, bijvoorbeeld via blueToothVal.toInt(). Deze code maakt van een karakter of string een integer.

De aansluiting van pinnen staat op de module (let op: rx moet naar tx en tx naar rx!). Deze twee pinnen moeten pas verbonden worden met de Arduino als het programma is geüpload. Pin 0 en 1 van de Arduino worden immers ook gebruikt voor communicatie met de computer…

## Geluidsensor 
Een geluidsensor geeft een hoog signaal wanneer het geluidsniveau boven een bepaalde waarde komt. Deze waarde is in te stellen met de potmeter op de sensor. Je kunt helaas geen geluid opnemen via deze sensor.
Het uitlezen van de sensor is vrijwel identiek aan het uitlezen van een button. Je leest (digitaal) de output uit en krijgt een 0 of een 1 terug.

## Timer 
In veel projecten wordt gebruik gemaakt van een timer. Deze kun je maken m.b.v. de code millis(); deze code geeft aan hoeveel milliseconde zijn verstreken sinds de Arduino is aangezet. Maak van de variabelen die de tijd bijhouden wel het type long! 
Een voorbeeldcode is hiernaast weergegeven. Deze toont elke seconde in de seriële monitor dat er een seconde voorbij is. Een volledige code vind je achterin de module.


## Buzzer
In een piëzo buzzer zit een materiaal dat van vorm verandert als er een spanning over heen staat. Je kunt hem ook andersom gebruiken: verbuigt het materiaal dan wordt er een kleine spanning geleverd. Daarmee is dit materiaal ook prima te gebruiken om bijvoorbeeld regendruppels te detecteren. Je kunt er ook een goedkope speaker mee maken, zoals bij deze buzzer.
De Arduino kan één pin aansturen om een toon te maken, het is niet mogelijk meerdere tonen tegelijk te geven. Voor het maken van een toon kun je de tone functie gebruiken: 
tone(pin,frequentie,duration);
In deze functie is de derde optie, duration, optioneel. Met noTone(pin); stop je het geluid weer.
Zoals gezegd kan de buzzer ook andersom gebruikt worden. Je leest hem dan uit via een analoge pin. Echter zullen de gemeten waarden zeer laag zijn.

## Afstandssensor
De ultrasone afstandssensor werkt zoals een vleermuis afstanden bepaalt: Een puls wordt uitgezonden en de tijd tussen uitzenden van de puls en ontvangen van de reflectie wordt gemeten. Deze tijd wordt teruggegeven in microsecondes en kun je vervolgens omrekenen naar een afstand. In de Arduino voorbeelden zit het programma Ping (onder sensors). De afstandssensor die daar gebruikt wordt, werkt met drie pinnen waarbij de pinMode in het programma wordt omgedraaid. Dit programma kun je als basis gebruiken om de sensor met vier pinnen aan te sturen en uit te lezen. Wil je het liever meteen gebruiken? Dan staat de code hiernaast.
Let op! Het is pulsein met de i als hoofdletter.

## Bewegingssensor
Als bewegingssensor kan een Passive InfraRed (PIR) gebruikt worden. Een PIR meet de stralingsenergie in het infraroodspectrum. Bij verandering van intensiteit, dus detectie van beweging, wordt het signaal hoog. 
Het hoedje van de PIR kan opgetild worden zodat je weet welke functie elk van de pinnen heeft. Met de twee stelschroefjes kun je de gevoeligheid en de wachttijd tussen twee metingen instellen. 
De PIR kijkt alle kanten op. Focussen op een bepaald gebied kan door een deel van de sensor af te dekken.

## LM35 
De LM35 is een van de vele temperatuursensoren die je goedkoop kunt krijgen. Volgens de datasheet van TI  heeft deze een bereik tussen -55oC en +150oC met een resolutie van 10 mV/oC. Bij kamertemperatuur is de nauwkeurigheid 0,25oC. Voor temperaturen onder de 2oC moet er extra weerstand in de schakeling opgenomen worden, zie wederom de datasheet voor verder informatie. 
Voor het berekenen van de temperatuur kun je de volgende formule gebruiken: temp = (5.0 * analogRead(tempPin) * 100.0) / 1024;
De Arduino vergelijkt nu de spanning met een interne referentie van 5,0 V. Echter is de uitgelezen waarde altijd kleiner dan 1 V en is de resolutie niet zo hoog als mogelijk. Je kunt dit wijzigen door de interne referentie (1.1V) aan te zetten: analogReference(INTERNAL); Het script voor de LM35 met hoge resolutie is in het boekje opgenomen, maar probeer eerst zelf de eenvoudige versie van de temperatuur uit te lezen!



## H-brug 
Een H-brug maakt het mogelijk om met DC spanning een motor toch twee kanten op te laten draaien. Om dit te doen wordt er gebruik gemaakt van transistoren. Je bestuurt met de Arduino de transistoren S1 t/m S4. Let op! S1 en S2 mogen nooit tegelijk omgezet worden. Dan ontstaat een kortsluitstroom. Hetzelfde geldt voor S3 en S4 (in onderstaande code MCL1 en MCL2).
Met de L298N is het mogelijk twee motoren aan te sturen. Je kunt een hogere (externe) bronspanning leveren. De 5V is nodig voor het aansturen van het interne circuit. Het PWM-signaal (voor het regelen van de snelheid) kan gedaan worden met de ENA. IN1 hoog zetten laat de motor de ene kant op draaien, IN2 de andere kant op. De drie pinnen er naast (IN3, IN4, ENB) doen hetzelfde maar dan voor de andere motor. 
Een voorbeeld code voor de motor staat aan het einde van deze handleiding.

## Dataloggen met een SD-kaart
Wanneer je de Arduino uit zet, is je verzamelde data weg. Wil je gebruik maken van je data dan kun je dit via een omweg wegschrijven naar bijvoorbeeld excel (voorbeelden zijn redelijk eenvoudig op internet te vinden). Een tweede mogelijkheid is om de data weg te schrijven naar een SD-kaart m.b.v. een SD module. Voordeel hiervan is dat de Arduino stand-alone kan draaien en dus op afgelegen plekken (dak van de school) kan liggen.
In de voorbeelden van Arduino staat de code voor datalogger (voorbeelden/SD/datalogger). In dat voorbeeld worden drie analoge pinnen uitgelezen. Er wordt een String aangemaakt en de uitgelezen waarden worden toegevoegd aan deze string. Per meting wordt die string weggeschreven naar de SD kaart. 
In codes achterin staat een voorbeeld van een temperatuurmeting die elke minuut plaats vindt. 

## Hall sensor
Een Hall sensor is een sensor voor het meten van het magnetische veld. De sensor is ideaal om bijvoorbeeld snelheden te meten zoals dat gedaan wordt met een snelheidsmeter op je fiets. De sensor is gebaseerd op het Hall-effect: Elektronen gaan naar een zijde (van een draad) wanneer ze bewegen door een magnetisch veld. Hierdoor ontstaat er een spanningsverschil	tussen de verschillende zijdes van de draad. Er zijn verschillende soorten Hall sensoren, de een geeft een hoog/laag signaal als er een bepaalde waarde overschreden wordt (soort treshold). De andere sensor meet daadwerkelijk de sterkte van het magnetische veld. In het pakket zit de eenvoudige versie. 
Voor het werken met de Hall-sensor, plaats de sensor met de tekst zijde naar je toe in het breadboard. Plaats over de uiterste twee poten een 10 kΩ weerstand. Verbind de rechterzijde van de sensor met pin 2, de middelste pin met GND en de linkerzijde met 5V. Voor het programma kun je starten met analogReadSerial (en dan analogRead veranderen in digitalRead en A0 naar pin 2 wijzigen).
Een nadeel van deze wijze van uitlezen is dat je altijd bezig bent met kijken naar pin 2. Je kunt dit veranderen door gebruik maken van een interupt (pin 2 en 3 zijn daar specifiek voor op de UNO). Zodra pin 2 iets meet, wordt het programma onderbroken om een functie uit te voeren. Zie de voorbeeld sketches onderaan voor een voorbeeld.
Let op! De magneet moet aan de bedrukte zijde langs gaan voor een detectie.
Een leuk project met de Hall-sensor is gemaakt door [Rolf Hut](http://www.instructables.com/id/Longboard-With-NeoPixel-LEDStrip-Reacting-to-Speed/) 

## Playstation
Leerlingen die thuis bijvoorbeeld met een playstation spelen, moeten de knop hiernaast herkennen. De knop heeft drie mogelijkheden: links/rechts, boven/beneden, en indrukken. Daarom zijn er ook 5 pinnen (incl gnd en 5V). Het uitlezen is eenvoudig als je weet wat er in zit: een drukknop en twee keer een potentiometer. In combinatie met bijvoorbeeld een RGB kun je hier leuke projecten mee doen!

## Flow sensor
Mijn directe natuurkunde collega gebruikt de flow-sensor bij het bepalen van de wet van Darcy,  geofysica practicum voor 5V. De sensor meet het aantal rotaties per seconde, daaruit rolt een frequentie die vervolgens omgezet kan worden naar een stroomsnelheid of debiet. 

## BMP 180
De BMP 180 is een luchtdruksensor met temperatuursensor. De sensor is prima te verwerken in een weerstation of bij het bepalen van de hoogte. 

## Laser
Voor €0,40 heb je een laser geschikt voor de Arduino. In combinatie met een LDR kun je deze prima gebruiken als tripwire of om tussen twee Arduino’s te communiceren. 



```{exercise}

Wanneer je een dag weg van huis bent, wil je voor de zekerheid een inbrekersalarm hebben. Een alarm is echter duur en met de spullen die we hebben kunnen we dat ook zelf maken. Aan het alarm stellen we de volgende eisen: 
-	Het alarm moet af gaan na het detecteren van beweging of bij te veel geluid
-	Het alarm moet pas na een halve minuut afgaan, zodat je bij thuiskomst het alarm kunt uitschakelen (met een drukknop) zonder dat het alarm afgaat
-	Het alarm moet een pulserend lichtje zijn en een sirene
-	Als er geen beweging of geluid meer gedetecteerd wordt, moet het alarm stoppen
-	Een lampje moet blijven branden zodat je weet dat iemand een inbraakpoging heeft gedaan.
Het programma van eisen is opgesteld. Maak een plan om stap voor stap het alarmsysteem te bouwen, te testen en vervolgens uit te breiden. Voer het plan uit. 
```

```{exercise} Leerlingteller
Is iedereen binnen? Je telt. Mist er één, telt nog een keer. En ja, je hebt er ergens een gemist. Is het niet handiger om aan je Arduino aan te geven hoeveel leerlingen je verwacht en dat de Arduino dan bijhoudt hoeveel leerlingen je lokaal binnen komen lopen? 
Voor het bijhouden van het aantal leerlingen dat binnenkomt kun je een afstandssensor gebruiken, een laser gericht op een ldr (tip: plaats een rietje over de ldr zodat alleen het laserlicht opgevangen wordt, of een bewegingssensor. Let bij het programmeren op dat een code als 0101 twee leerlingen zijn, maar 01110 maar een leerling!
```

```{exercise} Parkeersensor
Een parkeersensor begint te piepen wanneer de afstand kleiner wordt dan 50 cm. Daarna zal de piep hoger worden of volgen de piepjes elkaar sneller op. Bij minder dan 7 cm moet de piep aanhoudend zijn.
```

```{exercise} 
In de winkel kun je nu lampen kopen die je aan en uit kunt zetten met een app op je telefoon. Die lampen zijn vaak wel duur. Gelukkig kunnen we dat ook prima zelf maken met de Arduino en een bluetooth module. Maak een lamp die je aan en uit zet met je telefoon. Breid de code uit zodat je ook de helderheid van de lamp kunt instellen met je telefoon. Start eenvoudig door te praten met je Arduino m.b.v. de seriële monitor.
```

```{exercise} Simon Says
Het spelletje Simon Says lijkt op het spelletje ik ga op reis en ik neem mee… Bij Simon Says gaan vier verschillende ledjes in een bepaalde volgorde knipperen (1234). Dezelfde volgorde moet ingedrukt worden met behulp van vier drukknoppen. Als de juiste volgorde is ingedrukt, wordt de serie verder uitgebreid (12343). Het spel gaat net zo lang door totdat de speler de foute volgorde indrukt. Het is natuurlijk het leukst wanneer de volgorde nooit hetzelfde is en dat de Arduino de volgorde voor je bepaalt.

Maak het spel!
```

```{exercise} Robotica
Veel scholen willen aan de slag met Robotica. De Arduino geeft de mogelijkheid om dit relatief goedkoop en snel te doen. Er zijn kant en klare auto’s te koop voor ongeveer €100,- maar als je de onderdelen los besteld, dan heb je de auto zelf in elkaar gezet voor ongeveer €30,-. 
We beginnen met het laten rijden van de Arduino op verschillende snelheden. Dit kun je later zelf uitbreiden door een afstandssensor te gebruiken die er voor zorgt dat de auto niet tegen een muur botst en een bluetoothmodule waarmee je de auto kunt aansturen vanaf je telefoon. Lees ook het stukje over functies programmeren! Dat is bij robotica erg handig.
```

```{exercise} Een thermometerdisplay 
Systemen die de temperatuur, luchtvochtigheid en druk kunnen geven kunnen gekocht worden in de winkel. Je kunt ze ook zelf maken. En met een kleine uitbreiding van de spullen die je al hebt, kun je dit maken. Wanneer je er een mooi kastje om heen bouwt heb je je eigen weerstation gemaakt. Begin in deze opdracht met de temperatuur te tonen op een lcd display. Breid deze uit met een knop waarmee je bijvoorbeeld de hoeveelheid licht meet en deze toont op het display.
```

```{exercise}Een digitale meetlint
Met een afstandssensor en een lcd display kun je een eenvoudige digitale meetlint maken. Altijd handig als je snel een afstand moet meten die ligt tussen de 2 cm en 3,00 m, of bij het maken van een practicum waarbij de afstand bepaald moet worden (bijvoorbeeld als functie van de tijd). Bij dit laatste is het ook handig om je data op te slaan in een array en weg te schrijven naar een SD-module.
```