# Lokaal bouwen

Om het boek niet alleen online te bouwen en te zien, maar ook op je lokale computer te maken en bouwen heb je het volgende nodig: 

<label><input type="checkbox" class="box"> Python, bijv. via [conda](../Software/Anaconda.md).</input></label> 

<label><input type="checkbox" class="box"> Een integrated development environment (IDE) zoals [VSC](../Software/VSC.md).</input></label> 

<label><input type="checkbox" class="box"> De juiste software packages.</input></label> 

<label><input type="checkbox" class="box"> De bestanden op de computer.</input></label> 

De eerste drie stappen hoef je maar eenmalig uit te voeren. Als je alle benodigdheden hebt geïnstalleerd, volstaat het een volgende keer om direct naar [stap X](sec:lok) te gaan.

## Stap 1: Miniconda installeren
Hopelijk heb je Miniconda al geïnstalleerd, zo niet dan kun je [deze instructies](../Software/Anaconda.md) volgen. 

Heb je meer informatie nodig over Miniconda? Kijk dan eens [hier](https://teachbooks.io/learn-programming/install/python/miniconda.html).


## Stap 2: Installeren van een IDE
Om bestanden te kunnen bewerken en (een deel van) de output te kunnen zien, is het nodig om een IDE te installeren, bijvoorbeeld [VSC](../Software/VSC.md). Als je dat nog niet gedaan hebt, volg de instructies voor het installeren van VSC en de betreffende extensies.

Ook hier geldt, heb je meer informatie nodig, kijk dan [hier](https://teachbooks.io/learn-programming/install/ide/vsc.html).

## Stap 3: Jupyter-book
Om de boeken lokaal te kunnen bouwen (van markdown files omzetten naar functionele HTML pagina's) heb je nog een aantal packages nodig, zie bijv. [Jupyter book](https://jupyterbook.org/en/stable/start/overview.html#install-jupyter-book). Dat kun je zelf handmatig doen, maar de Teachbooks tool voorziet daar ook in. Heb je dat nog niet gedaan, bekijk dan de sectie over de [requirements](seq:req) en volg de stappen die daar beschrijven staan. Dan ben je als het goed is klaar om ook op de eigen computer het boek te bouwen en bekijken.

(sec:lok)=
## Stap 4: Boek lokaal opslaan
Het boek staat nu alleen nog online, op GitHub. We moeten alles downloaden (clonen). Dat kan zoals [hier beschreven met VSC](https://learn.microsoft.com/en-us/azure/developer/javascript/how-to/with-visual-studio-code/clone-github-repository?tabs=activity-bar). Maar we kiezen er hiervoor om dat te doen via GitHub Desktop.

1. Open op GitHub de repository die je wilt klonen. Bovenin vind je de groene knop genaamd '<> code'

``` {figure} ./figures/gitdesktop1.png
```

2. Kopieer de link en open Github Desktop.

3. In GitHub Desktop, klik linksboven op `file` en vervolgens `Clone Repository`. Dat levert, als het goed is het volgende scherm op: 

``` {figure} ./figures/gitdesktop2.png
---
width: 50%
---
```

4. Klik vervolgens op URL, plak de gekopieerde link van de repository en specificeer waar de map naartoe gekloond moet worden. 

``` {figure} ./figures/gitdesktop3.png
---
width: 50%
---
```

De bestanden worden nu gekopieerd en je hebt een lokale (exacte) kopie van de repository.

## Stap 5: Aanpassing maken in VSC
1. Open VSC en open de folder waarin het *boek* staat. Je kunt dezelfde folder structuur herkennen die op GitHub stond. 

2. Open het `overview.md` bestand en pas deze naar eigen wens aan. Bijvoorbeeld door de inhoud van een document dat je mee hebt genomen kopieert (let op! Headings en figuren worden natuurlijk niet meteen omgezet). 

3. Navigeer in VSC naar de `some_content folder`, en creëer in die map een nieuwe markdown file (bijv. `nieuwe pagina.md`) (linksboven new file). Zet in de die file een titel (bijv. # Mijn eerste hoofdstuk).

Nu heb je een eigen hoofdstuk aangemaakt, maar die is nog niet in het boek opgenomen. Dat moet je melden in de table of contents. 

4. Zoek de `_toc.yml` file en open deze. Voeg het hoofdstuk toe (`- file: some_content/nieuwe_pagina`). Let op, je moet op de juiste wijze inspringen anders krijg je foutmeldingen.

5. Sla alle aangepaste documenten op. (`ctrl + s`)

6. Laat een van de workshopleiders even controleren.

## Stap 6: Synchroniseren met GitHub
Je hebt nu aanpassingen gedaan maar die staan nog niet op GitHub. Ga weer terug naar GitHub Desktop. Daar zie je de aangepaste bestanden. Geef een bijbehorende summary in de tekstbalk links onder, druk op `commit to main` en vervolgens op  

```{figure} figures/gitdesktop edits.PNG
---
width: 80%
---
Alle aangepaste bestanden zie je links in GitHub Dekstop.
```

````{tip}
:class:dropdown
Een goede aanpak in werken met GitHub is als je weer verder werkt met aan je project je eerst een `pull` doet, het werk van eventuele collega's die aan hetzelfde wordt dan gekopieerd. Na het werken `commit` en `push` je je wijzigingen naar GitHub. Als de collega's op dezelfde manier werken, heeft iedereen altijd de laatste versie.

```{note}
Een stap verder is dat iedereen werkt in een eigen `branche` en deze later `merged` met de `main branch`  
```
````

## Stap 7: Het lokaal bouwen van het boek

