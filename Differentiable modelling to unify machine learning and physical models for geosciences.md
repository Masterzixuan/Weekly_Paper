# Differentiable modelling to unify machine learning and physical models for geosciences

主要内容：综述性文章，主要讲可微建模，保持地学可解释性的同时利用数据驱动学习的强大能力。讲解了四种可微建模的方法

地学过程的特征：

> Some geoscientific processes are well understood whereas others are only assumed or empirically represented. 

传统数值模型的优劣：

> PBMs cannot rapidly evolve with and fully exploit information from big data owing to the time needed to develop and test process representations and parameterizations
>
> This iterative process is very expensive (in both labour and time) and complex, and can be biased by the knowledge background of the modeller

ML优劣：

>  ML typically requires large volumes of data, which unfortunately are not often available in many geoscientific applications
>
>  For rare and extreme events that critically affect human activities, such as floods, droughts,
>
> and earthquakes, available data are even scarcer.
>
>  ML is not exempt from deficiencies and can struggle with data errors, incompleteness, out-of-sample or out-of-distribution predictions, and bias in the inputs or training data
>
> ML algorithms are based on correlations and not causality, regarding both attributes and temporal changes.

文章的核心：物理与AI结合的重要前提：所有模块必须是可微的（之后提出了四种将物理模型可微的方法）

> Only gradient-based optimization, which updates the network weights by explicitly tracking their contributions to the outcome, makes it computationally tractable to learn from big data and efficiently train the large numbers of parameters necessary to approximate complex unknown functions.

**方法1:将物理模型以可微的形式重新编写**

> Differentiating through numerical models. The most straightforward DM approach is to differentiate through numerical models by leveraging ML platforms; this approach is also the most similar to traditional models. Both AD and customized backward functions (adjoint) can be used to keep track of gradients at relatively elementary levels of operations

对于不需要迭代求解的模型，可以直接重新编写代码（fortune->pytorch）

对于需要迭代求解的模型，可通过**伴随法**实现对梯度的跟踪，从而避免计算图在迭代过程的计算

什么是伴随法？

> **伴随法 (Adjoint Method)** 是一种在方程层面计算梯度的技术。它通过构造一个新的“伴随方程”，在时间上反向积分来传播误差，从而高效地求得损失函数对参数的导数。它是“反向传播”的连续版本，在可微建模、科学机器学习和地球系统优化中至关重要。

**方法2:surrogated model**利用nn替代物理模型

> Connecting NNs with PBMs through surrogate models. If an NN is trained as a surrogate for a PBM (reproducing its behaviour), this surrogate model can then be connected to other NN components ina DM framework because the NN surrogate is programmatically differentiable.

**方法3:PINN**
**方法4:PIML**





