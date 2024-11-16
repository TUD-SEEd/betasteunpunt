# Programmeren deel 1
Arduino heeft een eigen programma
dat gebaseerd is op C++. Heb je al
ervaring met programmeren en/
of met C++ (of java), dan is het
programmeren heel makkelijk. Heb
je geen ervaring met programmeren?
Het is veel minder moeilijk dan je
misschien wel denkt!
Bovenaan het script Blink staat
/* dit betekent dat alles na dit
beginteken en voor het afsluitteken
*/ commentaar is. Hier zet je neer
hoe het programma heet, wat het
doet, wie het gemaakt heeft en
wanneer je het voor het laatst hebt
veranderd.
Een tweede mogelijkheid om commentaar toe te voegen is met
behulp van //. Alles op dezelfde regel na // is commentaar. Zo kun
je bijhouden wat de code op die regel doet. Met behulp van de
snel code ctrl / kun je code snel omzetten naar commentaar.
Voordat de belangrijkste code wordt uitgevoerd moet je zeggen
wat er precies aangestuurd wordt. We geven aan dat in pin 13 iets
zit en dat de Arduino daar een output (spanning) geeft als jij dat
wilt. Iets netter zou zijn om nog voor de setup aan te geven hoe
pin 13 heet: je geeft de pin een naam (int LEDrood = 13;). Wil je
pin 13 vervolgens aansturen, dan kan je dat doen met de naam
LEDrood.
Alles wat tussen de accolades {} van de loop staat wordt continu herhaald. Eerst wordt pin 13 hoog
(5,0 V) gemaakt met behulp van de code digitalWrite (digitalWrite kan alleen aan of uit). Daarna
moet het programma 1000 ms wachten (delay) voordat de volgende regel code wordt uitgevoerd.
De volgende regel code maakt pin 13 weer laag (0,0 V).
De pin wordt aangestuurd met een hoog of met een laag
signaal. Zit daar nog iets tussen? Ja en nee… De output is
altijd 0,0 V of 5,0 V. Maar je kunt de LED wel dimmen door
maar een bepaalde tijd de LED aan te zetten. Als de LED
snel genoeg knippert zie je niet dat de LED knippert, het
lijkt er alleen op dat de LED minder fel brandt. Wanneer
je een LED wilt dimmen gebruik je een output met het
symbool ~. Dit is een Puls Width Modulation (PWM). De
waarde van de PWM zit tussen de 0 (geheel uit) en 255
(geheel aan).