# Conda
Anaconda en Miniconda zijn beide distributies van de programmeertalen Python en R, voornamelijk gericht op het vereenvoudigen van pakketbeheer en implementatie voor data science, machine learning en wetenschappelijk computergebruik. Het belangrijkste verschil tussen deze distributies is de hoeveelheid benodigde schijfruimte (~4 GB voor Anaconda, 50 MB voor Miniconda). Terwijl Anaconda al alle hoofdpakketten voor u heeft geïnstalleerd, bepaal je met Miniconda precies wat je wilt installeren. Miniconda is dus een minimale installer voor de Anaconda-distributie. Het bevat alleen de conda-pakketbeheerder (om pakketten te installeren) en Python, samen met hun afhankelijkheden. Het wordt geleverd met geen vooraf geïnstalleerde pakketten, behalve deze essentiële. Dat betekent ook dat het een grafische gebruikersinterface mist die wel beschikbaar is met Anaconda.

## Installeren
We raden aan om Miniconda te installeren, omdat het een beter idee geeft van hoe de computer werkt, meer controle geeft over wat er wordt geïnstalleerd en veel minder schijfruimte in beslag neemt. Om Miniconda te installeren, downloadt en voert je het .exe-bestand uit zoals beschreven op hun [website](https://docs.anaconda.com/miniconda/install/).

```{warning}
Er zijn meerdere downloadopties op de site van conda. Zorg ervoor dat je miniconda downloadt. Wacht bovendien met het volgen van de onderstaande instructies totdat miniconda volledig is geïnstalleerd.
```

Open na de installatie de anaconda-prompt. Dit opent een terminal (een tekstinterface die wordt gebruikt om te communiceren met het besturingssysteem door opdrachten, scripts of programma's uit te voeren), zie {numref}`Figuur {number} <fig_condaversion>`. Om te controleren of de installatie correct is en welke versie is geïnstalleerd, typ:

```{code}
conda --version
```

```{figure} condaversion.PNG
---
name: fig_condaversion
figclass: margin
width: 100%
---
De conda terminal waar we de versie checken.
```

en druk op enter, de terminal zal de conda-versie retourneren.

Om bepaalde packages te installeren heb je de zogenaamde `pip` pipeline nodig. Om zeker van te zijn dat deze is geïnstalleerd, type in de terminal `pip --version`. Als `pip` niet beschikbaar is, kun je deze installeren met:
```{code}
conda install pip
```


## Requirements
Omdat miniconda een minimale installatie is, moet je een aantal packages, libraries extra installeren. De belangrijkste staan in deze [requirements file](./requirements.txt). 

```{exercise}
1. Download de requirements file. 

2. Start miniconda prompt. 

3. Navigeer naar de map waarin de gedownloade file staat.

4. Type `pip install -r requirements.txt` en druk enter.

5. De packages die nog niet geïnstalleerd zijn worden nu geïnstalleerd. Dat kan even duren...

```

