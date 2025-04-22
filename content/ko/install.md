---
title: NumPy 설치
sidebar: false
---

{{< admonition >}}
{{< /admonition >}}

The recommended method of installing NumPy depends on your preferred workflow. 아래에 설치 방법을 다음과 같이 분류하였습니다:

- **Project-based** (e.g., uv, pixi) _(recommended for new users)_
- **Environment-based** (e.g., pip, conda) _(the traditional workflow)_
- **System package managers** _(not recommended for most users)_
- **Building from source** _(for advanced users and development purposes)_

Choose the method that best suits your needs. If you're unsure, start with the **Environment-based** method using `conda` or `pip`.

{{< tabs >}}

[[tab]]
name = 'Project Based'
content = '''

Recommended for new users who want a streamlined workflow.

- **uv:** A modern Python package manager designed for speed and simplicity.
  ```bash
  uv pip install numpy
  ```

- **pixi:** A cross-platform package manager for Python and other languages.
  ```bash
  pixi add numpy
  ```

'''
{{< /card >}}

개인적인 선호나 아래의 conda 와 pip의 차이점을 설명하는 글을 읽은 유저나 또는 pip/PyPI기반의 설치 방법을 선호하는 경우 참고하십시오.

The two main tools that install Python packages are `pip` and `conda`. Their functionality partially overlaps (e.g. both can install `numpy`), however, they can also work together. 고성능 컴퓨터 (HPC) 를 사용하는 경우 <a href="https://github.com/spack/spack">Spack</a>를 사용하는 것을 추천합니다.

The first difference is that conda is cross-language and it can install Python, while pip is installed for a particular Python on your system and installs other packages to that same Python install only. 그 도구들의 기능은 부분적으로 겹칩지만 (e.g. both can install <code>numpy</code>), 같이 쓰일 수도 있습니다.

첫번째 차이점은, conda는 cross-language 를 지원하고, Python을 설치할 수 도 있지만, pip는 특정 Python에만 패키지를 설치하고 관리할 수 있다는 것 입니다. 또한 conda는 non-Python 라이브러리나 도구들을 설치할 수 있지만 (e.g. compilers, CUDA, HDF5), pip는 Python이 필요하기 때문에 설치할 수 없습니다.

The third difference is that conda is an integrated solution for managing packages, dependencies and environments, while with pip you may need another tool (there are many!) for dealing with environments or complex dependencies.

- **Conda:** If you use conda, you can install NumPy from the defaults or conda-forge channels:
  ```bash
  conda create -n my-env
  conda activate my-env
  conda install numpy
  ```
- **Pip:**
  ```bash
  pip install numpy
  ```

{{< admonition >}}
{{< /admonition >}}

  ```bash
  python -m venv my-env
  source my-env/bin/activate  # macOS/Linux
  my-env\Scripts\activate     # Windows
  pip install numpy
  ```

'''
{{< /card >}}

[[tab]]
name = 'System Package Managers'
content = '''
Not recommended for most users, but available for convenience.

**macOS (Homebrew):**

```bash
# 가장 좋은 방법은 기본 환경 대신에 새로운 환경을 이용하는 것입니다
conda create -n my-env
conda activate my-env
# my-env 에 conda-forge 채널을 더해줍니다
conda config --env --add channels conda-forge
# my-env 에 NumPy 를 설치합니다
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

A word of warning: building Numpy from source can be a nontrivial exercise.
We recommend using binaries instead if those are available for your platform via one of the above methods.
For details on how to build from source, see [the building from source guide in the Numpy docs](https://numpy.org/devdocs/building/).

{{< /tabs >}}

## 권장 사항

After installing NumPy, verify the installation by running the following in a Python shell or script:

```python
import numpy as np
print(np.__version__)
```

This should print the installed version of NumPy without errors.

## 트러블슈팅

If your installation fails with the message below, see Troubleshooting
ImportError.

```
IMPORTANT: PLEASE READ THIS FOR ADVICE ON HOW TO SOLVE THIS ISSUE!

Importing the numpy c-extensions failed. This error can happen for
different reasons, often due to issues with your setup.
```

