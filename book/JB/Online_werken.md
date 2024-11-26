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

````{exercise} De eerste aanpassing
Navigeer naar het bestand `book/some_content/overview.md`. Klik dan op de pen aan de rechterkant (edit this file).

Verander de tekst na de `#`. Dit is de titel van het bestand.

``` {figure} figures/eersteedit.gif
```

Breng eventueel andere wijzigingen aan in de teksteditor en als je klaar bent, commit je je wijzigingen naar de "remote repository" door op de groene `Commit changes` knop te klikken.

Het boek wordt nu opnieuw gebouwd. Als dat klaar is, kun je het resultaat op de GitHub page bekijken.
````

```{note} Summary
:class: dropdown
Werk je met meerdere mensen in GitHub, of zelf aan een groot project. Dan is het verstandig om de commit een herkenbare titel te geven en eventueel een samenvatting toe te voegen wat er precies gewijzigd is. Zo kun je eventuele fouten vroegtijdig opsporen en te niet doen. Ook kun je uitleggen waarom bepaalde aanpassingen gedaan zijn.
```

## Toevoegen van een figuur

Een figuur zegt soms meer dan 1000 woorden... 

![Externe afbeelding](https://polslab.tnw.tudelft.nl/figures/training.JPG)

Als we een figuur in ons boek willen toevoegen, dan kunnen we verwijzen naar een andere website (zoals in bovenstaande figuur). Dat brengt wel het risico met zich mee dat deze figuur niet meer zichtbaar is als de figuur van locatie verhuist. Het is dus beter dat het figuur zich in een eigen bron bestand is. 

We moeten dus eerst een figuur uploaden naar GitHub en vervolgens in onze file verwijzen naar die figuur. (Let op! Later wordt dit veel makkelijker.)

````{exercise}
**1 add file in de map**

``` {figure} figures/incl_fig.PNG
---
width: 50%
---
add bestand in folder
```

**2 toevoegen van figuur in de .md file**

**3 aanpassen van width, toevoegen van label**
```{tip}
We hebben een pagina met alle belangrijke [codes](./Cheatsheet.md).

Nog meer informatie over de opties bij figuren vind je [hier](https://teachbooks.io/manual/basic-features/figures.html).
```
````

**Iets meer uitleg over figuur en verwijzen naar figuur**



