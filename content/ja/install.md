---
title: NumPyのインストール
sidebar: false
---

{{< admonition >}}
{{< /admonition >}}

NumPy のインストールする推奨の方法は、希望するワークフローによって異なります。 そこで、インストール方法を以下のカテゴリに分類しました。

- **Project-based** (e.g., uv, pixi) _(recommended for new users)_
- **Environment-based** (e.g., pip, conda) _(the traditional workflow)_
- **System package managers** _(not recommended for most users)_
- **Building from source** _(for advanced users and development purposes)_

あなたの目的に応じて最適な方法を選択してください。 If you're unsure, start with the **Environment-based** method using `conda` or `pip`.

{{< tabs >}}

[[tab]]
name = 'プロジェクトベースの方法'
content = '''

合理的なワークフローを求める、新規ユーザーにお勧めです。

- **uv:** A modern Python package manager designed for speed and simplicity.

    uv pip install numpy

- **pixi:** A cross-platform package manager for Python and other languages.

    pixi add numpy



個人的な好みや、下記のcondaとpipの違いを理解した上で、pip/PyPIベースの方法を使いたいユーザーには、下記をお勧めします:

The two main tools that install Python packages are `pip` and `conda`. Their functionality partially overlaps (e.g. both can install `numpy`), however, they can also work together. ハイパフォーマンスコンピューティング(HPC)では、 <a href="https://github.com/spack/spack">Spack</a> を使うことを検討して下さい。

pipとcondaの最初の違いは、Conda は複数の言語に対応しており Python 自体をインストールできるのに対し、pip は特定の Python 環境にインストールされ、その Python に対してのみパッケージをインストールすることができることです。 これら二つのツールの機能は部分的に重複しますが(例えば、両方とも <code>numpy</code>をインストールできます)、一緒に動作することもできます。

2つ目の違いは、pipはPython Packaging Index(PyPI) からパッケージをインストールするのに対し、condaは独自のチャンネル(一般的には "defaults "や "conda-forge "など) からインストールすることです。 PyPIは最大のパッケージ管理システムですが、人気のある全てのパッケージがcondaでも利用可能です。

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



[[tab]]
name = 'システムパッケージマネージャを利用'
content = '''
ほとんどのユーザーには推奨されませんが、こちらの方が便利な人向けに利用可能です。

**macOS (Homebrew):**

```bash
# base envにインストールするのでなく、environmentを作成するのがベストプラクティスです
conda create -n my-env
conda activate my-env
# conda-forgeからインストールする場合
conda config --env --add channels conda-forge
# インストールコマンド
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



[[tab]]
name = 'Building from Source'
content = '''
For advanced users and developers who want to customize or debug **NumPy**.

警告:ソースコードからNumPyをビルドすることは簡単では無い場合があります。
前述のいずれかの方法であなたの環境NumPyを使用できる場合は、バイナリを使用することをお勧めします.
For details on how to build from source, see [the building from source guide in the Numpy docs](https://numpy.org/devdocs/building/).

{{< /tabs >}}

## 推奨方法

NumPy をインストールした後、以下のコードをPython シェルまたはスクリプトで実行して、インストールが正しく実施されているか確認してください。

```python
import numpy as np
print(np.__version__)
```

インストールに問題が無い場合は、インストールされているNumPyのバージョンが表示されるはずです。

## トラブルシューティング

If your installation fails with the message below, see Troubleshooting
ImportError.

```
IMPORTANT: PLEASE READ THIS FOR ADVICE ON HOW TO SOLVE THIS ISSUE!

Importing the numpy c-extensions failed. This error can happen for
different reasons, often due to issues with your setup.
```

