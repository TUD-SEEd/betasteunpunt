# Aan de slag

We gaan er vanuit dat je een [Github](../Software/Github.md) account hebt (aangemaakt). Die heb je nu nodig...

## Maken van eigen template boek
Volg de volgende stappen uit deze animatie, hieronder stapsgewijs uitgewerkt:
``` {figure} ../figures/teachbooks-template.gif
```

1. Ga naar deze [repository](https://github.com/TeachBooks/template)
2. Klik op de groene `use this template` en klik `create a new repository`.
3. Kies de naam voor je repository, en kies voor de optie `public`.
4. In je repository, klik links op pages en kies voor `Github actions`
``` {figure} ../figures/set_up_pages.png
```
5. Klik op `code` en klik op het tandwiel (bij **About**) aan de rechterkant van het scherm. 
6. Vink **Use your GitHub Pages website** aan.
7. Ga naar actions in het bovenste menu, klik op de (rode) `inital commit` en klik op `re-run all jobs`

Het boek wordt nu nog een keer aangemaakt en ingeladen in de githubpages. 

```{figure} Figures/rerunjobs.PNG
---
name: fig_rerun
width: 70%
---
Als het boek bouw proces klaar is zijn alle bolletjes groen gekleurd.
```

8. Ga via de link (code, rechterkant onder **About**) naar de GitHub page waar het boek online gezet wordt.
9. De output is gelijk aan {numref}`Figuur {number} <fig_templatebook>` hieronder.

``` {figure} figures/templateboekoutput.PNG
---
name: fig_templatebook
width: 100%
---
De output van het boek zoals dat op GitHub pages staat.
```

## Github Actions to deploy the book
De TeachBooks tool is zo gemaakt dat het omzet van de markdown (en eventueel notebook) files naar een HTML pagina automatisch gedaan wordt nadat er een verandering op GitHub gedaan wordt (een commit). Alhoewel de precieze werking voor nu niet van belang is, wordt er meer in deze [documentatie](https://teachbooks.io/manual/external/deploy-book-workflow/README.html) verteld over de precieze workflow die gebruik wordt.


