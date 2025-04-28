---
title: 案例研究：通过数据分析玩转板球！
sidebar: false
---

{{< figure
 src='/images/content_images/cs/ipl-stadium.png'
 >}}
{{< /figure >}}

{{< blockquote
 cite="印度人喜欢板球几乎人尽皆知。 这个游戏几乎在印度的任何角落都可以玩，无论是农村还是城市，与其它任何运动项目相比，只有板球可以轻松连接印度的数十亿年轻人和老年人。 板球受到了媒体的广泛关注。 无数 [金钱](https://www.statista.com/topics/4543/indian-premier-league-ipl/) 和 荣誉都压宝在这项运动上。 在过去的几年中，数据技术分析确实成为了运动场上的常胜将军。 流媒体、锦标赛、在移动设备上实时的观看板球等形式让不同观众的观看欲望得到最大满足。"
 by="{{< blockquote cite="https://www.scoopwhoop.com/sports/ms-dhoni/" by="M S Dhoni, _International Cricket Player, ex-captain, Indian Team, plays for Chennai Super Kings in IPL_""
>}}
{{< /blockquote >}}

## 关于板球

印度人喜欢板球几乎人尽皆知。 这个游戏几乎在印度的任何角落都可以玩，无论是农村还是城市，与其它任何运动项目相比，只有板球可以轻松连接印度的数十亿年轻人和老年人。
板球受到了媒体的广泛关注。 There is a significant amount of
[money](https://www.statista.com/topics/4543/indian-premier-league-ipl/) and
fame at stake. 在过去的几年中，数据技术分析确实成为了运动场上的常胜将军。 流媒体、锦标赛、在移动设备上实时的观看板球等形式让不同观众的观看欲望得到最大满足。

印度超级联赛(IPL) 是成立于2008年的Twenty20板球职业联赛。 It is one of the most attended cricketing events in
the world, valued at [$6.7 billion](https://en.wikipedia.org/wiki/Indian_Premier_League)
in 2019.

板球本质上是关于数字的游戏-击球方的跑动得分，投球手击中门柱的次数，板球队赢得回合的次数，击球手以特定方式还击的次数等等。 借助类似Numpy等功能强大的数值计算分析软件，可以充分挖掘板球得分背后的原理，并对板球的商业化、市场化和经济效益提供重要的参考价值。 板球数据分析为比赛提供了独特的视角，并提供了有关比赛结果的智能预测。

时至今日，板球比赛的记录和统计数据非常丰富，几乎无穷无尽。例如[ESPN cricinfo](https://stats.espncricinfo.com/ci/engine/stats/index.html) 和 [cricsheet](https://cricsheet.org)。 这些板球数据库使用最新的机器学习和预测建模算法来进行 [板球分析](https://www.researchgate.net/publication/336886516_Data_visualization_and_toss_related_analysis_of_IPL_teams_and_batsmen_performances)。 媒体和娱乐平台以及与游戏相关联的专业体育机构使用技术分析来确定关键指标，以提高比赛获胜机率： These and several such cricket databases
have been used for cricket
analysis
using the latest machine learning and predictive modelling algorithms.
媒体和娱乐平台以及与游戏相关联的专业体育机构使用技术分析来确定关键指标，以提高比赛获胜机率：

- 击球时跑动步数均值的表现
- 分数预测
- 深入了解球员在面对不同对手时的身体表现状况
- 在团队组成的决策过程中考察球员对比赛输赢的贡献值

{{< figure >}}
{{< /figure >}}

### 关键数据分析目标

- 运动数据分析不仅用于板球运动，还适用于 [其它运动](https://adtmag.com/blogs/dev-watch/2017/07/sports-analytics.aspx) 中，以改善团队的整体表现并最大程度的提高获胜机会。
- 实时数据分析甚至可以在比赛过程中帮助提高洞察力，从而使团队和相关投资方改变比赛策略以获取更高的经济效益。
- 除了历史数据分析之外，预测模型也被使用来确定可能的比赛结果，这些结果需要大量的数值处理和数据科学专业知识， 可视化工具以及在分析中增加新观察项的能力。

{{< figure >}}
{{< /figure >}}

### 面临的挑战

- **数据清理和预处理**

 IPL has expanded cricket beyond the classic test match format to a much
 larger scale. The number of matches played every season across various
 formats has increased and so has the data, the algorithms, newer sports data
 analysis technologies and simulation models. Cricket data analysis requires
 field mapping, player tracking, ball tracking, player shot analysis, and
 several other aspects involved in how the ball is delivered, its angle, spin,
 velocity, and trajectory. All these factors together have increased the
 complexity of data cleaning and preprocessing.

- **数据动态建模**

 In cricket, just like any other sport,
 there can be a large number of variables related to tracking various numbers
 of players on the field, their attributes, the ball, and several possibilities
 of potential actions. The complexity of data analytics and modeling is
 directly proportional to the kind of predictive questions that are put forth
 during analysis and are highly dependent on data representation and the
 model. Things get even more challenging in terms of computation, data
 comparisons when dynamic cricket play predictions are sought such as what
 would have happened if the batsman had hit the ball at a different angle or
 velocity.

- **预测分析的复杂性**

 Much of the decision making in cricket is based on questions such as "how
 often does a batsman play a certain kind of shot if the ball delivery is of a
 particular type", or "how does a bowler change his line and length if the
 batsman responds to his delivery in a certain way".
 This kind of predictive analytics query requires highly granular dataset
 availability and the capability to synthesize data and create generative
 models that are highly accurate.

## NumPy在板球数据分析中的角色

体育分析是一个蓬勃发展的领域。 体育分析是一个蓬勃发展的领域。 除了使用最新的机器学习和AI技术之外，许多研究人员和公司[使用Numpy](https://adtmag.com/blogs/dev-watch/2017/07/sports-analytics.aspx)和其它Python数据处理包，例如Scikit-learn, SciPy, Matplotlib和Jupyter。  Numpy已用于各种与板球相关的体育分析中，例如：  Numpy已用于各种与板球相关的体育分析中，例如：

- **统计分析:** NumPy的数值计算功能有助于在各种球员和比赛策略下估算观察数据或比赛事件的统计意义，并通过与生成模型或静态模型进行比较来预测比赛结果。 [因果分析](https://amplitude.com/blog/2017/01/19/causation-correlation) 和 [大数据分析](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4996805/) 就常用于战术分析。
 [Causal analysis](https://amplitude.com/blog/2017/01/19/causation-correlation)
 and [big data approaches](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4996805/)
 are used for tactical analysis.

- **Data Visualization:** Data graphing and visualization provide useful insights into relationship between various datasets.

## 总结

在专业赛事中，特别是需要战略决策的比赛，运动数据分析常常能起到力挽狂澜的效果，哪怕是现在，主要还是依赖“勇气和直觉”或对过去传统的经验来完成分析。 NumPy为大量的 Python 软件包奠定了坚实的基础，这些软件包提供了与数据分析， 机器学习和AI算法相关的更高层级的函数。
这些软件包被广泛应用以获取实时赛况的分析，从而有助于在现场做出最有利于自己的决策，实现在板球比赛过程中的商业利益最大化。 找出影响板球比赛结果的隐藏参数、模式和属性，有助于投资方获得隐藏在数字和统计数据背后的比赛洞察力。

{{< figure >}}
{{< /figure >}}
