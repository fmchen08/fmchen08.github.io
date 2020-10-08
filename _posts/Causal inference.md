# 因果推断

- causal inference without models (nonparametric)
- causal inference with models (parametric)
- causal inference from complex longitudinal data

Identification and estimation of **causal effects** on populations, that is, numerical quantities that measure changes in the distribution of an outcome under different interventions. 

## 因果效应的定义

### 1. 数学表示

#### 1.1 个体因果效应

Zeus 1月1日进行了心脏移植手术，5天后他去世了。如果1号那天他没有做这个手术，5天后可能还活着。那么心脏移植手术对Zeus的5日生存具有因果效应。Hera也在1月1日进行了心脏移植手术，5天后她仍然活着。如果我们知道如果那天她没有做这个手术，5天后也能生存。那么心脏移植手术对Hera的5日生存就不具有因果效应。

**How human reason about causal effects**: we compare the outcome when an action A is taken versus the outcome when the action A is withheld.  If the outcomes differ, we say that the action A has a causal effect, causative or preventive, on the outcome. 

***Action A***: an intervention, an exposure, a treatment, etc.

对于审美问题来说，Action 可以指对某个特征的调整（如比例、形状、肤色、光照等）或者依据某种算法的整体美化操作，Outcome 指美学评分。Action和Outcome本质上都是连续的量，为了简化问题，也可以将他们量化成等级。

**数学表示**：
$$
\text{Zeus: } Y^{a=1}=1, Y^{a=0}=0 \\
\text{Hera: } Y^{a=1}=0, Y^{a=0}=0
$$

**定义**：The treatment $A$ has a ***causal effect on an individual***'s outcome $Y$ if $Y^{a=1}\ne Y^{a=0}$ for the individual. 

$Y^{a=1}, Y^{a=0}$ 称为潜在结果或反事实结果。$Y$ 为观测结果。Zeus 做了心脏移植手术，因此 $A=1$ 是真实存在的情况。观测结果与反事实结果一致，即 $Y = Y^{a=1}$. 

**一致性**：if $A_{i}=a, \text{then}~ Y_{i}^{a}=Y_{i}^{A}=Y_{i}$, 即 $Y = Y^{A}$

个体因果效应是反事实结果之差，但是只有一个反事实结果能够观测到，其他的反事实结果都无法观测，因此个体因果效应无法表示为观测数据的函数。

#### 1.2 平均因果效应

个体因果效应一般来说难以计算，一个群体的平均因果效应可以计算吗？

![table1_1](https://i.loli.net/2020/10/08/iJA2RNdBX7HMf3S.png)


$$
Pr[Y^{a=1}=1]=10/20=0.5\\
Pr[Y^{a=0}=1]=10/20=0.5
$$
**平均因果效应**：An average causal effect of treatment $A$ on outcome $Y$ is present if $Pr[Y^{a=1}=1]\ne Pr[Y^{a=0}=1]$ in the population of interest. 

上面的例子里，A 对 Y 没有因果效应。

Rewrite the definition of a non-null average cause effect in the population as $E[Y^{a=1}]\ne E[Y^{a=0}]$ 

- Absence of average causal effect does not imply absence of individual effects. 
- When there is no causal effect for any individual in the population, i.e., $Y^{a=1}=Y^{a=0}$ for all individuals, we say that the **sharp causal null hypothesis** is true. 

average causal effect --> causal effect

no average effect --> causal null hypothesis



## 思考

- 如何提出因果问题？



