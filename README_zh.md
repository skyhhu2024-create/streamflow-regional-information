# 全球径流区域观测信息：代码与复现案例

本仓库保存论文 **Global data availability does not make nearby streamflow gauges dispensable** 的 **v0.2.0** 代码发布包，对应2026年11月8日核对后的正文与SI。

## 下载和使用

下载[完整代码包](streamflow-regional-information_v0.2.0.zip)，解压后进入 `streamflow-regional-information` 文件夹，再按其中英文 `README.md` 或中文 `README_zh.md` 操作。完整目录保存在ZIP中，不要直接在本仓库首页目录运行安装命令。

包内共有 **182个文件**，包括 **142个归档计算源文件**、便携计算核心、合成案例、真实河流案例提取工具、测试、中英文说明和正文—SI—计算入口对应表。包含信息筛选、区域参考撤除、降雨补充、观测位置以及水资源后果等计算。

33项测试已通过。Paraná / Posadas真实案例的16个数组与冻结结果完全一致，包括2,880个预测值。此次代码整理没有重跑全球经验试验。

原始GSIM、GRDC、ERA5观测不随代码分发。合成案例可直接运行；真实案例及完整全球实验需要按 `docs/REPRODUCTION.md` 准备原始数据和冻结输入。校验值见[SHA256SUMS.txt](SHA256SUMS.txt)。

详细英文导航见[README](README.md)。当前尚未指定开源许可证。
