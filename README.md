# FAST-LIVO2三位一体解析：从论文到代码再到实战
:mortar_board: 从小白的视角去分析多源融合SLAM的SOTA框架: FAST-LIVO2

## :tada: FAST-LIVO2 是一项令人惊艳的 SLAM 工作，其精妙的设计使其能够鲁棒、高效地应对诸多挑战性场景。然而，这也使得初学者在理解和复现该框架时可能面临不小的困难。

## :umbrella: 笔者在学习过程中，深感其理论之深邃、实现之精妙，同时也踩过不少“坑”。为帮助更多同好少走弯路，斗胆将个人学习笔记整理成文，涵盖论文解析、代码解读以及实战调优经验。才疏学浅，文中难免存在疏漏或理解不当之处，恳请各位读者批评指正。若此仓库能对您的学习略有助益，笔者将倍感欣慰。

### :rocket: 解析内容简介
FAST-LIVO2作为SLAM领域的前沿工作，其论文与代码中蕴含了许多精妙的设计。但受限于论文篇幅和代码的工程复杂性，部分关键细节可能对初学者不够友好。本解析尝试从以下三个层面展开，希望能为读者提供一些参考：

### :black_nib: 1. 论文解析
对原论文中因篇幅限制未展开的基础理论（如数学推导、设计动机等）进行补充说明。 通过图解和示例，帮助理解核心创新点（例如紧耦合设计、特征提取策略等）。附注相关领域的背景知识，降低跨领域学习门槛。

### :computer: 2. 代码解析
基于官方默认配置，对代码框架进行逐行注释。在关键算法实现处标注对应的论文公式，建立理论与代码的映射关系。总结代码中的工程技巧（如并行化设计、内存管理等），供实际开发借鉴。
由于笔者发现用word文档的形式去解析代码属实费事（函数一个套一个），故以思维导图的形式对整个框架进行展开（也可选文档模式），如下图所示。pdf版本已上传，或者可以选择在线思维导图浏览（打开链接后请选择右上角的思维导图或者文档模式） https://www.mubu.com/doc/w8Dd21eztg
<div align=center>
<img src="https://github.com/cchester25/FAST_LIVO2_Noted/blob/main/img/示意图.png" width="850" height="400">
</div>

### :hammer: 3. 实战解析
硬件选型与组装：针对不同预算和场景（如无人机、机器人），推荐传感器配置方案。 调试与标定：分享传感器标定、时间同步等常见问题的解决方法。 部署优化：从实际数据采集到算法的全流程经验。
这里先放上本人进行硬件搭建时的笔记，目前还比较粗糙，但关键信息也都有了，https://www.mubu.com/doc/D81I0U3qM

### :rose: 特别说明
本解析是笔者在复现过程中的个人学习笔记，并非官方指南。若存在理解偏差，欢迎通过Issue或PR指正！ 或者联系本人邮箱：fengpan97618@163.com


# :clap: :clap: :clap: 致谢：特别感谢 FAST-LIVO2 作者团队的杰出工作，开源精神推动着整个领域的进步！

# 设备及效果展示

### 手持设备

<div align=center>
<img src="https://github.com/cchester25/FAST_LIVO2_Noted/blob/main/img/handle1.jpg" width="350" height="450"><img src="https://github.com/cchester25/FAST_LIVO2_Noted/blob/main/img/handle2.jpg" width="350" height="450">
</div>

### 无人机挂载设备

<div align=center>
<img src="https://github.com/cchester25/FAST_LIVO2_Noted/blob/main/img/M3001.jpg" width="350" height="450"/><img src="https://github.com/cchester25/FAST_LIVO2_Noted/blob/main/img/M3002.jpg" width="350" height="450"/>
</div>

### 挂载效果

<div align=center>
<img src="https://github.com/cchester25/FAST_LIVO2_Noted/blob/main/img/Fly.jpg" width="350" height="450"/>
</div>

### 操场建图效果

<div align=center>
<img src="https://github.com/cchester25/FAST_LIVO2_Noted/blob/main/gif1/gfcc0 00_00_00-00_00_30.gif" width="450" height="350">
</div>

### 工厂建图效果

<div align=center>
<img src="https://github.com/cchester25/FAST_LIVO2_Noted/blob/main/gif2/jichi0_1 00_00_00-00_00_30.gif" width="400" height="350"><img src="https://github.com/cchester25/FAST_LIVO2_Noted/blob/main/gif2/jichi1_3 00_00_00-00_00_30.gif" width="400" height="350">
</div>

### 农田建图效果

<div align=center>
<img src="https://github.com/cchester25/FAST_LIVO2_Noted/blob/main/gif3/farmland1_0 00_00_00-00_00_30.gif" width="400" height="350"><img src="https://github.com/cchester25/FAST_LIVO2_Noted/blob/main/gif3/farmland1_1 00_00_00-00_00_30.gif" width="400" height="350">
</div>

<div align=center>
<img src="https://github.com/cchester25/FAST_LIVO2_Noted/blob/main/gif4/farmlan1_2 00_00_00-00_00_30.gif" width="400" height="350"><img src="https://github.com/cchester25/FAST_LIVO2_Noted/blob/main/gif4/farmland1_3 00_00_00-00_00_30.gif" width="400" height="350">
</div>


