---
title: "Estudo de Caso: Estimativa de Pose 3D com DeepLabCut"
sidebar: false
---

{{< figure >}}
{{< /figure >}}

{{< blockquote
  cite="https://news.harvard.edu/gazette/story/newsplus/harvard-researchers-awarded-czi-open-source-award/"
  by="Alexander Mathis, _Assistant Professor, École polytechnique fédérale de Lausanne_ ([EPFL](https://www.epfl.ch/en/))"
>}}
{{< /blockquote >}}

## Sobre o DeepLabCut

[DeepLabCut](https://github.com/DeepLabCut/DeepLabCut) is an open source toolbox that empowers researchers at hundreds of institutions worldwide to track behaviour of laboratory animals, with very little training data, at human-level accuracy. Com a tecnologia DeepLabCut, cientistas podem aprofundar a compreensão científica do controle motor e do comportamento em diversas espécies animais e escalas temporais.

Várias áreas de pesquisa, incluindo a neurociência, a medicina e a biomecânica, utilizam dados de rastreamento da movimentação de animais. A DeepLabCut ajuda a compreender o que os seres humanos e outros animais estão fazendo, analisando ações que foram registradas em vídeo. Ao usar automação para tarefas trabalhosas de monitoramento e marcação, junto com análise de dados baseada em redes neurais profundas, a DeepLabCut garante que estudos científicos envolvendo a observação de animais como primatas, camundongos, peixes, moscas etc. sejam mais rápidos e precisos.

{{< figure >}}
{{< /figure >}}

DeepLabCut's non-invasive behavioral tracking of animals by extracting the poses of animals is crucial for scientific pursuits in domains such as biomechanics, genetics, ethology & neuroscience. Medir as poses dos animais de maneira não invasiva através de vídeo - sem marcadores - com fundos dinâmicos é computacionalmente desafiador, tanto tecnicamente quanto em termos de recursos e dados de treinamento necessários.

A DeepLabCut permite que pesquisadores façam estimativas de poses para os sujeitos, permitindo que se possa quantificar de maneira eficiente seus comportamentos através de um conjunto de ferramentas de software baseado em Python.  Com a DeepLabCut, pesquisadores podem identificar quadros (<em x-id="3">frames</em>) distintos em vídeos e rotular digitalmente partes específicas do corpo em alguns quadros com uma GUI especializada. A partir disso, a arquitetura de estimação de poses baseada em deep learning da DeepLabCut aprende a selecionar essas mesmas características no resto do vídeo e em outros vídeos similares. It works across species of animals, from common laboratory animals such as flies and mice to more unusual animals like [cheetahs][cheetah-movement].

[cheetah-movement]: https://www.technologynetworks.com/neuroscience/articles/interview-a-deeper-cut-into-behavior-with-mackenzie-mathis-327618

DeepLabCut uses a principle called [transfer learning](https://arxiv.org/pdf/1909.11229), which greatly reduces the amount of training data required and speeds up the convergence of the training period.  Dependendo das suas necessidades, usuários podem escolher diferentes arquiteturas de rede que forneçam inferência mais rápida (por exemplo, MobileNetV2), e que também podem ser combinadas com feedback experimental em tempo real. DeepLabCut originally used the feature detectors from a top-performing human pose estimation architecture, called [DeeperCut](https://arxiv.org/abs/1605.03170), which inspired the name. O pacote foi significativamente alterado para incluir mais arquiteturas, métodos de ampliação e uma experiência de usuário completa no front-end. Além de possibilitar experimentos biológicos em grande escala, DeepLabCut fornece capacidades ativas de aprendizado para que os usuários possam aumentar o conjunto de treinamento ao longo do tempo, para incluir casos particulares e tornar seu algoritmo de estimativa de poses robusto no seu contexto específico.

Recently, the [DeepLabCut model zoo](https://deeplabcut.github.io/DeepLabCut/docs/ModelZoo.html) was introduced, which provides pre-trained models for various species and experimental conditions from facial analysis in primates to dog posture. Isso pode ser executado na nuvem, por exemplo, sem qualquer rotulagem de novos dados ou treinamento em rede neural, e não é necessária nenhuma experiência em programação.

### Principais Objetivos e Resultados

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

  Um fluxo de trabalho típico na DeepLabCut inclui:

  - criação e refinamento de conjuntos de treinamento por meio de aprendizagem ativa
  - criação de redes neurais personalizadas para animais e cenários específicos
  - código para inferência em larga escala em vídeos
  - inferências de desenho usando ferramentas integradas de visualização

{{< figure >}}
{{< /figure >}}

[DLCToolkit]: https://github.com/DeepLabCut/DeepLabCut

### Desafios

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

## O papel da NumPy nos desafios da estimação de poses

NumPy supre a principal necessidade da tecnologia DeepLabCut de cálculos numéricos de alta velocidade para análises comportamentais.  Besides NumPy, DeepLabCut employs
various Python software that utilize NumPy at their core, such as
[SciPy](https://www.scipy.org), [Pandas](https://pandas.pydata.org),
[matplotlib](https://matplotlib.org),
[Tensorpack](https://github.com/tensorpack/tensorpack),
[imgaug](https://github.com/aleju/imgaug),
[scikit-learn](https://scikit-learn.org/stable/),
[scikit-image](https://scikit-image.org) and
[Tensorflow](https://www.tensorflow.org).

As seguintes características da NumPy desempenharam um papel fundamental para atender às necessidades de processamento de imagens, combinatória e cálculos rápidos nos algoritmos de estimação de pose na DeepLabCut:

- Vetorização
- Operações em arrays com máscaras
- Álgebra linear
- Amostragem aleatória
- Reordenamento de matrizes grandes

A DeepLabCut utiliza as capacidades de manipulação de arrays da NumPy em todo o fluxo de trabalho oferecido pelo seu conjunto de ferramentas. Em particular, a NumPy é usada para amostragem de quadros distintos para serem rotulados com anotações humanas e para escrita, edição e processamento de dados de anotação.  Dentro da TensorFlow, a rede neural é treinada pela tecnologia DeepLabCut em milhares de iterações para prever as anotações verdadeiras dos quadros. Para este propósito, densidades de alvo (<em x-id="3">scoremaps</em>) são criadas para colocar a estimativa como um problema de tradução de imagem a imagem. Para tornar as redes neurais robustas, o aumento de dados é empregado, o que requer o cálculo de scoremaps alvo sujeitos a várias etapas geométricas e de processamento de imagem. Para tornar o treinamento rápido, os recursos de vectorização da NumPy são utilizados. Para inferência, as previsões mais prováveis de scoremaps alvo precisam ser extraídas e é necessário "vincular previsões para montar animais individuais" de maneira eficiente.

{{< figure >}}
{{< /figure >}}

## Resumo

Observação e descrição eficiente do comportamento é uma peça fundamental da etologia, neurociência, medicina e tecnologia modernas.
[DeepLabCut](https://static1.squarespace.com/static/57f6d51c9f74566f55ecf271/t/5eab5ff7999bf94756b27481/1588289532243/NathMathis2019.pdf)
allows researchers to estimate the pose of the subject, efficiently enabling
them to quantify the behavior. Com apenas um pequeno conjunto de imagens de treinamento, o conjunto de ferramentas em Python da DeepLabCut permite treinar uma rede neural tão precisa quanto a rotulagem humana, expandindo assim sua aplicação para não só análise de comportamento dentro do laboratório, mas também potencialmente em esportes, análise de locomoção, medicina e estudos sobre reabilitação. Desafios complexos em combinatória e processamento de dados enfrentados pelos algoritmos da DeepLabCut são tratados através do uso de recursos de manipulação de matriz do NumPy.

{{< figure >}}
{{< /figure >}}
