# 全球径流区域信息：计算与复现代码

[下载完整代码包](streamflow-regional-information.zip)，解压后使用。代码按功能组织，包含 236 个文件；文件校验值见 [SHA256SUMS.txt](SHA256SUMS.txt)。

## 目录

| 目录 | 内容 |
|---|---|
| `workflows/archive_diagnosis` | 缺失结构、参考支撑与规则敏感性 |
| `workflows/benchmarks` | 信息输入、算法对照、参考站筛选 |
| `workflows/regional_dependence` | 全球参考池、区域撤源、季节信息 |
| `workflows/rainfall` | 降雨准备、联合输入与观测背景 |
| `workflows/monitoring` | 新增观测、共同历史和位置试验 |
| `workflows/validation` | 站点身份、真实缺口与外部资料核验 |
| `workflows/water_resources` | 低流时序、累计亏缺与区间水量 |
| `workflows/shared` | 共用数据、模型和评价工具 |
| `src/streamflow_info` | 可独立调用的数值核心 |
| `examples`、`tests`、`docs` | 案例、测试和英文复现说明 |

## 使用

进入解压后的 `streamflow-regional-information` 文件夹：

```sh
python -m pip install -e .
python -m unittest discover -s tests -v
python examples/run_synthetic_case.py --output-dir outputs/synthetic_case
```

合成案例不需要观测数据。Paraná / Posadas 注册案例通过 JSON 明确指定输入文件，详见包内 `examples/README.md`。完整计算需要包内复现说明所列的数据和登记文件；观测数据未随代码分发。

## 核查

37项测试通过。真实案例15个输入数组、25个输出数组完全一致，其中包括2,880个预测值；另外12种合成工况共1,860项核心输出精确一致。代码内部调用、路径和文档链接已检查。

[English README](README.md)
