---
title: Instalando o NumPy
sidebar: false
---

{{< admonition >}}
{{< /admonition >}}

O método recomendado de instalar o NumPy depende do seu fluxo de trabalho preferido. A seguir, dividimos os métodos de instalação entre as seguintes categorias:

- **Project-based** (e.g., uv, pixi) _(recommended for new users)_
- **Environment-based** (e.g., pip, conda) _(the traditional workflow)_
- **System package managers** _(not recommended for most users)_
- **Building from source** _(for advanced users and development purposes)_

Escolha o método mais adequado às suas necessidades. If you're unsure, start with the **Environment-based** method using `conda` or `pip`.

{{< tabs >}}

[[tab]]
name = 'Baseados em projetos'
conteúdo = '''

Recomendado para novos usuários que queiram um fluxo de trabalho simplificado.

- **uv:** A modern Python package manager designed for speed and simplicity.

    uv pip install numpy

- **pixi:** A cross-platform package manager for Python and other languages.

    pixi add numpy

'''
{{< /card >}}

Para usuários que preferem uma solução baseada em pip/PyPI, por preferência pessoal ou leitura sobre as principais diferenças entre o conda e o pip explicadas adiante, nós recomendamos:

The two main tools that install Python packages are `pip` and `conda`. Their functionality partially overlaps (e.g. both can install `numpy`), however, they can also work together. Para computação de alto desempenho (HPC), vale a pena considerar o <a href="https://github.com/spack/spack">Spack</a>.

A primeira diferença é que conda é multilinguagens e pode instalar o Python, enquanto o pip é instalado em um determinado Python em seu sistema e instala outros pacotes apenas para essa mesma instalação de Python. Elas têm algumas funcionalidades em comum (por exemplo, ambas podem instalar o <code>numpy</code>). No entanto, elas também podem trabalhar juntas.

A primeira diferença é que "conda" é multilinguagens e pode instalar o Python, enquanto o pip é instalado em um determinado Python em seu sistema e instala outros pacotes apenas para essa mesma instalação de Python. Isto também significa que o conda pode instalar bibliotecas e ferramentas não-Python das quais você pode precisar (por exemplo, compiladores, CUDA, HDF5), enquanto pip não pode.

The third difference is that conda is an integrated solution for managing packages, dependencies and environments, while with pip you may need another tool (there are many!) for dealing with environments or complex dependencies.

- **Conda:** If you use conda, you can install NumPy from the defaults or conda-forge channels:

    conda create -n my-env
    conda activate my-env
    conda install numpy
- **Pip:**

    pip install numpy

{{< admonition >}}
{{< /admonition >}}

  python -m venv my-env
  source my-env/bin/activate  # macOS/Linux
  my-env\Scripts\activate     # Windows
  pip install numpy

'''
{{< /card >}}

[[tab]]
name = 'Gerenciadores de Pacotes do Sistema'
conteúdo = '''
Não recomendado para a maioria dos usuários, mas disponível por conveniência.

**macOS (Homebrew):**

```bash
# Recomenda-se usar um ambiente novo ao invés de instalar no ambiente-base
conda create -n my-env
conda activate my-env
# Se quiser instalar do conda-forge
conda config --env --add channels conda-forge
# O comando para instação
conda install numpy
```

**Linux (APT):**

```bash
sudo apt install python3-numpy
```

**Windows (Chocolatey):**

```bash
choco install numpy
```

'''
{{< /card >}}

[[tab]]
name = 'Building from Source'
content = '''
For advanced users and developers who want to customize or debug **NumPy**.

Um pequeno aviso: construir o Numpy a partir do código-fonte pode ser um exercício não-trivial.
Recomendamos o uso de binários se eles estiverem disponíveis para a sua plataforma através de um dos métodos anteriores.
For details on how to build from source, see [the building from source guide in the Numpy docs](https://numpy.org/devdocs/building/).

{{< /tabs >}}

## Recomendações

Depois de instalar o NumPy, verifique a instalação, executando o seguinte em um shell ou script Python:

```python
import numpy as np
print(np.__version__)
```

Isto deve imprimir a versão instalada do NumPy sem erros.

## Solução de problemas

If your installation fails with the message below, see Troubleshooting
ImportError.

```
IMPORTANT: PLEASE READ THIS FOR ADVICE ON HOW TO SOLVE THIS ISSUE!

Importing the numpy c-extensions failed. This error can happen for
different reasons, often due to issues with your setup.
```

