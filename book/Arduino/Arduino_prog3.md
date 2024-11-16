# Programmeren deel 3
De Arduino kan niet alle waarden uitlezen. De ANALOG IN heeft een 10 bits chip. Dit betekent dat er 210 = 1024 waarden doorgegeven kunnen worden. Het is alsof je de 5,0 V in 1024 - 1 kleine blokjes verdeelt. De waarde die je uitleest bij opdracht 8 is dus ook niet de spanning zelf, maar het getal dat bij een spanning hoort. Het getal 223 hoort dus bij: 223 / 1023 · 5,0 = 1,09 V. De PWM (~) is een 8 bits systeem en kan dus 28 = 256 waarden geven. Oei… zie je het probleem? We kunnen lezen met 1023 verschillende waardes maar schrijven kan maar met 255 waardes…. Gelukkig is er een code die zorgt voor automatische schalen (map).

```{code} C
void loop() {
    sensorValue = analogRead(sensorPin);
    brightness = map(sensorValue,500,900,255,0);
    Serial.println(sensorValue);
    delay(10);
    analogWrite(ledPin,brightness);
}
```

De functie map wil 5 getallen hebben. Het eerste getal is de waarde die de analoge poort uitleest. Het tweede getal is het laagste getal dat uitgelezen kan worden, het derde getal de grootste waarde die uitgelezen kan worden. Dit hoeven niet per se 0 en 1023 te zijn, de waarde verkrijg je bij het ijken van je sensor. De gevoeligheid van je sensor kan dus ook zitten tussen 500 en 900, zie wederom grafiek 2 uit programmeren deel 3. Het vierde en vijfde getal geven het bereik van de output weer. In het voorbeeld moet een input waarde van 500 een output waarde worden van 255. Een input waarde van 900 moet een output waarde van 0 worden.

Een functie die ook handig is, is de functie ++. Elke keer als de loop de volgende cyclus ingaat, wordt de waarde met 1 verhoogd. Zo kun je bijvoorbeeld eenvoudig  bijhouden hoeveel loops (iteraties) er al zijn geweest. Ook is het mogelijk om op die manier elke keer een andere pin aan te sturen of later een frequentie te veranderen.

Als ++ bestaat, dan zal -- ook wel bestaan. En dat klopt. -- zorgt ervoor dat de waarde met 1 wordt verlaagd. Beide codes kunnen in een for-loop geplaatst worden. Dit is een loop binnen de loop. Kijk eens naar het voorbeeld waarbij er een soort aftel mechanisme in zit voordat het programma zelf begint… (let op, de variabele i moet je nog wel even declareren voor de setup!

**Opdracht 10 Sneller programmeren**

Herschrijf opdracht 2h met de functie ++.

**Opdracht 11 Alarmschakelaar**
Onder de kassa van een winkel zit een schakelaar (drukknop), als deze wordt ingedrukt dan moet er een pulserend alarmbel (ditmaal nog een LED) gaan. Maak dit systeem.

**Opdracht 12 Een RGB LED**
Een RGB LED heeft vier pootjes. In de LED zitten eigenlijk drie LED’s verwerkt. Door de drie LED’s met behulp van een PWM (~) aan te sturen kun je kleuren mengen en zo tussenliggende kleuren krijgen. Nu kunnen we via de software de sterkte van elke kleur bepalen, maar het zou leuk zijn wanneer we ook handmatig de kleuren kunnen instellen. We gebruiken hiervoor variabele weerstanden ook wel potmeters genaamd.

De potmeter heeft drie poten. Eentje voor de 5,0 V in, eentje voor de aarde (0,0 V) en een poot voor het uitlezen van de meter met behulp van een analoge pin, zie ook de figuur hiernaast.

Als je de draaiknop van de potmeter draait, verandert de weerstand, dit verandert dus ook de waarde van de spanning die je uit leest. Een potmeter is dus eigenlijk een spanningsdeler.

a) Bouw de schakeling.

b) Schrijf de bijbehorende code waarbij je eerst de waarde van de potmeter uitleest en vervolgens de RGB LED aanstuurt.

c) Probeer de verschillende standen van de RGB Led en controleer of het plaatje hieronder goed overeenkomt met de kleuren van de LED.

**Opdracht 13 De snelheid van een elektromotor**
Een elektromotor zorgt ervoor dat van elektrische energie bewegingsenergie gemaakt wordt. Een elektromotor vind je in alle apparaten die bewegen en werken op elektriciteit. De snelheid van een elektromotor is afhankelijk van de spanning over de motor. We werken in deze les dus met de PWM pin (~). We kunnen natuurlijk direct de snelheid van de elektromotor in ons script zetten, maar het zou handiger zijn wanneer we de snelheid van de elektromotor kunnen aanpassen, bijvoorbeeld met behulp van een draaiknop. We gaan gebruik maken van een variabele weerstand, ook wel een potmeter genoemd.

a) Bouw de rechterzijde van de schakeling met de potmeter. De elektromotor hoef je nog niet aan te sluiten.

b) Leg uit waarom de signal out van de potmeter naar een ANALOG IN moet.

c) Leg uit waarom de diode is opgenomen in de schakeling.

d) Programmeer het bijbehorende script zodat de snelheid van draaien van de elektromotor ingesteld kan worden met behulp van de potmeter. Gebruik daarbij de map functie.