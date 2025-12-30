# Prediction of Flash Droughts over the United States

这项研究探讨了利用NOAA第二代全球对流层系预报系统（GEFSv2）对美国突发性干旱进行中短期预测的可行性。作者将此类干旱细分为由极端高温触发的热浪型和由降水缺失引起的降水短缺型，并评估了它们在不同季节的发生频率。研究发现，该模型在1至2个五日候（pentads）的预报时效内表现出显著的预测技能，尤其是在春季的热浪型干旱预测方面。然而，由于降水预测本身存在局限性，导致降水短缺型干旱的预报准确度相对较低且存在较高的误报率。总体而言，模型能够较好地捕捉土壤湿度与蒸发之间的线性物理关系，为未来开发实时干旱预警系统奠定了基础。尽管如此，预报时效一旦超过10天，其针对具体干旱事件的预测效能就会因误差累积而明显下降。

flash drought引起了较强的关注，列举了几个flash drought的时间**我们是否有必要修改一下模型训练的时间**使用2017年比较适合CVS评估
> Flash droughts have received considerable attention since the rapidly evolving 2012 central U.S. event (Hoerling et al. 2014), and subsequent events in 2017 over the northern Great Plains, and 2019 over the southern states.

几个flash drought的时间：
2017 event that lasted from mid-May to June resulted in an estimated $2.6 billion in agricultural losses
2019 flash drought that lasted from 16 July to 12 August also demonstrated linkages between rapid drying of vegetation and subsequent wildfires

flash drought的特点:**爆发速度快且加强迅速,持续时间短**,可分类为热浪型突发性干旱和降水亏缺型突发性干旱
> Flash droughts differ from conventional drought which is characterized by the persistent lack of precipitation P, accompanied by soil moisture (SM), and/or runoff deficits, usually for 6 months or longer (Svoboda et al. 2002). Flash droughts have much shorter durations—typically a few weeks. Furthermore, while conventional droughts develop slowly, a key feature of flash droughts is their rapid onset and intensification (Pendergrass et al. 2020).