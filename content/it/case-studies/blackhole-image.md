---
title: "Caso di Studio: Prima Immagine di un Buco Nero"
sidebar: false
---

{{< figure >}}
{{< /figure >}}

{{< blockquote
  cite="https://www.youtube.com/watch?v=BIvezCVcsYs"
  by="Katie Bouman, _Assistant Professor, Computing & Mathematical Sciences, Caltech_"
>}}
{{< /blockquote >}}

## Un telescopio dalla dimensione della Terra

The [Event Horizon telescope (EHT)](https://eventhorizontelescope.org) is an
array of eight ground-based radio telescopes forming a computational telescope
the size of the earth, studing the universe with unprecedented
sensitivity and resolution.  The huge virtual telescope,  which uses a technique
called very-long-baseline interferometry (VLBI), has an angular resolution of
[20 micro-arcseconds][resolution] — enough to read a newspaper in New York
from a sidewalk café in Paris!

[resolution]: https://eventhorizontelescope.org/press-release-april-10-2019-astronomers-capture-first-image-black-hole

### Obiettivi Principali e Risultati

- **A New View of the Universe:**
  The groundwork for the EHT's groundbreaking image had been laid 100 years
  earlier when [Sir Arthur Eddington][eddington] yielded the first
  observational support of Einstein's theory of general relativity.

- **The Black Hole:** EHT was trained on a supermassive black hole
  approximately 55 million light-years from Earth, lying at the center
  of the galaxy Messier 87 (M87) in the Virgo galaxy cluster. Its mass is
  6.5 billion times the Sun's. It had been studied for
  [over 100 years](https://www.jpl.nasa.gov/news/news.php?feature=7385), but never before
  had a black hole been visually observed.

- **Comparing Observations to Theory:** From Einstein’s general theory of
  relativity, scientists expected to find a shadow-like region caused by
  gravitational bending and capture of light. Scientists could
  use it to measure the black hole's enormous mass.

[eddington]: https://en.wikipedia.org/wiki/Eddington_experiment

### Le Sfide

- **Computational scale**

  EHT poses massive data-processing challenges, including rapid atmospheric
  phase fluctuations, large recording bandwidth, and telescopes that are
  widely dissimilar and geographically dispersed.

- **Too much information**

  Each day EHT generates over 350 terabytes of observations, stored on
  helium-filled hard drives. Reducing the volume and complexity of this much
  data is enormously difficult.

- **Into the unknown**

  When the goal is to see something never before seen, how can scientists be
  confident the image is correct?

{{< figure >}}
{{< /figure >}}

## Il Ruolo di NumPy

Che cosa succede se c'è un problema con i dati? O magari se un algoritmo si basa troppo su un'assunzione particolare. src = '/images/content_images/cs/dataprocessbh.png'
title = 'Pipeline della Processione Dati dell'EHT'
alt = 'data pipeline'
align = 'center'
attribution = '(Crediti del Diagramma: The Astrophysical Journal, Collaborazione del Telescopio Event Horizon)'
attributionlink = 'https://iopscience.iop.org/article/10.3847/2041-8213/ab0c57'

La collaborazione dell'EHT ha riscontrato queste problematiche durante l'elaborazione dei dati indipendente dei gruppi di ricerca, usando tecniche di ricostruzione d'immagine ben stabilite e all'avanguardia.  Quando i risultati si sono dimostrati coerenti, sono stati combinati per produrre la prima immagine mai esistita del buco nero.

Il loro lavoro illustra il ruolo che l'ecosistema scientifico di Python gioca nell'avanzamento della scienza attraverso l'analisi collaborativa di dati.

{{< figure >}}
{{< /figure >}}

For example, the [`eht-imaging`][ehtim] Python package provides tools for
simulating and performing image reconstruction on VLBI data.
NumPy è al centro dell'elaborazione dei dati matriciali utilizzati in questo pacchetto, come illustrato dal grafico delle dipendenze parziali del software
qui sotto.

{{< figure >}}
{{< /figure >}}

[ehtim]: https://github.com/achael/eht-imaging

Besides NumPy, many other packages, such as
[SciPy](https://scipy.org) and [Pandas](https://pandas.pydata.org), are part of the
data processing pipeline for imaging the black hole.
The standard astronomical file formats and time/coordinate transformations
were handled by [Astropy][astropy], while [Matplotlib][mpl] was used
in visualizing data throughout the analysis pipeline, including the generation
of the final image of the black hole.

[astropy]: https://www.astropy.org/
[mpl]: https://matplotlib.org/

## Sommario

La gestione efficiente ed adattabile di matrici n-dimensionali, che è la caratteristica centrale di NumPy,
ha permesso ai ricercatori di manipolare grandi insiemi di dati numerici, fornendo una base
per la prima immagine mai osservata di un buco nero. Pietra miliare della scienza, si tratta di una splendida testimonianza visiva della teoria di Einstein.   Algoritmi innovativi e tecniche di elaborazione dati, migliorando i modelli astronomici esistenti, hanno contribuito a spiegare un mistero
dell'universo.

{{< figure >}}
{{< /figure >}}
