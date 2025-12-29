# Deep Learning-Based Postprocessing to Enhance Subseasonal Soil Moisture Forecasts Over Europe

**主要内容：**
S2S尺度的土壤湿度预报对于监测和减轻骤发干旱的影响至关重要，但目前的数值天气预报模型在这一尺度上存在明显的偏差且空间分辨率较低。论文通过将动力模型预报与深度学习结合的混合建模框架，修正系统性误差并将低分辨率预报提升至高分辨率，增强预报的准确性和实用性。

文章主要是使用ERA5数据，用DL来修正ECMWF S2S和ERA5之间的差异，提升S2S中对土壤湿度的预测能力
> Accurate forecasts on subseasonal (S2S) timescales are essential for the preparation and mitigation of the impacts of high‐impact events, such as flash droughts. To improve the accuracy of soil moisture forecasts—a critical factor in identifying flash droughts—we present a hybrid modeling framework that combines dynamical forecasts from the European Centre for Medium‐Range Weather Forecasts with deep learning (DL) models. This approach not only corrects biases in numerical weather prediction models but also improves spatial resolution, increasing the accuracy of S2S forecasts.


**研究背景意义：**
> Accurate forecasts on subseasonal (S2S) timescales are essential for the preparation and mitigation of the impacts of high-impact events, such as flash droughts

**评估方法**
MAE + RMSE + CRPS + CRPSS

文章中有一个章节**Seasonal Variability in the Forecasts Skill**主要计算了四个季节的ACC和Bias来体现模型在不同季节的表现能力

**结论**
给增加额外的气象变量并未显著提升模型能力
解释：
1、土壤湿度（SM20）信号本身已经“嵌入”了与其相关的气象变量的统计依赖性，模型可以直接从 SM20 中提取大部分关键特征
2、陆面持久性主导，在次季节尺度上，预报的准确性主要soil moisture memory，土壤湿度的自相关性成为了预测的主导因素，而大气输入的贡献小
> Interestingly, our analysis demonstrated that including more predictors did not yield to a better performance, with only little marginal improvement. This suggests that the models may have already captured the critical infor-mation needed for accurate soil moisture forecast from the low‐resolution input, or that the additional variables introduced redundancy or noise rather than contributing meaningful improvements. We also hypothesize that this behavior could partially be due to overfitting, given the relatively limited size of the data set, even when using data augmentation techniques. Similar observations were reported by Springenberg et al. (2025), who found that adding more inputs did not substantially enhance S2S wind speed forecasts using diffusion models. This high-lights the need for a balanced approach when selecting predictors, ensuring that added complexity is justified by the availability of sufficient training samples, especially within the context of subseasonal forecasts.