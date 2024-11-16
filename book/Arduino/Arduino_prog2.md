# Programmeren deel 2
Het script *Button* is uitgebreider dan we voorheen hebben gezien. We lopen stap voor stap door het script.

```{code} C
const int buttonPin = 2;
const int ledPin = 13;
```

We hebben te maken met twee poorten waar iets moet gebeuren. Pin 2 is een invoer en pin 13 moet een uitvoer zijn. De pin verandert niet, dit is een constante (`const`). Het is een gehele waarde, een integer (`int`). We geven pin 2 een herkenbare naam, pin 2 heet nu *buttonPin*. Pin 13 heeft de naam *ledPin* gekregen.

```{code} C
int buttonState = 0;
```

We willen straks weten wat de ‘staat’ van de knop is (ingedrukt of niet). Deze kan 1 of 0 zijn. We moeten even vertellen dat we de staat van de knop willen weten (aanmaken van een variabele) en deze straks willen vergelijken. Voordat we het script laten draaien is de buttonState gelijk aan 0.

```{code} C
void setup() {
    pinMode(ledPin, OUTPUT);
    pinMode(buttonPin, INPUT);
}
```

Zoals gezegd, we moeten even vertellen dat de ledPin een `OUTPUT` is en de buttonPin een `INPUT`. Zo, dat weten ze nu dan ook…

```{code} C
void loop() {
buttonState = digitalRead(buttonPin);
    if (buttonState == HIGH) {
        digitalWrite(ledPin, HIGH);
    }
    else {
    digitalWrite(ledPin, LOW);
    }
}
```
Er moet iets gebeuren als de knop wordt ingedrukt. Aan het begin van de loop wordt de knop uitgelezen (eigenlijk wordt er alleen gecontroleerd of er een 5,0 V spanning over de weerstand staat). Daarna volgt een if-statement. Als (`if`) de knop is ingedrukt (`buttonState == HIGH`) dan moet de LED gaan branden (`digitalWrite(ledPin, HIGH);`). In alle andere gevallen (else), moet de LED niet branden (`digitalWrite(ledPin, LOW);`).

```{code} C
void loop() {
buttonState = digitalRead(buttonPin);
    if (buttonState == HIGH && state == LOW){
    state2 = HIGH;
    }
    if (buttonState == HIGH && state == HIGH){
    state2 = LOW;
    }
state = state2;
digitalWrite(ledPin,state);
delay (100);
}
```
Het is een makkelijk if-statement. Je kunt ook meerdere voorwaarden stellen. Als je twee knoppen tegelijk in moet drukken voordat de LED gaat branden zet je && tussen de tekens (`if buttonState1 == HIGH && buttonState 2 == HIGH){}`). Je kunt ook het teken `||` gebruiken. Dan moet of de ene voorwaarde gelden of de andere. 

Helaas blijft het lampje nu nog niet branden als je de knop hebt ingedrukt. Je kunt er wel zelf voor zorgen dat je met één knop het lampje aan en uit kan zetten. Vergeet niet de nieuwe variabele (`int`) te definiëren aan het begin! Er zijn nog eenvoudigere manieren, deze zijn alleen getoond als script. Leg uit hoe ze werken!

```{code} C
if(buttonState == HIGH){ i++;}
digitalWrite(ledPin,i%2);
```

```{code} C
digitalWrite(13,!digitalRead(13));
```

```{exercise} Het beveiligen van een kluis

De kluis van de bank is beveiligd. De kluis gaat pas open (de LED brandt pas) als er twee sleutels worden omgedraaid (knoppen ingedrukt). Een sleutelgat bevindt zich op de kamer van de directeur, de andere zit naast de kluis.

Bouw de bijbehorende schakeling en programmeer het script zodanig dat de kluis pas open gaat als beide sleutels tegelijk worden omgedraaid.
```

```{exercise} Een wisselschakeling

Als je onderaan de trap staat wil je het licht bovenaan de trap aan zetten. Bovenaan de trap zit nog een lichtknop. Daarmee kan je het licht weer uit of aan zetten. Bouw de schakeling met twee knoppen en schrijf het programma zodat je een werkende  wisselschakeling hebt. Lukt dit niet meteen? Probeer het dan eerst met een enkele knop.
```

```{exercise} Een voetgangersoversteekplaats**

Voor voetgangers is een speciale overgangsplek gemaakt. Deze plek ligt aan een drukke weg. Als er geen voetgangers zijn, staat het verkeerslicht voor de auto’s op groen. Op het moment dat een voetganger over wil steken, drukt deze op de knop. Het verkeerslicht voor de auto’s gaat dan van groen naar geel naar rood. Voetgangers hebben dan 15 seconde om over te steken. Het verkeerslicht voor hen staat op groen! Dan gaat het groene lampje vijf keer knipperen en springt op rood. Een seconde later springt het verkeerslicht voor de auto’s weer op groen.

Maak dit systeem.
```