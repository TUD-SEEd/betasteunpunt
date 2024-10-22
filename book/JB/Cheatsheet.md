# Cheatsheet

## Headings

`# Chapter`

`## Section`

`### Subsection`

## Figuren
````
    ```{figure} <figurename>.png/.jpg
    ---
    height/width: <height or width in percentage>
    name: <name of figure's label>
    align: left / center / right
    figclass: left blank or "margin"
    ---
    <Figure caption>
    ```
````

## YT Video
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

**Machten**
`^ tot de macht`
Bijv:
`e^{2x}`
geeft:

$$e^{2x}$$

**Breuk**
`\frac{}{}`
bijv. 
`\frac{2}{3}`
geeft:

$$\frac{2}{3}$$

**Symbolen**
|||
|---|---|
|`\sqrt`|$\sqrt$|


Uitgebreider: https://en.wikibooks.org/wiki/LaTeX/Mathematics

## Tabellen


## Referenties

`[tekst](url)`

## Admonitions

iets over admonitions

warning
tip
danger
note
...

```{warning}
Dit is een waarschuwing!
```

```{tip}
:class: dropdown
Je kunt een dropdown class toevoegen `:class: dropdown`. 
```


## Exercise
iets over exercise en solutions

````
    ```{exercise}
    Hier is een mooie opdracht voor je
    ```
````

resulteert in:
 ```{exercise}
Hier is een mooie opdracht voor je
```