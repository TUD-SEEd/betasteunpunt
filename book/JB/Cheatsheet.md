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

tekst.

`$$ Vergelijking $$`

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


## Referenties

`[tekst](url)`

## Admonitions

iets over admonitions

warning
tip
danger
note
...

## exercise
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