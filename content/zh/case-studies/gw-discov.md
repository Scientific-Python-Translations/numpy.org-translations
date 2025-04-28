---
title: 案例研究：发现引力波
sidebar: false
---

{{< figure >}}
{{< /figure >}}

{{< blockquote
  cite="https://www.youtube.com/watch?v=BIvezCVcsYs"
  by="David Shoemaker, _LIGO Scientific Collaboration_" >}}
{{< /blockquote >}}

## 关于 [引力波](https://www.nationalgeographic.com/news/2017/10/what-are-gravitational-waves-ligo-astronomy-science/) and [LIGO](https://www.ligo.caltech.edu)

引力波是空间和时间结构中的涟漪。由宇宙中的灾难性事件产生，例如两个黑洞的碰撞和合并或双星或超新星的合并。 观测引力波不仅有助于研究引力，而且有助于了解遥远宇宙中一些不为人知的现象及其影响。

[激光干涉引力波天文台(LIGO)](https://www.ligo.caltech.edu)旨在通过直接探测爱因斯坦广义相对论预测的引力波来打开引力波天体物理学领域。 It comprises two widely separated interferometers within the United States — one in Hanford, Washington and the other in Livingston, Louisiana — operated in unison to detect gravitational waves. It comprises two widely separated interferometers within the
United States — one in Hanford, Washington and the other in Livingston,
Louisiana — operated in unison to detect gravitational waves. 每一个仪器都装载使用了激光干涉测量法的公里级引力波探测器。  LIGO科学计算团队(LSC) 是由来自美国各地大学和其他 14 个国家的 1000 多名科学家组成的团体，得到了 90 多所大学和研究机构的支持；大约 250 名学生积极参与项目合作。 LIGO 的新发现是关于对引力波本身的首次观测，通过测量引力波在穿过地球时对空间和时间造成的微小扰动而制成。  它开辟了新的天体物理学研究方向，致力于探索宇宙扭曲的一面—研究由扭曲的时空构成的物体和现象。

### 关键目标

- 虽然它的 [任务](https://www.ligo.caltech.edu/page/what-is-ligo) 是探测宇宙中反应最剧烈和能量最集中的区域产生的引力波，但 LIGO 收集的数据可能会对物理学的许多领域产生深远的影响，包括引力、相对论、天体物理学、宇宙学、粒子物理学和核物理。
- 通过涉及复杂数学的数值相对论来计算和处理观测数据，以便从噪声中辨别信号、滤除相关信号并统计估计观测数据的重要性。
- 数据可视化，以便可以理解二进制/数值结果。

### 面临的挑战

- **计算**

  Gravitational Waves are hard to detect as they produce a very small effect
  and have tiny interaction with matter. Processing and analyzing all of
  LIGO's data requires a vast computing infrastructure.After taking care of
  noise, which is billions of times of the signal, there is still very
  complex relativity equations and huge amounts of data which present a
  computational challenge:
  [O(10^7) CPU hrs needed for binary merger analyses](https://youtu.be/7mcHknWWzNI)
  spread on 6 dedicated LIGO clusters

- **数据泛滥**

  As observational devices become more sensitive and reliable, the challenges
  posed by data deluge and finding a needle in a haystack rise multi-fold.
  LIGO 每天生成数 TB 的数据！ Making sense of this data
  requires an enormous effort for each and every detection. For example, the
  signals being collected by LIGO must be matched by supercomputers against
  hundreds of thousands of templates of possible gravitational-wave signatures.

- **可视化**

  Once the obstacles related to understanding Einstein’s equations well
  enough to solve them using supercomputers are taken care of, the next big
  challenge was making data comprehensible to the human brain. Simulation
  modeling as well as  signal detection requires effective visualization
  techniques.  Visualization also plays a role in lending more credibility
  to numerical relativity in the eyes of pure science aficionados, who did
  not give enough importance to numerical relativity until imaging and
  simulations made it easier to comprehend results for a larger audience.
  Speed of complex computations and rendering, re-rendering images and
  simulations using latest experimental inputs and insights can be a time
  consuming activity that challenges researchers in this domain.

{{< figure >}}
{{< /figure >}}

## Numpy 在引力波检测中的作用

除了使用超级计算机暴力计算数值相对论之外，目前还无法使用任何其它技术计算黑洞合并发出的引力波。
LIGO 收集的数据量之大，就像无比微弱的引力波信号一样，令人难以置信。

NumPy 是 Python 的标准数值分析包，被用于 LIGO GW 检测项目期间执行的各种任务的软件所使用。 NumPy 有助于高性能处理复杂的数学问题和数据操作。  这里有一些例子：

- [信号处理](https://www.uv.es/virgogroup/Denoising_ROF.html): 毛刺检测,  [噪音识别和数据表征](https://ep2016.europython.eu/media/conference/slides/pyhton-in-gravitational-waves-research-communities.pdf) (NumPy, scikit-learn, scipy, matplab, pandas, pyCharm)
- 数据检索：决定哪些数据可以用于分析，确定它是否包含信号—犹如大海捞针
- 统计分析：估计观测数据的统计显著性，通过与模型比较来估计信号参数(如恒星质量、自旋速度和距离)。
- 数据可视化
  - 时间序列
  - 频谱图
- 计算相关性
- 在GW 数据分析中开发的关键 [软件](https://github.com/lscsoft) 例如： [GwPy](https://gwpy.github.io/docs/stable/overview.html) 和 [PyCBC](https://pycbc.org) 使用 NumPy 和 AstroPy 为实用程序、工具和方法提供基于对象的接口，用于研究来自引力波探测器的数据。

{{< figure >}}
{{< /figure >}}

----

{{< figure >}}
{{< /figure >}}

## 总结

GW 探测使研究人员能够发现完全出乎意料的现象，同时为许多已知的最深刻的天体物理现象提供了新的见解。 数学运算和数据可视化是帮助科学家深入了解从科学观察中收集到的数据并理解结果的关键步骤。 计算是复杂的，除非使用计算机模拟进行可视化，并提供真实的观察数据和分析，否则人类无法理解。  NumPy
along with other Python packages such as matplotlib, pandas, and scikit-learn
is [enabling researchers](https://www.gw-openscience.org/events/GW150914/) to
answer complex questions and discover new horizons in our understanding of the
universe.

{{< figure >}}
{{< /figure >}}
