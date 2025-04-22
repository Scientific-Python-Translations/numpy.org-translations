---
title: "사례 연구: 최초의 블랙홀 사진"
sidebar: false
---

{{< figure >}}
{{< /figure >}}

{{< blockquote
  cite="https://www.youtube.com/watch?v=BIvezCVcsYs"
  by="Katie Bouman, _Assistant Professor, Computing & Mathematical Sciences, Caltech_"
>}}
{{< /blockquote >}}

## 지구 크기의 망원경

[사건의 지평선 전파 망원경 (EHT)](https://eventhorizontelescope.org) 은 8개의 지상 전파 망원경을 연결하여 지구 크기의 가상의 전파 망원경을 만들어서 우주를 전례 없는 감도와 해상도로 연구하고자 하는 것입니다.  해당 거대 가상 전파 망원경이 사용하는 기술은 매우 긴 기준선을 가지는 간섭계라고 (VLBI) 하며, 각 해상도는 \[20 micro-arcseconds]에 달하는데, [resolution] — 뉴욕의 신문을 파리의 길가의 카페에서 읽을 수 있는 수준입니다!

[resolution]: https://eventhorizontelescope.org/press-release-april-10-2019-astronomers-capture-first-image-black-hole

### 주요 목표 및 결과

- **새로운 우주를 바라보는 시각**
  EHT의 획기적인 이미지를 위한 초석은 100 년 전
  [아서 에딩턴][eddington]경이 아인시타인의 일반 상대성 이론을 뒷받침하는 첫번째 관측 증거를 얻었을 때 놓여졌습니다.

- **블랙홀** EHT 는 지구로부터 대략 5천5백만광년 떨어진, 처녀자리 은하단에 속한 메시에 87 은하 (M87) 중심에 놓여 있는 초거대블랙홀에 최적화 되었습니다. Its mass is
  6.5 billion times the Sun's. It had been studied for
  [over 100 years](https://www.jpl.nasa.gov/news/news.php?feature=7385), but never before
  had a black hole been visually observed.

- **Comparing Observations to Theory:** From Einstein’s general theory of
  relativity, scientists expected to find a shadow-like region caused by
  gravitational bending and capture of light. Scientists could
  use it to measure the black hole's enormous mass.

[eddington]: https://en.wikipedia.org/wiki/Eddington_experiment

### 도전

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

## NumPy의 역할

데이터에 만약 문제가 있다면 어떨까요? 아니면 알고리즘이 특정 가정에 지나치게 의존할 수도 있습니다. 매개변수 하나만 달라져도 사진이 크게 바뀔까요?

EHT는 기존 및 최첨된 이미지 재구성 기술을 모두 사용한 뒤, 개개의 팀이 데이터를 평가하도록 하여 이런 문제를 해결했습니다. 결과가 일관적이라는 것을 검증한 뒤, 이들을 결합해 최초의 블랙홀 이미지를 만들어내었습니다.

그들의 연구는 협업 데이터 분석을 통해 과학을 발전시키는 과학적인 Python 생태계의 역할을 보여줍니다.

{{< figure >}}
{{< /figure >}}

For example, the [`eht-imaging`][ehtim] Python package provides tools for
simulating and performing image reconstruction on VLBI data.
NumPy는 아래 소프트웨어 종속성 차트에 나와 있는 것처럼 이 패키지에서 사용되는 배열 데이터 처리의 핵심 역할을 합니다.

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

## 요약

NumPy의 핵심 기능인 효율적이고 유용한 n차원 배열은 연구자들이 대규모 수치 데이터셋을 다룰 수 있도록 하여 최초의 블랙홀 사진을 만드는 데 토대를 제공했습니다. 이번 관측은 아인슈타인의 이론에 훌륭한 시각적 증거를 준 관측으로, 과학계에 한 획을 그은 순간이었습니다. 기술적 혁신뿐만 아니라 200명 이상의 과학자와 세계 최고의 전파 관측소 간의 국제 협력도 이루어 냈습니다.  기존의 천문학 모델을 개선한 혁신적인 알고리즘과 데이터 처리 기술이 우주의 비밀을 알아내는 데 도움을 주었습니다.

{{< figure >}}
{{< /figure >}}
