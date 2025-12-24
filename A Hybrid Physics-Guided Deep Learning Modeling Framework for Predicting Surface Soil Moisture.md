# A Hybrid Physics-Guided Deep Learning Modeling Framework for Predicting Surface Soil Moisture
土壤湿度研究重要性：陆气耦合、水热预测、碳循环
> Accurate prediction of surface soil moisture (SSM) is vital for understanding the complex interactions between terrestrial and atmospheric processes with significant implications for weather forecasting, agriculture, and water management. 
>
> SSM acts as a pivotal link between the terrestrial water cycle and atmospheric conditions influencing weather patterns, climate regulation, and water availability for ecosystems and agriculture (Koster et al., 2004; Rodriguez-Iturbe, 2000; Seneviratne et al., 2010)
>
> Accurate measurements and predictions of SSM can significantly improve weather forecasting accuracy, agricultural productivity, and water resource management (Abowarda et al., 2021; Chatterjee et al., 2022).
>
> SSM affects evapotranspiration, soil respiration, and plant transpiration processes as well as the exchange of water and heat energy between the land surface and the atmosphere (Porporato et al., 2002; Zhou et al., 2021)
>
> SSM is also important to understanding the carbon cycle and its feedback on the Earth climate system (Green et al., 2019; Humphrey et al., 2021).

ML的作用：海量数据处理，非线性关系捕捉，解释复杂动态特征
> The core strength of ML/DL lies in processing large amounts of data and deciphering the complex nonlinear patterns and interactions, thereby revealing insights into complex SSM dynamics influenced by multiple factors (Reichstein et al., 2019)

ML的一个不足：可能不能实现对未来的预测，因为超出了训练数据的分布
> Furthermore, the success of ML/DL models in capturing complex nonlinear relationships does not necessarily imply the ability to predict future conditions under climate change where the underlying dynamics may be beyond the range of historical changes captured in the training data (Reichstein et al., 2019).

传统物理模型的不足：参数不确定性大，参数调优困难
> the reliability of PB models is often compromised by their parameter-related uncertainties, oversimplification of complex processes, and the need for extensive calibration against empirical data (Arhonditsis & Brett, 2004; Clark et al., 2016; Montanari, 2007). 


数据：
ISMN地面观测土壤湿度、ERA5做驱动、

物理约束组主要是一个水量平衡公式
![alt text](image.png)
AI模型用的是LSTM
