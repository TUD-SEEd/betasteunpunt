# Editing

Je hebt nu (hopelijk) de basics een beetje door. De volgende stap is (meer) zelfstandig aan de slag te gaan met het maken van een opgemaakt hoofdstuk.

```{exercise} Hoofdstuk toevoegen
Maak een nieuw markdown file aan, geef deze een hoofdstuk titel en voeg deze toe in de Table of Contents.
```

```{exercise} Secties en content toevoegen
Voeg tekst toe, verdeeld in secties en subsecties. Voeg ook een figuur toe. Verwijs in de tekst naar deze figuur (clickable link).
```

```{exercise} Verwijzing naar een hoofdstuk
[Refereer](sec-ref) in de tekst naar een ander hoofdstuk `[tekst](link)`. 
```

```{exercise} YouTube filmpje toevoegen
Voeg een [YouTube filmpje](sec-YT) toe.
```

```{exercise} Admonitions toevoegen
Voeg een admoniton toe, bijvoorbeeld een exercise, warning, of tip.
```

```{tip}
Vergeet niet om regelmatig je boek te laten bouwen om zo vroegtijdig eventuele fouten op te sporen!
```

`````{exercise} Literatuur referentie
Een van de documenten in de folder heet references.bib. Dat bestand is je literatuurlijst. In de lijst vind je al een referentie:
```{code}
@misc{jason_moore,
  title={Learn Multibody Dynamics, SymPy},
  author={Moore, Jason},
  howpublished={\url{https://moorepants.github.io/learn-multibody-dynamics/sympy.html}},
  year={2023}
}
```
Die referentie kun je oproepen via ``{cite:p}`jason_moore` ``, met als output: {cite:p}`jason_moore`

Zoek via google scholar een referentie op, klik op citeren en BibTeX. Kopier de code naar de reference.bib file en neem die referentie op in je hoofdstuk.

Om de referentie op te nemen op de pagina zelf, moet de volgend code toegevoegd worden:
````{code}
```{bibliography}
:filter: docname in docnames
```
````


`````

```{bibliography}
:filter: docname in docnames
```