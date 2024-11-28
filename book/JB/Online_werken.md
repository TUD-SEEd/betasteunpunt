# Je eerste aanpassingen via GitHUB

Zoals in het vorige hoofdstuk uitgelegd, je bestanden staan op GitHub en het template zorgt ervoor dat het boek gebouwd wordt. Je kunt online, in GitHub, direct wijzigingen aanbrengen aan de bestanden, en nieuwe bestanden aanmaken of uploaden. 

In het template boek zijn al een aantal bestanden aanwezig. De folderstructuur zie je weergegeven in {numref}`Figuur {number} <fig_templatecontent>`.

``` {figure} figures/templatecontent.PNG
---
width: 80%
name: fig_templatecontent
---
De folderstructuur in het templateboek.
```

We gaan nu aan de slag met een kleine aanpassing aan een van de bestanden om vervolgens te kijken naar het resultaat van die wijziging.

````{exercise} Je eerste aanpassing
Navigeer naar het bestand `book/some_content/overview.md`. Klik dan op de pen aan de rechterkant (edit this file).

Verander de tekst na de `#`. Dit is de titel van het bestand.

``` {figure} figures/eersteedit.gif
```

Breng eventueel andere wijzigingen aan in de teksteditor en als je klaar bent, commit je je wijzigingen naar de "remote repository" door op de groene `Commit changes` knop te klikken.

Het boek wordt nu opnieuw gebouwd. Als dat klaar is, kun je het resultaat op de GitHub page bekijken.
````

```{admonition} Samenvatting bij commit
:class: dropdown
Werk je met meerdere mensen in GitHub, of zelf aan een groot project. Dan is het verstandig om de commit een herkenbare titel (commit message) te geven en eventueel een samenvatting (extended description) toe te voegen wat er precies gewijzigd is. Zo kun je eventuele fouten vroegtijdig opsporen en te niet doen. Ook kun je uitleggen waarom bepaalde aanpassingen gedaan zijn.
```

## Toevoegen van een figuur

Een figuur zegt soms meer dan 1000 woorden... 

![Externe afbeelding](https://polslab.tnw.tudelft.nl/figures/training.JPG)

Als we een figuur in ons boek willen toevoegen, dan kunnen we verwijzen naar een andere website (zoals in bovenstaande figuur). Dat brengt wel het risico met zich mee dat deze figuur niet meer zichtbaar is als de figuur van locatie verhuist. Het is dus beter dat het figuur zich in een eigen bron bestand is. 

We moeten dus eerst een figuur uploaden naar GitHub en vervolgens in onze file verwijzen naar die figuur. (Let op! Later wordt dit veel makkelijker.)

`````{exercise}
Op GitHub, onder het kopje `code`...

1. Navigeer naar book/figures en klik op `add file` {fa}`right-long` `Upload files`. 
```` {figure} figures/incl_fig.PNG
---
width: 50%
---
add bestand in de folder
````
2. Kies de figuur die je toe wilt voegen (onthoud de naam van de file!).
3. Commit je veranderingen naar github (het bestand wordt geüpload)
4. Navigeer naar book en open `intro.md` en druk op `edit this file`.
5. Kopieer de code hieronder naar die file, pas de naam van het figuur aan naar de naam van je eigen figuur.

````{code}
``` {figure} figures/incl_fig.PNG
---
width: 50%
name: fig_mijneerstefiguur
---
add bestand in de folder
```
````

6. Commit je verandering en bekijk het resultaat op GitHub pages.

`````

```{warning}
De code is hoofdletter gevoelig. Het maakt dus uit of je extensie .png is of .PNG
```

```{tip}
We hebben een pagina met alle belangrijke [codes](./Cheatsheet.md).

Nog meer informatie over de opties bij figuren vind je [hier](https://teachbooks.io/manual/basic-features/figures.html).
```

Je kunt figuren op verschillende plaatsen positioneren (links / midden / rechts /kantlijn), de grootte aanpassen, van een onderschrift voorzien etc. Raadpleeg bovenstaande documentatie en probeer de verschillende settings.

## Je favoriete vergelijking

```{exercise} Een vergelijking toevoegen
Kijk eens op de [Cheatsheet pagina](./Cheatsheet.md) hoe je een formule toevoegt en probeer dat eens...
```

## En andere aanpassingen

```{exercise} Andere aanpassingen
Probeer eens wat andere aanpassingen te maken, bijvoorbeeld door de structuur van de pagina verder uit te werken in secties en subsecties, elk met wat tekst. Bekijk het resultaat.
```
