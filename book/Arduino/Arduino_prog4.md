# Programmeren deel 4

Voor het aansturen van sommige apparaten zijn al scripts geschreven waardoor het aansturen van de apparaten eenvoudiger gaat. Een van die apparaten is een servo motor. Een servo motor is een soort elektromotor die 180o kan draaien. De rotatiehoek kan nauwkeurig ingesteld worden doordat deze werkt met een ingebouwde potmeter. Om gebruik te maken van een servo hebben we het volgende script nodig. 

Eerst wordt het script uit de bibliotheek opgehaald. Daarna noemen we de servo mijnServo en krijgt deze de begin positie 0.

Met mijnServo.attach(9) zeggen we dat de servo verbonden is met pin 9. Uiteraard is dit weer een PWM poort. Nu is het mogelijk de servo te sturen. Waarbij pos staat voor de positie, die kan tussen 0 en 180 zitten. De code voor het sturen van deze servo wordt dan: mijnServo.write(pos); Een servo motor kan niet helemaal rond draaien zoals een gewone elektromotor maar we kunnen wel heel goed richten met een servomotor. Dit komt omdat er in de Servo een potmeter zit, de sturing gaat dus via het uitlezen van de spanning!


```{exercise} Een lichtwijzer
Gebruik opdracht 8 als basis. Vervang daarin de LED door de servo motor. Je kunt op de servo een wijzer plakken en een schaalverdeling maken zodat de wijzer aangeeft hoe licht/donker het is. 
```

```{exercise} Zo veel mogelijk zonlicht

Zonnepanelen worden neer gezet om stralingsenergie, afkomstig van de zon zon, om te zetten in elektrische energie. De panelen vangen het meeste licht op als ze loodrecht op de zon staan. De aarde draait en we zouden de panelen mee moeten laten draaien om zoveel mogelijk energie op te vangen. Dat gaan we in deze opdracht doen.

Op een groot veld staan alle zonnepanelen opgesteld zoals zonnepaneel 1. Zonnepaneel 2 en 3 staan beide een beetje gedraaid ten opzichte van paneel 1. Je kunt nu goed zien dat de zonnepanelen de meeste elektrische energie produceren als zonnepaneel 2 en 3 even veel elektrische energie produceren. Paneel 2 vangt nu meer lichtstralen op dan paneel 3. Het hele systeem zou dus linksom gedraaid moeten worden.

In plaats van een zonnecel beginnen we met een LDR.

a) Bouw de schakeling en programmeer het eerste stuk waarbij je de waarden van de LDR kan uitlezen.

b) Zet de flitser van je telefoon aan en lees met behulp van `Serial.println(LDR1);` de waarden van LDR1 en LDR2 uit. Beweeg je telefoon van links naar rechts en bekijk hoe de waarden variëren.

c) Schrijf nu het stukje code voor de servo. Laat de servo naar links draaien als LDR1 meer licht ontvangt dan LDR2 en andersom. Denk eraan dat de servo gebruik maakt van een  potmeter en je dus ook gebruik kan maken van de map functie.

d) Leg uit dat al aardig in de buurt komt van het draaien van de zonnepanelen.
```