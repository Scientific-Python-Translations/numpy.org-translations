---
title: 配列演算
sidebar: false
---

_Array computing is the foundation of statistical, mathematical, scientific computing
in various contemporary data science and analytics applications such as data
visualization, digital signal processing, image processing, bioinformatics,
machine learning, AI, and several others._

大規模なデータ処理やデータ変換には、効率的な配列演算が重要です。 The language of choice for data analytics,
machine learning, and productive numerical computing is **Python.**

**Num**erical **Py**thon or NumPy is its de-facto standard Python programming
language library that supports large, multi-dimensional arrays and matrices,
and comes with a vast collection of high-level mathematical functions to
operate on these arrays.

2006年にNumPyが発表されてから、2008年にPandasが登場し、その後、数年間にいくつかの配列演算関連のライブラリが次々と現れるようになりました。
これらの新しい配列演算ライブラリの多くは、NumPyの機能や能力を模倣しており、機械学習や人工知能向けの新しいアルゴリズムや機能を持っています。

<img
src="/images/content_images/array_c_landscape.png"
alt="arraycl"
title="Array Computing Landscape">

**Array computing** is based on **arrays** data structures. _Arrays_ are used
to organize vast amounts of data such that a related set of values can be easily
sorted, searched, mathematically manipulated, and transformed easily and quickly.

Array computing is _unique_ as it involves operating on the data array _at
once_. これは、配列操作が一回の処理で、配列内の 全ての値に適用されることを意味しています。 このベクトル化手法は、速さと単純さという恩恵をもたらします。 プログラマーはループを回して個々の要素のスカラー演算を行うことなく、データの集合を操作しコーディングすることができるのです。
