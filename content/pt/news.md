---
title: Notícias
sidebar: false
newsHeader: Lançado o NumPy versão 2.2.0!
date: 2024-12-08
---

### Lançado o NumPy versão 2.2.0

_8 de dezembro de 2024_ -- A NumPy 2.2.0 é uma versão que nos traz de volta para o calendário habitual de lançamento duas vezes por ano. Ela inclui um número de pequenas limpezas, melhorias para o StringDType, e melhor suporte para
o free-threaded Python. Alguns dos destaques são:

- Novas funções `matvec` e `vecmat`,
- Várias melhorias nas anotações de tipos,
- Suporte melhorado para o novo StringDType,
- Suporte aprimorado para Python free-threaded,
- Correções para o f2py.

Esta versão suporta as versões 3.10-3.13 do Python.

### Lançado o NumPy versão 2.1.0

_18 de agosto de 2024_ -- NumPy 2.1.0 fornece suporte para Python 3.13 e remove suporte para Python 3.9. Além das habituais correções de erros e suporte a Python atualizado, esta versão ajuda a trazer o NumPy de volta ao ciclo habitual de lançamento após o longo desenvolvimento da versão 2.0. Os destaques desta versão são:

- Suporte ao Python 3.13.
- Suporte preliminar para Python 3.13 free threaded.
- Suporte para o padrão array-api 2023.12.

As versões 3.10-3.13 do Python são suportadas por esta versão.

### NumPy 2.0.0 lançada

_16 de junho de 2024_ -- NumPy 2.0.0 é a primeira grande versão desde 2006. É o resultado de 11 meses de desenvolvimento desde a última feature release e é o trabalho de 212 contribuidores espalhado por 1078 pull requests. Esta versão contém um grande número de novas funcionalidades interessantes, bem como mudanças nas APIs Python e C.  As mudanças incluem quebras de compatibilidade que não puderam acontecer em uma versão regular menor - incluindo uma quebra na ABI, mudanças nas regras de promoção de tipo e mudanças na API
que poderiam não estar emitindo alertas de fim de suporte nas versões 1.26.x. Documentos-chave, relacionados a como se adaptar às mudanças no NumPy 2.0, incluem:

- O [guia de migração NumPy 2.0](https://numpy.org/devdocs/numpy_2_0_migration_guide.html)
- As [notas de lançamento da versão 2.0.0](https://numpy.org/devdocs/release/2.0.0-notes.html)
- Issue de anúncio para atualizações de estado: [numpy#24300](https://github.com/numpy/numpy/issues/24300)

A postagem de blog ["NumPy 2.0: an evolutionary milestone"](https://blog.scientific-python.org/numpy/numpy2/) conta um pouco da história sobre como esta versão foi construída.

### Data de lançamento da NumPy 2.0: 16 de junho

_23 de maio de 2024_ -- Estamos animados em anunciar que planejamos lançar a NumPy 2.0 em 16 de junho de 2024. Este lançamento está em desenvolvimento há mais de um ano, e
é o primeiro grande lançamento desde 2006. Importantly, in addition to many new
features and performance improvement, it contains **breaking changes** to the
ABI as well as the Python and C APIs. Importante, além de muitas funcionalidades novas e melhoria de desempenho, esta versão contém **quebras de compatibilidade** com a ABI e com as APIs Python e C. É provável que os pacotes downstream e o código de usuário final precisem ser adaptados - se você puder, por favor, verifique se o seu código funciona com NumPy `2.0.0rc2`. **Por favor, veja o seguinte para mais detalhes:**

- O [guia de migração NumPy 2.0](https://numpy.org/devdocs/numpy_2_0_migration_guide.html)
- As [notas de lançamento da versão 2.0.0](https://numpy.org/devdocs/release/2.0.0-notes.html)
- Issue de anúncio para atualizações de estado: [numpy#24300](https://github.com/numpy/numpy/issues/24300)

### Arrecadação de fundos de fim de ano da NumFOCUS

_19 de dezembro de 2023_ -- A NumFOCUS se juntou ao PyCharm durante sua campanha de final de ano para oferecer 30% de desconto em licenças de PyCharm para novos usuários. Todas as receitas do primeiro ano das compras do PyCharm a partir de agora
até 23 de dezembro de 2023 irão diretamente para os programas NumFOCUS.

Use a URL única que permitirá rastrear as compras https://lp.jetbrains.com/support-data-science/ ou um código de cupom ISUPPORTDATASCIENCE

### Lançada versão 1.26.0 do NumPy

_17 de junho de 2023_ -- [NumPy 1.25.0](https://numpy.org/doc/stable/release/1.25.0-notes.html) está disponível agora. Os destaques desta versão são:

- Suporte ao Python 3.12.0.
- Compatibilidade com Cython 3.0.0.
- Utilização do sistema Meson para compilação
- Suporte a SIMD atualizado
- Melhorias para f2py, suporte a meson e bind(x)
- Suporte à versão mais recente da biblioteca Accelerate BLAS/LAPACK

A versão 1.26.0 é uma continuação da série de versões 1.25.x que marcam a transição para o sistema de compilação Meson e o fornecimento de suporte para o Cython 3.0.0.
Um total de 20 pessoas contribuíram para este lançamento e 59 pull requests foram incorporadas.

As versões do Python suportadas por esta versão são 3.9-3.12.

### numpy.org agora está disponível em japonês e português

_2 de agosto de 2023_ -- numpy.org agora está disponível em 2 idiomas adicionais: japonês e português. Isto não seria possível sem nossos voluntários dedicados:

_Português:_

- Melissa Weber Mendonça (melissawm)
- Ricardo Prins (ricardoprins)
- Getúlio Silva (getuliosilva)
- Julio Batista Silva (jbsilva)
- Alexandre de Siqueira (alexdesiqueira)
- Alexandre B A Villares (villares)
- Vini Salazar (vinisalazar)

_Japonês:_

- Atsushi Sakai (AtsushiSakai)
- KKunai
- Tom Kelly (TomKellyGenetics)
- Yuji Kanagawa (kngwyu)
- Tetsuo Koyama (tkoyama010)

O trabalho na infraestrutura de tradução é apoiado com financiamento da CZI.

No futuro, adoraríamos traduzir o site para mais línguas.
Se você quiser ajudar, por favor entre em contato com o time de traduções do NumPy no Slack:
https://join.slack.com/t/numpy-team/shared_invite/zt-1gokbq56s-bvEpo10Ef7aHbVtVFeZv2w.
(Procure pelo canal de #translations.) Também estamos construindo uma Equipe de Traduções que vai trabalhar na localização da documentação e conteúdo educacional por todo o ecossistema de Python científico. Se esse trabalho te interessa, junte-se a nós no Discord do projeto Scientific Python: https://discord.gg/khWtqY6RKr. (Procure pelo canal #translation)

### Lançado o NumPy 1.25.0

_31 de dezembro de 2021_ -- [NumPy 1.22.0](https://numpy.org/doc/stable/release/1.22.0-notes.html) está agora disponível. Os destaques desta versão são:

- Suporte para MUSL, agora existem rodas MUSL.
- Suporte para o compilador Fujitsu C/C++.
- Arrays de objetos agora são suportados em einsum.
- Suporte para a multiplicação da matriz inplace (`@=`).

A versão 1.25.0 do NumPy continua o trabalho de melhorias no suporte e promoção de dtypes, na velocidade e execução, e na documentação. Também tem havido trabalho preparatório para a futura versão 2.0.0, resultando em um grande número de depreciações novas e expiradas.

Um total de 148 pessoas contribuíram para este lançamento e 530 pull requests foram incorporadas.

As versões do Python suportadas por esta versão são 3.9-3.11.

### Promovendo uma cultura inclusiva: Chamada de participação

_10 de maio de 2023_ -- Promovendo uma Cultura Inclusiva: Chamada de Participação

Como podemos ser melhores quando se trata de diversidade e de inclusão?
Leia o relatório e descubra como colaborar [aqui](https://contributor-experience.org/docs/posts/dei-report/).

### Transição de liderança do time de documentação do NumPy

_6 de janeiro de 2023_ –- Mukulika Pahari e Ross Barnowski são nomeados como lideres do time de documentação do NumPy, substituindo Melissa Mendonça. Agradecemos a Melissa por todas suas contribuições para a documentação oficial do NumPy e materiais educacionais, e Mukulika e Ross por aceitarem o desafio.

### NumPy versão 1.23.0

_16 de setembro de 2023_ -- [NumPy 1.26.0](https://numpy.org/doc/stable/release/1.26.0-notes.html) está disponível. Os destaques desta versão são:

- Novas palavras-chave "dtype" e "casting" para funções que atuam com stacking.
- Novas funcionalidades e correções do F2PY.
- Muitas depreciações novas, confira.
- Muitas depreciações expiradas.

A versão 1.24.0 do NumPy continua o trabalho de melhorias no suporte e promoção de dtypes, na velocidade e execução, e na documentação.
Há um grande número de depreciações novas e expiradas devido a mudanças na promoção de dtypes e limpezas no código. É o trabalho de 177 contribuidores espalhados em 444 pull requests. As versões suportadas do Python são 3.8-3.11.

### NumPy versão 1.23.0

_22 de junho de 2022_ -- O [NumPy 1.23.0](https://numpy.org/doc/stable/release/1.23.0-notes.html) está disponível. Os destaques desta versão são:

- Implementação de `loadtxt` em C, melhorando muito seu desempenho.
- Exposição do DLPack ao nível de Python para facilitar a troca de dados.
- Mudanças na promoção e comparações de dtypes estruturados.
- Melhorias no f2py.

A versão 1.23.0 do NumPy continua o trabalho de melhorias no suporte e promoção de dtypes, na velocidade de execução, na documentação e na expiração de depreciações. É o trabalho de 151 contribuidores espalhados em 494 pull requests. As versões do Python suportadas por esta versão são 3.8-3.10.
Python 3.11 será suportado quando chegar na etapa rc.

### Pesquisa NumFOCUS DEI: chamada para participação

_13 de abril de 2022_ -- O NumPy está trabalhando com a [NumFOCUS](http://numfocus.org/) em um projeto de pesquisa financiado pela Gordon & Betty Moore Foundation para entender as barreiras à participação que contribuidores, especialmente aqueles de grupos historicamente subrepresentados, enfrentam na comunidade open source. A equipe da pesquisa gostaria de falar com novos colaboradores, desenvolvedores e mantenedores, e aqueles que contribuíram no passado sobre suas experiências contribuindo para o NumPy.

**Quer compartilhar suas experiências?**

Por favor, preencha este breve formulário: ["Participant Interest form"](https://numfocus.typeform.com/to/WBWVJSqe) que contém informações adicionais sobre os objetivos da pesquisa, privacidade e considerações de confidencialidade. Sua participação será valiosa para o crescimento e sustentabilidade de comunidades de software de código aberto diversas e inclusivas. Os participantes aceitos participarão de uma entrevista de 30 minutos com um membro da equipe de pesquisa.

### NumPy versão 1.22.0

_23 de junho de 2021_ -- O [NumPy 1.21.0](https://numpy.org/doc/stable/release/1.21.0-notes.html) está disponível. Os destaques desta versão são:

- Anotações de tipo do namespace principal estão praticamente completas. Upstream é um alvo em movimento, então provavelmente haverá mais melhorias, mas a maior parte do trabalho está feita. Esta é provavelmente a melhoria mais visível para os usuários nesta versão.
- Uma versão preliminar da proposta do [array API Standard](https://data-apis.org/array-api/latest/) está disponível (veja [NEP 47](https://numpy.org/neps/nep-0047-array-api-standard.html)).
  Este é um passo na criação de uma coleção padrão de funções que podem ser compartilhadas entre bibliotecas como CuPy e JAX.
- NumPy agora tem um backend de DLPack. DLPack fornece um formato comum de compartilhamento para dados de arrays (tensores).
- Novos métodos para `quantile`, `percentile`, e funções relacionadas. Os novos métodos fornecem um conjunto completo dos métodos comumente encontrados na literatura.
- As funções universais foram refatoradas para implementar a maior parte da [NEP 43](https://numpy.org/neps/nep-0043-extensible-ufuncs.html).
  Isso também desbloqueia a capacidade de experimentar a futura API DType.
- Um novo alocador de memória configurável para uso pelos projetos downstream.

NumPy 1.22.0 é uma versão importante com o trabalho de 153 contribuidores espalhados por mais de 609 pull requests. As versões do Python suportadas por esta versão são 3.8-3.10.

### Promovendo uma cultura inclusiva no ecossistema científico de Python

_31 de agosto de 2021_ -- Estamos felizes em anunciar que a Chan Zuckerberg Initiative [vai financiar](https://chanzuckerberg.com/newsroom/czi-awards-16-million-for-foundational-open-source-software-tools-essential-to-biomedicine/) um projeto para apoiar a integração, inclusão, e retenção de pessoas de grupos marginalizados historicamente em projetos científicos em Python, e para estruturalmente melhorar a dinâmica das comunidades para o NumPy, SciPy, Matplotlib, e Pandas.

Como parte do programa [CZI's Essential Open Source Software for Science](https://chanzuckerberg.com/eoss/), esse [financiamento adicional para diversidade e inclusão](https://cziscience.medium.com/advancing-diversity-and-inclusion-in-scientific-open-source-eaabe6a5488b) vai apoiar a criação de posições de Contributor Experience Lead para identificar, documentar e implementar práticas para fomentar comunidades open source inclusivas. Este projeto será liderado por Melissa Mendonça (NumPy), com apoio adicional de Ralf Gommers (NumPy, SciPy), Hannah Aizenman e Thomas Caswell (Matplotlib), Matt Haberland (SciPy), e Joris Van den Bossche (Pandas).

Esse é um projeto ambicioso que visa descobrir e implementar atividades que devem estruturalmente melhorar a dinâmica da comunidade de nossos projetos. Ao criar essas novas funções entre projetos, esperamos introduzir um novo modelo de colaboração às comunidades de Python científico, permitir que o trabalho de construção da comunidade no ecossistema seja feito de forma mais eficiente e com maiores resultados. Também esperamos desenvolver uma imagem mais clara do que funciona e o que não funciona em nossos projetos para engajar e reter novos colaboradores, especialmente de grupos historicamente sub-representados. Finalmente, planejamos produzir relatórios detalhados sobre as ações executadas, explicando como eles afetaram nossos projetos em termos de representação e interação com nossas comunidades.

O projeto de dois anos deverá começar em novembro de 2021 e estamos animados para ver os resultados deste trabalho!
[Você pode ler a proposta completa aqui](https://figshare.com/articles/online_resource/Advancing_an_inclusive_culture_in_the_scientific_Python_ecosystem/16548063).

### Pesquisa NumPy 2021

_12 de julho de 2021_ -- Nós do NumPy acreditamos no poder da nossa comunidade. 1.236 usuários do NumPy de 75 países participaram da nossa primeira pesquisa ano passado.
Os resultados da pesquisa nos ajudaram a compreender muito bem o que devemos fazer pelos 12 meses seguintes.

Chegou a hora de fazer outra pesquisa e estamos contando com você novamente. Vai levar cerca de 15 minutos do seu tempo. Além de Inglês, o questionário de pesquisa está disponível em 8 idiomas adicionais: Bangla, Francês, Hindi, Japonês, Mandarim, Português, Russo e Espanhol.

Siga o link para começar: https://berkeley.qualtrics.com/jfe/form/SV_aaOONjgcBXDSl4q.

### NumPy versão 1.19.0

_23 de junho de 2021_ -- O [NumPy 1.21.0](https://numpy.org/doc/stable/release/1.21.0-notes.html) está disponível. Os destaques desta versão são:

- continuamos o trabalho com SIMD para suportar mais funções e plataformas,
- trabalho inicial na infraestrutura e conversão de novos dtypes,
- wheels universal2 para Python 3.8 e Python 3.9 no Mac,
- melhorias na documentação,
- melhorias nas anotações de tipos,
- novo bitgenerator `PCG64DXSM` para números aleatórios.

Esta versão do NumPy é o resultado de 581 pull requests aceitos, a partir das contribuições de 175 pessoas.  As versões do Python suportadas por esta versão são 3.7-3.9; o suporte para o Python 3.10 será adicionado após o lançamento do Python 3.10.

### Resultados da pesquisa NumPy 2020

_22 de junho de 2021_ -- Em 2020, o time de pesquisas NumPy, em parceria com estudantes e professores da Universidade de Michigan e da Universidade de Maryland, realizou a primeira pesquisa oficial sobre a comunidade NumPy. Confira os resultados da pesquisa aqui: https://numpy.org/user-survey-2020/.

### NumPy versão 1.20.0

_30 de janeiro de 2021_ -- O [NumPy 1.20.0](https://numpy.org/doc/stable/release/1.20.0-notes.html) está disponível. Este é o maior lançamento do NumPy até hoje, graças a mais de 180 colaboradores. As duas novidades mais emocionantes são:

- Anotações de tipos para grandes partes do NumPy, e um novo submódulo `numpy.typing` contendo aliases `ArrayLike` e `DtypeLike` que usuários e bibliotecas downstream podem usar quando quiserem adicionar anotações de tipos em seu próprio código.
- Otimizações de compilação SIMD multi-plataforma, com suporte para instruções x86 (SSE, AVX), ARM64 (Neon) e PowerPC (VSX). Isso rendeu melhorias significativas de desempenho para muitas funções (exemplos: [sen/cos](https://github.com/numpy/numpy/pull/17587), [einsum](https://github.com/numpy/numpy/pull/18194)).

### Diversidade no projeto NumPy

_20 de setembro de 2020_ -- Escrevemos uma [declaração sobre o estado da diversidade e inclusão no projeto NumPy e discussões em redes sociais sobre isso.](/diversity_sep2020).

### Primeiro artigo oficial do NumPy publicado na Nature!

_16 de setembro de 2020_ -- Temos o prazer de anunciar a publicação do [primeiro artigo oficial do NumPy](https://www.nature.com/articles/s41586-020-2649-2) como um artigo de revisão na Nature. Isso ocorre 14 anos após o lançamento do NumPy 1.0.
O artigo abrange aplicações e conceitos fundamentais da programação de matrizes, o rico ecossistema científico de Python construído em cima do NumPy, e os protocolos de array recentemente adicionados para facilitar a interoperabilidade com bibliotecas externas para computação com matrizes e tensores, como CuPy, Dask e JAX.

### O Python 3.9 está chegando, quando o NumPy vai liberar wheels binárias?

_14 de setembro de 2020_ -- Python 3.9 será lançado em algumas semanas. Se você for querer usar imediatamente a nova versão do Python, você pode ficar desapontado ao descobrir que o NumPy (e outros pacotes binários como SciPy) não terão wheels no dia do lançamento. É um grande esforço adaptar a infraestrutura de compilação a uma nova versão de Python e normalmente leva algumas semanas para que os pacotes apareçam no PyPI e no conda-forge. Em preparação para este evento, por favor, certifique-se de

- atualizar seu `pip` para a versão 20.1 pelo menos para suportar `manylinux2010` e `manylinux2014`
- usar [`--only-binary=numpy`](https://pip.pypa.io/en/stable/reference/pip_install/#cmdoption-only-binary) ou `--only-binary=:all:` para impedir `pip` de tentar compilar a partir do código fonte.

### NumPy versão 1.18.0

_10 de setembro de 2020_ -- O [NumPy 1.19.2](https://numpy.org/devdocs/release/1.19.2-notes.html) está disponível.
Essa última versão da série 1.19 corrige vários bugs, inclui preparações para o lançamento [do Cython 3](http://docs.cython.org/en/latest/src/changes.html) e fixa o setuptools para que o distutils continue funcionando enquanto modificações upstream estão sendo feitas.
As wheels para aarch64 são compiladas com a manylinux2014 mais recente que conserta o problema da diferença no tamanho das páginas usadas por distribuições linux diferentes.

### A primeira pesquisa NumPy está aqui!

_2 de julho de 2020_ -- Esta pesquisa tem como objetivo guiar e definir prioridades para tomada de decisões sobre o desenvolvimento do NumPy como software e como comunidade.
A pesquisa está disponível em mais 8 idiomas além do inglês: Bangla, Hindi, Japonês, Mandarim, Português, Russo, Espanhol e Francês.

Ajude-nos a melhorar o NumPy respondendo à pesquisa [aqui](https://umdsurvey.umd.edu/jfe/form/SV_8bJrXjbhXf7saAl).

### O NumPy tem um novo logo!

_24 de junho de 2020_ -- NumPy agora tem um novo logo:

<img
src="/images/logos/numpy_logo.svg"
alt="NumPy logo"
title="The new NumPy logo"
width=300>

O logotipo é uma versão moderna do antigo, com um design mais limpo. Obrigado à Isabela Presedo-Floyd por projetar o novo logotipo, bem como ao Travis Vaught pelo o logotipo antigo que nos serviu bem durante mais de 15 anos.

### NumPy versão 1.19.0

_20 de junho de 2020_ -- O NumPy 1.19.0 está disponível. Esta é a primeira versão sem suporte ao Python 2, portanto foi uma "versão de limpeza". A versão mínima de Python suportada agora é Python 3.6. Uma característica nova importante é que a infraestrutura de geração de números aleatórios que foi introduzida na NumPy 1.17.0 agora está acessível a partir do Cython.

### Aceitação no programa Season of Docs

_11 de maio de 2020_ -- O NumPy foi aceito como uma das organizações mentoras do programa Google Season of Docs. Estamos animados com a oportunidade de trabalhar com um <em x-id="3">technical writer</em> para melhorar a documentação do NumPy mais uma vez! Estamos animados com a oportunidade de trabalhar com um _technical writer_ para melhorar a documentação do NumPy mais uma vez!

### NumPy versão 1.18.0

_22 de dezembro de 2019_ -- O NumPy 1.18.0 está disponível. Após as principais mudanças em 1.17.0, esta é uma versão de consolidação. É a última versão menor que suportará Python 3.5. Destaques dessa versão incluem a adição de uma infraestrutura básica para permitir o link com as bibliotecas BLAS e LAPACK em 64 bits durante a compilação, e uma nova C-API para `numpy.random`.

Por favor, veja as [notas de lançamento](https://github.com/numpy/numpy/releases/tag/v1.18.0) para mais detalhes.

### O NumPy recebe financiamento da Chan Zuckerberg Initiative

_15 de novembro de 2019_ -- Estamos felizes em anunciar que o NumPy e a OpenBLAS, uma das dependências-chave do NumPy, receberam um auxílio conjunto de $195,000 da Chan Zuckerberg Initiative através do seu programa [Essential Open Source Software for Science](https://chanzuckerberg.com/eoss/) que apoia a manutenção, crescimento, desenvolvimento e envolvimento da comunidade em ferramentas de código aberto fundamentais para a ciência.

Este auxílio será usado para aumentar os esforços de melhoria da documentação do NumPy, reformulação do site, desenvolvimento comunitário para melhor servir a nossa grande, e rapidamente crescente, base de usuários, assim como para garantir a sustentabilidade do projeto a longo prazo. Enquanto a equipe OpenBLAS se concentrará em tratar de um conjunto de questões técnicas fundamentais, em particular relacionadas a <em x-id="3">thread-safety</em>, AVX-512, e <em x-id="3">thread-local storage</em> (TLS), bem como melhorias algorítmicas na ReLAPACK (Recursive LAPACK) da qual a OpenBLAS depende.

Mais detalhes sobre nossas propostas e resultados esperados podem ser encontrados na [proposta completa de concessão de auxílio](https://figshare.com/articles/Proposal_NumPy_OpenBLAS_for_Chan_Zuckerberg_Initiative_EOSS_2019_round_1/10302167). O trabalho está agendado para começar no dia 1 de dezembro de 2019 e continuar pelos próximos 12 meses.

<a name="releases"></a>

## Lançamentos

Aqui está uma lista de versões do NumPy, com links para notas de lançamento. Lançamentos para correção de falhas (apenas o `z` muda no número de versão `x.y.z`) não tem novos recursos; versões menores (o `y` aumenta) sim.

- NumPy 2.2.5 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v2.2.5)) -- _19 Abr 2025_.
- NumPy 2.2.4 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v2.2.4)) -- _16 de março de 2025_.
- NumPy 2.2.3 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v2.2.3)) -- _13 de fevereiro de 2025_.
- NumPy 2.2.2 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v2.2.2)) -- _18 de janeiro de 2025_.
- NumPy 2.2.1 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v2.2.1)) -- _21 de dezembro de 2024_.
- NumPy 2.2.0 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v2.2.0)) -- _8 de dezembro de 2024_.
- NumPy 2.1.3 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v2.1.3)) -- _2 de novembro de 2024_.
- NumPy 2.1.2 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v2.1.2)) -- _5 de outubro de 2024_.
- NumPy 2.1.1 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v2.1.1)) -- _3 de setembro de 2024_.
- NumPy 2.0.2 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v2.0.2)) -- _26 de agosto de 2024_.
- NumPy 2.1.0 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v2.1.0)) -- _18 de agosto de 2024_.
- NumPy 2.0.1 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v2.0.1)) -- _21 de julho de 2024_.
- NumPy 2.0.0 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v2.0.0)) -- _16 de junho de 2024_.
- NumPy 1.26.4 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.26.4)) -- _5 de fevereiro de 2024_.
- NumPy 1.26.3 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.26.3)) -- _2 de janeiro de 2024_.
- NumPy 1.26.2 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.26.2)) -- _12 de novembro de 2023_.
- NumPy 1.26.1 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.26.1)) -- _14 de outubro de 2023_.
- NumPy 1.26.0 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.26.0)) -- _16 de setembro de 2023_.
- NumPy 1.25.2 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.25.2)) -- _31 de julho de 2023_.
- NumPy 1.25.1 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.25.1)) -- _8 de julho de 2023_.
- NumPy 1.24.4 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.24.4)) -- _26 de junho de 2023_.
- NumPy 1.25.0 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.25.0)) -- _17 de junho de 2023_.
- NumPy 1.24.3 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.24.3)) -- _22 de abril de 2023_.
- NumPy 1.24.2 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.24.2)) -- _5 de fevereiro de 2023_.
- NumPy 1.24.1 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.24.1)) -- _26 de dezembro de 2022_.
- NumPy 1.24.0 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.24.0)) -- _18 de dezembro de 2022_.
- NumPy 1.23.5 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.23.5)) -- _19 de novembro de 2022_.
- NumPy 1.23.4 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.23.4)) -- _12 de outubro de 2022_.
- NumPy 1.23.3 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.23.3)) -- _9 de setembro de 2022_.
- NumPy 1.23.2 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.23.2)) -- _14 de agosto de 2022_.
- NumPy 1.23.1 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.23.1)) -- _8 de julho de 2022_.
- NumPy 1.23.0 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.23.0)) -- _22 de junho de 2022_.
- NumPy 1.22.4 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.22.4)) -- _20 de maio de 2022_.
- NumPy 1.21.6 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.21.6)) -- _12 de abril de 2022_.
- NumPy 1.22.3 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.22.3)) -- _7 de março de 2022_.
- NumPy 1.22.2 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.22.2)) -- _3 de fevereiro de 2022_.
- NumPy 1.22.1 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.22.1)) -- _14 de janeiro de 2022_.
- NumPy 1.22.0 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.22.0)) -- _31 de dezembro de 2021_.
- NumPy 1.21.5 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.21.5)) -- _19 de dezembro de 2021_.
- NumPy 1.21.0 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.21.0)) -- _22 de junho de 2021_.
- NumPy 1.20.3 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.20.3)) -- _10 de maio de 2021_.
- NumPy 1.20.0 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.20.0)) -- _30 de janeiro de 2021_.
- NumPy 1.19.5 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.19.5)) -- _5 de janeiro de 2021_.
- NumPy 1.19.0 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.19.0)) -- _20 de junho de 2020_.
- NumPy 1.18.4 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.18.4)) -- _3 de maio de 2020_.
- NumPy 1.17.5 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.17.5)) -- _1 de janeiro de 2020_.
- NumPy 1.18.0 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.18.0)) -- _22 de dezembro de 2019_.
- NumPy 1.17.0 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.17.0)) -- _26 de julho de 2019_.
- NumPy 1.16.0 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.16.0)) -- _14 de janeiro de 2019_.
- NumPy 1.15.0 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.15.0)) -- _23 de julho de 2018_.
- NumPy 1.14.0 ([notas de versão](https://github.com/numpy/numpy/releases/tag/v1.14.0)) -- _7 de janeiro de 2018_.
