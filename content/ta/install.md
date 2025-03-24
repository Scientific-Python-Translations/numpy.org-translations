---
title: NumPy ஐ நிறுவுதல்
sidebar: false
---

{{< admonition >}}
{{< /admonition >}}

The recommended method of installing NumPy depends on your preferred workflow. Below, we break down the installation methods into the following categories:

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

    uv pip install numpy

- **pixi:** A cross-platform package manager for Python and other languages.

    pixi add numpy

'''

[[tab]]
name = 'Environment Based'
content = '''

The two main tools that install Python packages are `pip` and `conda`. Their functionality partially overlaps (e.g. both can install `numpy`), however, they can also work together. We’ll discuss the major differences between pip and conda here - this is important to understand if you want to manage packages effectively.

The first difference is that conda is cross-language and it can install Python, while pip is installed for a particular Python on your system and installs other packages to that same Python install only. This also means conda can install non-Python libraries and tools you may need (e.g. compilers, CUDA, HDF5), while pip can’t.

The second difference is that pip installs from the Python Packaging Index (PyPI), while conda installs from its own channels (typically “defaults” or “conda-forge”). PyPI is the largest collection of packages by far, however, all popular packages are available for conda as well.

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

[[tab]]
name = 'System Package Managers'
content = '''
Not recommended for most users, but available for convenience.

**macOS (Homebrew):**

```bash
brew install numpy
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

[[tab]]
name = 'Building from Source'
content = '''
For advanced users and developers who want to customize or debug **NumPy**.

A word of warning: building Numpy from source can be a nontrivial exercise.
We recommend using binaries instead if those are available for your platform via one of the above methods.
For details on how to build from source, see [the building from source guide in the Numpy docs](https://numpy.org/devdocs/building/).

{{< /tabs >}}

## Verifying the Installation

After installing NumPy, verify the installation by running the following in a Python shell or script:

```python
import numpy as np
print(np.__version__)
```

This should print the installed version of NumPy without errors.

## Troubleshooting

If your installation fails with the message below, see Troubleshooting
ImportError.

```
IMPORTANT: PLEASE READ THIS FOR ADVICE ON HOW TO SOLVE THIS ISSUE!

Importing the numpy c-extensions failed. This error can happen for
different reasons, often due to issues with your setup.
```

