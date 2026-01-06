# Temperature Is Surpassing Precipitation as the Dominant Driver of Flash Drought Acceleration Under Climate Warming

文章主要是利用RF通过降水和温度等变量来预测flashdrought，然后根据SHAP来评估降水和温度对flash drought事件的可解释性，进而分析这一年的flash drought是降水亏损主导还是高温主导，进一步得到主导因素转变的趋势。
我觉得这个方法可以用到之前CSM里边，植被的生长状况收到水分和能量的约束，全球变化背景下，应该有一个由能量限制到水分限制的趋势变化，那么我们也可以用这个方法得到各个区域的趋势变化


flash drought引起的原因：
> Flash droughts (FDs), characterized by rapid soil moisture depletion, are typically driven by multiple factors including precipitation deficits, high temperature, increased radiation, strong winds, and enhanced land-atmosphere coupling.

使用的数据：
> ERA5:
> precipitation
> T2m
> Tdew
> net shortwave radiation
> 10-m U and V wind components
> top-1 m soil moisture (from layers 0–7 cm, 7–28 cm, and 28–100 cm) 
> for the period 1960–2022
>VPD(estimated by daily T2m and Tdew)
Daily simulations for precipitation, T2m, relative humidity (RH), surface downwelling and upwelling shortwave radiation, near-surface wind speed and top-1 m soil moisture were obtained from global climate models (GCMs)

flash drought的定义：
> To identify FD events at each pixel, pentad-mean root-zone soil moisture data was first converted to percentiles according to the climatology for each calendar pentad during growing season (April-September for North Hemisphere, October-March for South Hemisphere).