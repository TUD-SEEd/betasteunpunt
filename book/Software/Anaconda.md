# Conda

Anaconda en Miniconda zijn beide distributies van de programmeertalen Python en R, voornamelijk gericht op het vereenvoudigen van pakketbeheer en implementatie voor data science, machine learning en wetenschappelijk computergebruik. Het belangrijkste verschil tussen deze distributies is de hoeveelheid benodigde schijfruimte (~4 GB voor Anaconda, 50 MB voor Miniconda). Terwijl Anaconda al alle hoofdpakketten voor u heeft geïnstalleerd, bepaal je met Miniconda precies wat je wilt installeren. Miniconda is dus een minimale installer voor de Anaconda-distributie. Het bevat alleen de conda-pakketbeheerder (om pakketten te installeren) en Python, samen met hun afhankelijkheden. Het wordt geleverd met geen vooraf geïnstalleerde pakketten, behalve deze essentiële. Dat betekent ook dat het een grafische gebruikersinterface mist die wel beschikbaar is met Anaconda.

## Installeren
We raden aan om Miniconda te installeren, omdat het een beter idee geeft van hoe de computer werkt, meer controle geeft over wat er wordt geïnstalleerd en veel minder schijfruimte in beslag neemt. Om Miniconda te installeren, downloadt en voert je het .exe-bestand uit zoals beschreven op hun [website](https://docs.anaconda.com/miniconda/install/).

```{warning}
Er zijn meerdere downloadopties op de site van conda. Zorg ervoor dat je miniconda downloadt. Wacht bovendien met het volgen van de onderstaande instructies totdat miniconda volledig is geïnstalleerd.
```

Open na de installatie de anaconda-prompt. Dit opent een terminal (een tekstinterface die wordt gebruikt om te communiceren met het besturingssysteem door opdrachten, scripts of programma's uit te voeren). Om te controleren of de installatie correct is en welke versie is geïnstalleerd, typ:

```{code}
conda --version
```

```{figure} condaversion.PNG
:figclass: margin
:width: 100%
```

en druk op enter, de terminal zal de conda-versie retourneren.

