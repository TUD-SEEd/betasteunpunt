# Arduino elektronica deel 2

Een elektromotor kan veel stroom vragen. De Arduino is slecht in het leveren van veel stroom. Om toch grote stroomvragers te voorzien van de benodigde stroom kun je gebruik maken van een externe spanningsbron zoals een batterij. Dan heb je nog wel een transistor nodig zodat je de grootte van de stroom kunt regelen en je de snelheid van draaien van de elektromotor kunt aanpassen.

De transistor (hier gebruiken we alleen een zogenaamde NPN-transistor) heeft drie pootjes, zie de foto. Links zit de emitter, in het midden de base en aan de rechterzijde de collector. (LET OP! Bij verschillende transistors wordt de volgende omgedraaid, wij hebben de 2N222 transistor). Ten alle tijden wordt aan de collector de externe voeding (+ zijde) verbonden. Spanning over de base bepaalt of er stroom gaat lopen naar de emitter. Daarmee is een transistor een soort van kraan: de hoeveelheid spanning bij de  base bepaalt de hoeveelheid doorgelaten stroom. De base moet daarom aangestuurd worden met een PWM pin als je de snelheid wilt regelen.

Bij erg grote stroomsterktes moet je een grotere transistor gebruiken of eentje met een koelelement zodat de transistor z’n warmte kwijt kan.

**Opdracht 14 De snelheid van een elektromotor deel 2**

De schakeling van opdracht 13 is te eenvoudig en het kan goed zijn dat de Arduino te weinig stroom levert. Zeker wanneer je de DC motor snel wilt laten draaien.

a) Bouw de schakeling zoals hiernaast weergegeven.
b) Gebruik het script van opdracht 12 en upload het programma. Kan de elektromotor daadwerkelijk harder draaien?