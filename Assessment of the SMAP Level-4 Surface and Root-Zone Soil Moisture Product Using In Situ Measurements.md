# Assessment of the SMAP Level-4 Surface and Root-Zone Soil Moisture Product Using In Situ Measurements

SMAP观测了L波段的信息，该波段的强弱与土壤湿度以及温度有较强的关联
> These observations are highly sensitive to surface soil moisture and temperature, which impact the land surface water and energy balance through

传统物理模型的核心优势在于**严格遵循守恒定理**
> The land model’s key strength is its reliance on conservation principles for water (converting precipitation inputs into evaporation, runoff, and storage change) and energy (converting incident radiation into outgoing radiation, latent heat flux, sensible heat flux, storage change, and other miscellaneous terms).

SMAP L4系统的3天延迟主要取决于观测降水的限制
> The product is published within about 3 days from the time of observation, with the latency primarily dictated by the availability of the gauge-based precipitation product used to drive the land model

如何验证SMAP L4，使用的数据包括两个，**core validation site**和**sparse network**
> The L4_SM product is primarily validated through comparison with independent in situ measurements (section 4). Suitable measurements fall into two main categories: 1) for a limited set of climate and land cover conditions, “core validation site” measurements provide **accurate estimates of soil moisture at the 9- or 36-km scales of the model and satellite estimates** (section 3b), and 2) for a much **wider range of conditions**, “sparse network” measurements provide soil moisture estimates at a single, point-scale location within a 9-km model grid cell

SMAP L4的技术指标要求：0.04
> The accuracy requirement for the L4_SM surface and root-zone soil moisture estimates is that theiraverage unbiased RMSE (ubRMSE) versus in situ measurements must be less than 0.04 m3 m−3
> The ubRMSE is the RMSE computed after removing the long-term mean bias from the data, also referred to as the standard deviation of the error

**我目前算的误差较大的问题，是不是因为我的bias计算的只是一年的？？**

如何描述结果的精度，可以学习：
> The L4_SM and NRv4 estimates **clearly capture the overall variability**, as well as the timing of the major rainstorms. However, neither the NRv4 nor the L4_SM estimates fully capture the wet conditions starting in late October 2015 and lasting through the winter of 2015/16. Nevertheless, the time series correlation coefficients are very high, with R values of 0.81 for L4_SM surface soil moisture and 0.88 for L4_SM root-zone soil moisture, which is an improvement over the already high values of 0.73 and 0.87 for NRv4 surface and root-zone soil moisture, respectively
> ![alt text](/fig/LW.png)

模型精度的评估可以进一步考虑外部条件的影响，例如**地形复杂度、植被覆盖及气候差异**
气候变率与ubRMSE： 在干旱气候下，土壤湿度变率天然较低，因此ubRMSE（误差标准差）通常较小。而在气候湿润或变率大的地区（如澳大利亚部分站点），预测误差往往随之增大


