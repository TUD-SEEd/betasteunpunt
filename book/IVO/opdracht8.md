# Statistiek PO

## Afstand en prijs
In je dataset heb je de breedte- en lengtegraad van de airbnb's gekregen. We kunnen de lengte- en breedtegraad gebruiken om de afstand tot aan het centrum van New York te berekenen. De formule is: 

$$ d = \sqrt{(\text{breedtegraad}-420778)^2 + (\text{lengtegraad}+700327)^2}$$ (eq:Afstand)

Vergelijking {eq}`eq:Afstand` geeft de afstand van een airbnb tot aan het centrum van New York weer in meters.

### Correlatie

```{Theorie A: Spreidingsgrafiek}
Door een spreidingsgrafiek te maken van de prijs en de afstand kunnen we zien of er een verband tussen deze variabelen is. 
Een spreidingsgrafiek kun je google sheets maken door de kolommen van afstand en prijs te selecteren en daarna naar diagram te gaan en te klikken op spreidingsgrafiek.
```

```{Waarschuwing}
Sommige delen van de dataset hebben een foute breedtegraad of lengtegraad. Alle afstanden groter dan 30 000 ligt buiten New York en wil je niet in je spreidingsgrafiek hebben. 
```

```{excercise}
:label: ex_1

Maak een spreidingsgrafiek van de afstand en prijs van de airbnb's met de afstand op de horizontale as en de prijs op de verticale as. Stel de punten in op 2pxt en voeg een rode trend lijn toe. 
```
```{excercise}
: label: ex_2
Wat kunnen we zeggen over de prijs van de airbnb's met respect tot de afstand tot het centrum?
Leg uit aan de hand van je spreidingsgrafiek van ex_1.
