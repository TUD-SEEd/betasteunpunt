# Arduino Basics

**Opdracht 1: Het aansluiten van een LED**

Een LED is een diode die licht uitzendt als er stroom door de LED gaat. De LED laat stroom maar door in één richting. De lange poot van de LED moet altijd op de + kant aangesloten worden, de korte poot op de – kant, zie onderstaand figuur.

De stroom door een LED mag meestal maar 20 mA zijn. De spanning over de LED is dan ongeveer 2,0V, deze waardes verschillen een beetje per soort LED, zie onderstaande tabel. De Arduino levert een 5,0 V spanning. De LED moet dus in serie geschakeld worden met een weerstand. De weerstand moet dus minimaal 150 Ω zijn ($R = U / I = 3,0 / 0,020 = 150 Ω$). 

a) Er is geen weerstand aanwezig van 150 Ω maar wel een van 220 Ω. Zoek de weerstand op met behulp van de kleurcode: de eerste ring moet rood zijn, de tweede ring ook en de derde ring bruin (22·10). Een andere mogelijkheid is rood, rood, zwart, zwart.

b) Sluit nu de 5V uitgang van de Arduino aan op de + kolom en de GND (ground) uitgang van de Arduino aan op de – kolom. 

c) Sluit de LED en de weerstand in serie aan, zie de tekening.

d) Verbind de Arduino via de usb met de computer. Als je het goed hebt gedaan brandt
de LED!

Doordat de rode led bij lagere spanning licht uit zendt dan bijvoorbeeld een groene led, kun je een kleinere weerstand bij groene en blauwe led’s gebruiken. Zo branden ze uiteindelijk toch nog even fel!


** Opdracht 2 Een knipperende LED** 

Nu kun je je led wel laten branden, maar daar heb je nog niet veel aan… Een volgende stap is de LED aansturen met behulp van een stukje code. Om de LED aan te sturen met behulp van code moet je een uitvoerpoort (bijvoorbeeld pin 13) van de Arduino verbinden met je LED. De 5V output heb je nu niet nodig, pin 13 levert nu de spanning. In de tekening zie je dat deze wel verbonden is, bij grotere projecten vergeet je snel de 5V, vandaar!

a) Bouw de opstelling die je ziet in de tekening en sluit de Arduino aan op de computer. We willen de Arduino aansturen, daarvoor gebruiken we het Arduino programma.

b) Open het programma en open het script blink via: bestand/voorbeelden/basis/blink.

c) Controleer het script met het vinkje. Mocht het programma niet werken, dan geeft het onderaan een foutmelding weer (het kan zijn dat je de COM-poort moet toewijzen, dit doe je via hulpmiddelen/poort).

d) Upload het script naar je Arduino met het tekentje . (snelcode: ctrl + u)

e) Beschrijf kort wat je ziet. Probeer wat je ziet te verklaren met behulp van de code.

f) Verander het script zodat de LED sneller knippert.

g) Sluit drie verschillende LED lampjes aan, verander het script zodat ze om de beurt aan staan.

h) Verander het script en maak een verkeerslicht waarbij oranje maar even aan staat.