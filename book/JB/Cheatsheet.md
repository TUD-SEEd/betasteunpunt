# Cheatsheet
Hier een aantal standaard codes als referentie.

## Headings
Onderscheid in titels voor chapters `# Chapter`, secties `## Section` en subsecties`### Subsection`. Je kunt deze delen van een label `(sec-YT)= ## YT video` voorzien en er naar verwijzen, zoals naar het interessant deel over [Youtube Videos.](sec-YT)

## Figuren
Aanmaken van een figuur, met label (name)
````
    ```{figure} <figurename>.png/.jpg
    ---
    width: <breedte in percentage>
    name: <label van de figuur>
    align: left / center / right
    figclass: left blank of <margin>
    ---
    <Figure caption>
    ```
````
(sec-YT)=
## YT Video
Gebruik bij het embedden van YT video de insluitingslink van YT.

````
    <div style="display: flex; justify-content: center;">
        <div style="position: relative; width: 70%; height: 0; padding-bottom: 56.25%;">
            <iframe
                src="https://www.youtube.com/embed/YDBr1Lof_mI?si=RhTC31XHv-6gL4Kl"
                style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
                frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
            ></iframe>
        </div>
    </div>
````

## Vergelijkingen

Voor de betavakken zijn wiskundige vergelijkingen essentieel. Ook in JB's kun je vergelijkingen opnemen. Wat in LaTeX kan, kan in JB ook, bijv:

$$ F_{res} = m \cdot a$$ (eq:Newton)

Waarbij gelabelde vergelijkingen, zoals {eq}`eq:Newton` naar verwezen kan worden. 

`$$ Vergelijking $$`

Maar je kunt ook inline vergelijkingen opnemen zoals deze: $s=v_{gem}t$. Daarbij gebruik je een enkele dollar teken voor en na je `$ Vergelijking $`


|Naam|Script|Symbolen|
|---|---|---|
|wortel|`\sqrt{4}`|$\sqrt{4}$|
|macht|`^{2x}`|$^{2x}$|
|breuk|`\frac{2}{3}`|$\frac{2}{3}$|
|subscript|`_{gem}`|$_{gem}$
|superscript|`^{N}`|$^{N}$|
|vermenigvuldig|`\cdot`|$\cdot$|

Met wat voorbeelden:
|Naam|Script|Symbolen|
|---|---|---|
|Afgeleide|`\frac{\Delta f}{\Delta t}`|$\frac{\Delta f}{\Delta t}$|
|Integraal|`\int_a^b dx`|$\int_a^b dx$|
|sinus|`sin(x)`|$sin(x)$|

Uitgebreider: https://en.wikibooks.org/wiki/LaTeX/Mathematics

## Tabellen

Tabellen worden gemaakt met scheidingsteken `|`
Bijvoorbeeld:
```
|Kop 1|Kop 2|Kop3|
|---|---|---|
|tekst 1|tekst 2|tekst 3|
|tekst 4|tekst 5|tekst 6|
```

Met als output:
|Kop 1|Kop 2|Kop3|
|---|---|---|
|tekst 1|tekst 2|tekst 3|
|tekst 4|tekst 5|tekst 6|

Of via ...
````
    ```{list-table} Overzicht van sancties bij bepaald gedrag
    :header-rows: 1
    :name: sancties
    * - Gedrag
      - Sanctie bij 1e keer
      - Sanctie bij 2e keer
    * - Niet (tijdig of met een geldige reden) afgemeld 
      - Een penalty                                       
      - uitsluiting              
    ``` 
````

Met als output:
```{list-table} Overzicht van sancties bij bepaald gedrag
:header-rows: 1
:name: tb_sancties
* - Gedrag
  - Sanctie bij 1e keer
  - Sanctie bij 2e keer
* - Niet (tijdig of met een geldige reden) afgemeld 
  - Een penalty                                       
  - uitsluiting              
``` 

Methode 2 heeft als voordeel de mogelijkheid tot refereren naar {numref}`Tabel {number} <tb_sancties>`

## Referenties
Hier kun je een [link](https://nos.nl) kwijt met: `[tekst](url)`

Of de verwijzing naar vergelijking {eq}`eq:Newton` met ``` {eq}`label vergelijking` ```

Of naar een tabel zoals {numref}`Tabel {number} <tb_sancties>` met ``` {numref}`Tabel {number} <tabel label>` ```

Of naar een figuur zoals {numref}`Figuur {number} <figuur>` met ``` {numref}`Figuur {number} <figuur>` ```

## Admonitions
Er zijn een paar voorgeprogrammeerde blokken. Dit zijn: 

* warning
* tip
* danger
* note
* admonition 
* important

```{warning}
Dit is een waarschuwing!
```

Of:
````
    ```{tip}
    :class: dropdown
    Je kunt een dropdown class toevoegen `:class: dropdown`. 
    ```
````

resulterend in:

```{tip}
:class: dropdown
Je kunt een dropdown class toevoegen `:class: dropdown`. 
```
**Exercise**
Een speciale admonition is de exercise, deze nummert automatisch. Als je een label toevoegt kun je ook een solution maken die daaraan koppelt:

````
    ```{exercise} Vermenigvuldiging
    :label: ex_kleine_opdracht
    Wat is 4x2?
    ```
````

resulterend in:
 ```{exercise} Vermenigvuldiging
:label: ex_kleine_opdracht
Wat is 4x2?
```

en het antwoord:

````
    ```{solution} ex_kleine_opdracht
    :class: dropdown
    4x2 = 8
    ```
````

resulterend in:
 ```{solution} ex_kleine_opdracht
:class: dropdown
4x2 = 8
```

```{note}
Om gebruik te maken van exercise moet:
- In je requirement.txt file staan: sphinx-exercise
- In je _config file staan:\
    extra_extensions:\
        - sphinx_exercise

```