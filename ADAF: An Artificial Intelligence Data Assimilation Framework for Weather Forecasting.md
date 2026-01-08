# ADAF: An Artificial Intelligence Data Assimilation Framework for Weather Forecasting
**Author**
Yanfei Xiang, Haiyu Dong, Xiaomeng Huang
Department of Earth System Science, Ministry of Education Key Laboratory for Earth System Modeling, Institute for Global Change Studies, Tsinghua University, Beijing, China

**abstract：**
数据同化的意义：对未来状态的估计需要一个准确的背景场（也就是同化后的输出场），
> The forecasting skill of numerical weather prediction (NWP) models critically depends on the accurate initial conditions, also known as analysis, provided by data assimilation (DA).
>
> The precision of weather forecasts is highly dependent on the quality of the initial conditions provided by data assimilation (DA)


传统数据同化面临的问题：精度与计算资源的取舍,因此可以考虑使用AI进行替代
> Traditional DA methods often face a trade-off between computational cost and accuracy due to complex linear algebra computations and the high dimensionality of the model, especially in non-linear systems.
---
**Intro**
1.1 对未来状态的准确估计需要一个准确的背景场
数据同化可以提供一个准确的背景场
> The precision of weather forecasts is highly dependent on the quality of the initial conditions provided by data assimilation (DA) (Bauer et al., 2015; Griffith & Nichols, 2000; Hunt et al., 2005). DA methods aim to improve forecast accuracy by integrating observations into numerical weather prediction (NWP) models to generate reliable initial conditions (Asch et al., 2016).

1.2 介绍了三种传统数据同化的方法（4DVar， EnKF， Hybrid）
2.1 传统数据同化面临的问题（计算效率，非线性系统中同化困难，前提假设）
> Although DA methodology has evolved and improved, there remains a **trade-off between computational cost and accuracy**, largely due to **complex linear algebra and the high dimensions of models, particularly in non-linear systems** (Boudier et al., 2023; Khaki et al., 2018). The increased volume, complexity, and diversity of observations, coupled with the need for precise real-time processing, have notably raised resource demands in NWP (Eyre et al., 2022). This is particularly challenging when there is a significant difference between the model and observation states in spatial resolution, leading to representation errors and correlations in observation errors (Janjic et al., 2018; Lahoz et al., 2010). In practice, DA methods often depend on **simplifying assumptions** such as linearity and Gaussianity, which can reduce their accuracy (Kurosawa & Poterjoy, 2021; McLaughlin, 2002). Balancing these factors requires thoughtful algorithm design, model simplification, and leveraging high-performance computing resource.

3.1 ML的优势（improve the accuracy and efficiency ）