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



[Jupyter book](https://jupyterbook.org/en/stable/start/overview.html#install-jupyter-book)

### Requirements.txt en TeachBooks Python Package

Als TeachBooks verzamelen we een reeks bestaande open-source software en houden we onze boeken up-to-date zodat jij dat niet hoeft te doen! Sommige software is samen met onze TA's ontwikkeld om de leerervaring van onze studenten te verbeteren en het boekontwikkelingsproces voor onze docenten te vergemakkelijken. Door deze tools vanaf een centrale locatie in te zetten, kunnen we veelvoorkomende problemen voorkomen voordat ze zich voordoen en ze snel verhelpen als ze zich toch voordoen. Omdat het landschap van open-source software snel verandert, is het essentieel om contact te houden en bronnen met elkaar te delen om onderhoud en downtime voor onze boekwebsites te minimaliseren en ons te richten op wat echt belangrijk is: lesgeven!





Bij het werken aan grotere projecten (met veel coole interactieve functies) kan het nodig zijn om veel python-pakketten te installeren. Het kan handig zijn om de benodigde pakketten op te geven in een tekstbestand (bijvoorbeeld `environment.yml`) en dan conda te vertellen om de omgeving aan te maken op basis van de inhoud van het bestand!

Als je bij een team komt dat aan complexe projecten werkt, kan het bovendien handig zijn om een nieuwe omgeving aan te maken op basis van zo'n tekstbestand, zodat je een up-to-date omgeving hebt die je een vliegende start geeft. Het team kan ook een `requirements.txt` bestand leveren waarin alle pakketten staan die je moet downloaden om aan het project te kunnen werken. Nu zou het ook duidelijk moeten worden waarom het de voorkeur verdient om voor elk project/boek waaraan je werkt een nieuwe omgeving aan te maken, omdat ze kunnen vereisen dat je verschillende pakketten gebruikt!

Hier is een voorbeeld van hoe een `requirements.txt` bestand eruit zou kunnen zien.

```
# first list the packages you wish to download from PyPI
sympy
teachbooks
jupyterbook_patches

# now list the packages (and the respective url) you wish to download from the GitLab package registry
--extra-index-url https://gitlab.tudelft.nl/api/v4/projects/11239/packages/pypi/simple
sphinx-thebe ~= 0.9.9
```

Als je het TeachBooks template gebruikt, wordt het pakket `teachbooks` automatisch opgenomen in het `requirements.txt` bestand en hoef je het pakket `jupyter-book` niet op te geven.

Nu ben je klaar om boeken te maken!

(=sec:lok)
## Boek lokaal opslaan
1. Open de repository die je wilt klonen. Bovenin vind je de groene knop genaamd '<> code'

``` {figure} ./figures/gitdesktop1.png
```

2. Kopieer de link en open Github Desktop.

3. In GitHub Desktop, klik linksboven op `file` en vervolgens `Clone Repository`.

Clicking on the button will display the following screen. Click on Open with GitHub Desktop.

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

De bestanden worden nu gekopieerd en je hebt een lokale kopie van de repository.

## Stap X... het bouwen van het boek
