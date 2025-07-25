
# 全球疫情数据可视化与趋势分析

本项目基于 Python 3.9.11，使用 `pandas`、`numpy`、`matplotlib`、`seaborn` 等主流数据分析和可视化库，对 2021 年至 2023 年（部分）全球新冠疫情数据进行多维度可视化和趋势分析，挖掘各国疫情发展特征与对比。

##  项目目标

- 清洗并整合全球疫情数据
- 计算新增确诊、增长率、死亡率、滑动平均等关键指标
- 处理异常值并分析其对趋势的影响
- 通过多种图表（折线图、热力图等）可视化疫情趋势和严重程度
- 探索不同年份中各国疫情态势的变化

## 数据来源
- https://coronavirus.jhu.edu/
- https://github.com/CSSEGISandData/COVID-19

##  使用的数据维度

- `Confirmed`: 累计确诊数
- `Deaths`: 累计死亡数
- `new_confirmed`: 每日新增确诊数（已处理异常值）
- `growth_rate`: 确诊增长率
- `new_confirmed_7d_ave`: 7 日滑动平均新增数
- `new_confirmed_14d_ave`: 14 日滑动平均新增数
- `death_rate`: 病死率
- `Confirmed_cleaned`: 修正后的累计确诊数（异常值剔除）

##  可视化图表类型

- 折线图：展示各国每日新增、增长率及滑动平均趋势
- 热力图：多指标对比各国疫情严重性（可视化国家太多时使用截断优化显示）
- 滑动窗口分析：支持 `min_periods` 自定义，剔除首日无意义数据

##  使用的主要库

- `pandas`：数据处理与时间序列分析
- `numpy`：数值计算与异常值处理
- `matplotlib`：图形绘制
- `seaborn`：统计图表增强
- `warnings`：忽略无关提示

##  文件说明

| 文件名 | 说明 |
|--------|------|
| `全球疫情数据可视化与趋势分析.ipynb` | 主分析代码，包含数据读取、处理、可视化全流程 |
| `data` | 原数据 |
| `img` | 统计图 |
| `requirements.txt` | 需求文档 |
| `README.md` | 项目说明文档 |

##  使用方式

1. 安装依赖：

   ```bash
   pip install -r requirements.txt
   ```

2. 使用 Jupyter Lab 或 Jupyter Notebook 打开 `.ipynb` 文件运行即可。

##  项目亮点

- 综合使用 `pandas` + `numpy` + `matplotlib` 三大数据分析库
- 完善的数据清洗、异常剔除与滑动统计处理
- 多维度可视化，提升分析洞察力
- 支持多年份数据分段分析，结构清晰
