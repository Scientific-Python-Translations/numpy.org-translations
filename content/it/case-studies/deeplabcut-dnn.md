---
title: "Caso Di Studio: Stima della Posa con DeepLabCut 3D"
sidebar: false
---

{{< figure >}}
{{< /figure >}}

{{< blockquote
  cite="https://news.harvard.edu/gazette/story/newsplus/harvard-researchers-awarded-czi-open-source-award/"
  by="Alexander Mathis, _Assistant Professor, École polytechnique fédérale de Lausanne_ ([EPFL](https://www.epfl.ch/en/))"
>}}
{{< /blockquote >}}

## Riguardo DeepLabCut

[DeepLabCut](https://github.com/DeepLabCut/DeepLabCut) is an open source toolbox that empowers researchers at hundreds of institutions worldwide to track behaviour of laboratory animals, with very little training data, at human-level accuracy. Con la tecnologia DeepLabCut, gli scienziati possono approfondire la comprensione scientifica del controllo motorio e del comportamento in tutte le specie animali ed in tutti i lassi di tempo.

Diversi settori di ricerca, tra cui neuroscienza, medicina e biomeccanica, utilizzano i dati di monitoraggio del movimento degli animali. DeepLabCut aiuta a capire ciò che gli esseri umani e gli altri animali stanno facendo analizzando le azioni che sono state registrate su pellicola. Utilizzando l'automazione per le laboriose attività di etichettatura e monitoraggio, insieme all'analisi dei dati basata su reti neurali profonde, DeepLabCut rende molto più veloci e accurati gli studi scientifici che prevedono l'osservazione di animali quali primati, topi, pesci, mosche, ecc.

{{< figure >}}
{{< /figure >}}

DeepLabCut's non-invasive behavioral tracking of animals by extracting the poses of animals is crucial for scientific pursuits in domains such as biomechanics, genetics, ethology & neuroscience. Misurare le pose degli animali in modo non invasivo da un video - senza marcatori - su sfondi che cambiano dinamicamente è una sfida computazionale, sia dal punto di vista tecnico che da quello delle risorse necessarie e dei dati di addestramento richiesti.

DeepLabCut permette ai ricercatori di stimare la posa del soggetto, consentendo loro di quantificare in modo efficiente il comportamento attraverso un insieme di strumenti software basato su Python.  Con DeepLabCut, i ricercatori possono identificare fotogrammi distinti di video, etichettare digitalmente parti del corpo specifiche in poche decine di fotogrammi con un'interfaccia grafica personalizzata; dopodiché le architetture di stima della posa basate sull'apprendimento profondo di DeepLabCut imparano a individuare quelle stesse caratteristiche nel resto del video e in altri video simili di animali. It works across species of animals, from common laboratory animals such as flies and mice to more unusual animals like [cheetahs][cheetah-movement].

[cheetah-movement]: https://www.technologynetworks.com/neuroscience/articles/interview-a-deeper-cut-into-behavior-with-mackenzie-mathis-327618

DeepLabCut uses a principle called [transfer learning](https://arxiv.org/pdf/1909.11229), which greatly reduces the amount of training data required and speeds up the convergence of the training period.  A seconda delle esigenze, gli utenti possono scegliere diverse architetture di rete che forniscono un'inferenza più rapida (ad esempio, MobileNetV2), che può anche essere combinata con un feedback sperimentale in tempo reale. DeepLabCut originally used the feature detectors from a top-performing human pose estimation architecture, called [DeeperCut](https://arxiv.org/abs/1605.03170), which inspired the name. Il pacchetto è stato ora modificato in modo significativo per includere architetture aggiuntive, metodi di incremento e un'esperienza d'interazione con l'utente completa. Inoltre, per supportare esperimenti biologici su larga scala, DeepLabCut offre funzionalità di apprendimento attivo che consentono agli utenti di aumentare il set di addestramento nel tempo per coprire i casi limite e rendere l'algoritmo di stima della posa robusto all'interno del contesto specifico.

Recently, the [DeepLabCut model zoo](https://deeplabcut.github.io/DeepLabCut/docs/ModelZoo.html) was introduced, which provides pre-trained models for various species and experimental conditions from facial analysis in primates to dog posture. Questo può essere eseguito, ad esempio, nel cloud senza etichettatura di nuovi dati o addestramento di reti neurali, e non è necessaria alcuna esperienza di programmazione.

### Obiettivi Principali e Risultati

- **Automation of animal pose analysis for scientific studies:**

  The primary objective of DeepLabCut technology is to measure and track posture
  of animals in a diverse settings. This data can be used, for example, in
  neuroscience studies to understand how the brain controls movement, or to
  elucidate how animals socially interact. Researchers have observed a
  [tenfold performance boost](https://www.biorxiv.org/content/10.1101/457242v1)
  with DeepLabCut. Poses can be inferred offline at up to 1200 frames per second
  (FPS).

- **Creation of an easy-to-use Python toolkit for pose estimation:**

  DeepLabCut wanted to share their animal pose-estimation technology in the form
  of an easy to use tool that can be adopted by researchers easily. So they have
  created a complete, easy-to-use Python toolbox with project management features
  as well. These enable not only automation of pose-estimation but also
  managing the project end-to-end by helping the DeepLabCut Toolkit user right
  from the dataset collection stage to creating shareable and reusable analysis
  pipelines.

  Their [toolkit][DLCToolkit] is now available as open source.

  Un tipico flusso di lavoro con DeepLabCut comprende:

  - la creazione ed il perfezionamento di gruppi di formazione attraverso l'apprendimento attivo
  - la creazione di reti neurali su misura per animali e scenari specifici
  - un codice per l'inferenza su larga scala per video
  - rappresentazione di inferenze utilizzando strumenti di visualizzazione integrati

{{< figure >}}
{{< /figure >}}

[DLCToolkit]: https://github.com/DeepLabCut/DeepLabCut

### Le Sfide

- **Speed**

  Fast processing of animal behavior videos in order to measure their behavior
  and at the same time make scientific experiments more efficient, accurate.
  Extracting detailed animal poses for laboratory experiments, without
  markers, in dynamically changing backgrounds, can be challenging, both
  technically as well as in terms of resource needs and training data required.
  Coming up with a tool that is easy to use without the need for skills such
  as computer vision expertise that enables scientists to do research in more
  real-world contexts, is a non-trivial problem to solve.

- **Combinatorics**

  Combinatorics involves assembly and integration of movement of multiple
  limbs into individual animal behavior. Assembling keypoints and their
  connections into individual animal movements and linking them across time
  is a complex process that requires heavy-duty numerical analysis, especially
  in case of multi-animal movement tracking in experiment videos.

- **Data Processing**

  Last but not the least, array manipulation - processing large stacks of
  arrays corresponding to various images, target tensors and keypoints is
  fairly challenging.

{{< figure >}}
{{< /figure >}}

## Il Ruolo di NumPy verso le Sfide di Stima della Posa

NumPy affronta la necessità principale della tecnologia DeepLabCut di calcoli numerici ad alta velocità
per l'analisi comportamentale.  Besides NumPy, DeepLabCut employs
various Python software that utilize NumPy at their core, such as
[SciPy](https://www.scipy.org), [Pandas](https://pandas.pydata.org),
[matplotlib](https://matplotlib.org),
[Tensorpack](https://github.com/tensorpack/tensorpack),
[imgaug](https://github.com/aleju/imgaug),
[scikit-learn](https://scikit-learn.org/stable/),
[scikit-image](https://scikit-image.org) and
[Tensorflow](https://www.tensorflow.org).

Le seguenti caratteristiche di NumPy hanno svolto un ruolo fondamentale nel risolvere i requisiti di elaborazione delle immagini, di combinatoria e di velocità di calcolo degli algoritmi di stima della posa di DeepLabCut:

- Vettorizzazione
- Operazioni con Arrays Mascherati
- Algebra Lineare
- Campionamento Casuale
- Riarrangiamento di arrays di grandi dimensioni

DeepLabCut utilizza le capacità di array di NumPy durante il flusso di lavoro offerto dal toolkit. In particolare, NumPy viene utilizzato per il campionamento di frame distinti per l'etichettatura dell'annotazione umana e per scrivere, modificare ed elaborare i dati di annotazione.  All'interno di TensorFlow, la rete neurale è addestrata dalla tecnologia DeepLabCut sopra migliaia di iterazioni per prevedere le annotazioni di verità fondamentali dai frames. A questo scopo, le densità obiettivo (scoremap) sono create per lanciare la stima di posa come un problema di traduzione da immagine ad immagine. Per rendere le reti neurali
robuste, si ricorre all'aumento dei dati, che richiede il calcolo di scoremap del bersaglio soggetto in varie fasi di elaborazione geometrica e dell'immagine. Per rendere
veloce l'addestramento, le capacità di vettorializzazione di NumPy vengono sfruttate. Per l'inferenza,
le previsioni più probabili dalle scoremap di destinazione devono essere estratte e bisogna “collegare in modo efficiente le predizioni per assemblare i singoli animali”.

{{< figure >}}
{{< /figure >}}

## Sommario

Osservare e descrivere in modo efficiente il comportamento è un principio fondamentale dell'etologia moderna, delle neuroscienze, della medicina e della tecnologia.
[DeepLabCut](https://static1.squarespace.com/static/57f6d51c9f74566f55ecf271/t/5eab5ff7999bf94756b27481/1588289532243/NathMathis2019.pdf)
allows researchers to estimate the pose of the subject, efficiently enabling
them to quantify the behavior. Con solo un piccolo insieme di immagini di addestramento, l'insieme di strumenti Python di
DeepLabCut permette di addestrare una rete neurale con un'accuratezza di etichettatura al pari del livello umano, espandendo così la sua applicazione non solo all'analisi del comportamento in laboratorio, ma potenzialmente anche nello sport, nell'analisi dell'andatura e negli studi di medicina e riabilitazione. Le complesse sfide di calcolo combinatorio e di elaborazione dei dati riscontrate dagli algoritmi di DeepLabCut vengono affrontate attraverso l'uso delle capacità di NumPy di manipolazione degli array.

{{< figure >}}
{{< /figure >}}
