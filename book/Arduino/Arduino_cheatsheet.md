# Cheatsheet

Functies
Er is een gigantische lijst met functies. Hier de veelgebruikte functies in Arduino.
int waarde tussen -32768 en 32767 (215)
long waarde tussen -2.147.483.648 en 2.147.483.647 (231)
unsigned long/ unsigned int waardes zijn alleen positief
char karakters opgeslagen via het ASCII systeem
float zijn decimale waardes, maar wordt zoveel mogelijk omzeild in
Arduino programmeertaal
digitalWrite(pin,waarde); schrijft geen spanning (LOW) of een spanning van 5 V naar de pin.
analogWrite(pin,waarde) schrijft met een 8 bit output waardes tussen 0 en 5 V. De
aangegeven waarde moet tussen 0 en 255 liggen.
digitalRead(pin) leest of er een spanning op de pin staat, geeft een 0 of 1 terug.
analogRead(pin) leest hoeveel spanning op de pin staat, geeft een waarde tussen 0
en 1023 terug.
map(W,Min1,Max1,Min2,Max2) Is een schaalfunctie. Converteert een waarde (W) die ligt
tussen Min1 en Max1 naar een waarde die ligt tussen Min2
en Max2.
if(voorwaarde){} Als er voldaan wordt aan de gestelde voorwaarde, wordt de code
tussen de accolades uitgevoerd.
while(voorwaarde){} Zolang er aan de voorwaarde voldaan wordt, wordt de code tussen
de accolades uitgevoerd.
for(SW;EW;VF){} Een for-loop voert de code tussen de accolades een aantal keer uit.
SW is de startwaarde, EW de eindwaarde en VF de
verhogingsfactor. Vb: for(int i = 0; i<20;i++){delay(100);}
switch case switch case is een soort keuzemenu waarbij een stukje code
uitgevoerd kan worden. Als de variabele waarde een heeft dan
voert deze de code uit behorende bij case 1.
&& Beide voorwaardes moeten gelden
|| Een van de twee voorwaardes moet
gelden
!= Is ongelijk aan.
Tone(pin,f,t); Kan specifieke frequentie
produceren. In de toon moet
aangegeven worden op welke pin
de luidspreker zit, welke frequentie
gemaakt moet worden en eventueel
hoe lang de toon aangehouden moet
worden. Het is niet noodzakelijk
aan te geven hoe lang de toon
aangehouden moet worden.
noTone(pin); Stopt de toon die geproduceerd werd.
switch (var) {
case 1:
//doe iets als var is 1
break;
case 2:
//doe iets als var is 2
break;
default:
// als geen van
bovenstaande waar is, doe het
volgende (optioneel)
break;
}
21
millis(); Dit kan dienen als een timer. millis(); geeft het aantal milliseconde
dat de Arduino aan staat weer.
micros(); Geeft het aantal microseconde weer dat de Arduino aan staat. De
resolutie is 4 μs.
delay(); Wacht een aantal milliseconde voor het uitvoeren van het volgende stukje
code.
random(LW,HW) Random geeft een getal terug tussen de laagste waarde (LW) en hoogste
waarde (HW). Een nadeel van random is dat bij het opnieuw starten van
de Arduino dezelfde sequentie wordt afgespeeld. Random is dus niet
random… Dit probleem kan wel opgelost worden door eerst gebruik te
maken van de functie randomSeed(A0); Deze leest pin A0 uit. Als daar
niets is verbonden wordt hier ruis gemeten. randomSeed schudt als het
ware de vaste sequentie van Random door elkaar.