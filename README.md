House Prices 房价预测项目

项目简介

本项目基于 Kaggle 经典机器学习竞赛 House Prices - Advanced Regression Techniques 开展，旨在利用房屋属性数据预测住宅销售价格。

项目以 Ames Housing 数据集为基础，包含 80 余个房屋属性特征，涵盖房屋质量、建筑面积、地下室、车库、地理位置等多个维度信息。围绕房价预测任务，独立完成数据探索分析（EDA）、数据清洗、特征工程、模型训练、超参数优化以及模型集成等完整机器学习流程，并通过持续实验迭代不断优化模型性能。

项目累计完成 30 余个实验版本，对特征工程、模型结构及参数配置进行持续优化，将 RMSLE 从 0.143 优化至 0.11935，最终在 Kaggle 全球 5093 支参赛队伍中取得第 289 名（Top 5.6%）成绩。

⸻

项目目标

* 掌握完整的数据科学建模流程
* 提升机器学习实践能力
* 学习特征工程与模型优化方法
* 探索集成学习在结构化数据场景中的应用
* 形成基于数据驱动的实验设计与迭代优化思维

⸻

数据集介绍

数据来源

Kaggle - House Prices: Advanced Regression Techniques

数据规模

* 训练集：1460 条样本
* 测试集：1459 条样本
* 特征数量：80+ 个特征

目标变量

* SalePrice（房屋成交价格）

评价指标

* RMSLE（Root Mean Squared Logarithmic Error）

⸻

项目流程

1. 探索性数据分析（EDA）

针对数据集开展探索性分析，重点分析：

* 缺失值分布情况
* 异常值情况
* 特征相关性
* 目标变量分布特征

主要发现：

* 房价呈明显右偏分布
* 房屋整体质量、居住面积、车库容量等特征与房价具有较强相关性
* 部分特征存在较高比例缺失值，需要进行针对性处理

⸻

2. 数据预处理

完成数据清洗与预处理工作：

* 缺失值填补
* 异常值处理
* 特征标准化
* 类别变量编码
* 目标变量对数变换

使用方法：

* Label Encoding
* Target Encoding
* Log Transformation

⸻

3. 特征工程

特征工程是本项目的重要优化环节。

主要工作包括：

* 构建交互特征
* 构建聚合统计特征
* PCA降维
* KMeans聚类特征构造
* SHAP特征重要性分析
* 特征筛选与优化

通过多轮实验验证不同特征方案对模型性能的影响。

⸻

4. 模型训练

采用以下主流梯度提升树模型进行训练：

* XGBoost
* LightGBM
* CatBoost

同时构建：

* 5折交叉验证（Cross Validation）

用于评估模型泛化能力并降低过拟合风险。

⸻

5. 超参数优化

引入 Optuna 自动化超参数优化框架。

重点优化参数：

* learning_rate
* max_depth
* n_estimators
* subsample
* colsample_bytree

通过多轮搜索获得最优参数组合。

⸻

6. 模型集成

为了进一步提升模型性能与稳定性，构建：

* XGBoost
* LightGBM
* CatBoost

三模型集成方案。

采用 OOF（Out Of Fold）预测结果确定模型权重，实现模型融合。

⸻

项目成果

指标	结果
Baseline Score	0.143
Final Score	0.11935
成绩提升	约16.5%
全球排名	289 / 5093
排名比例	Top 5.6%

⸻

项目亮点

持续实验迭代

累计完成 30+ 个实验版本，对特征工程、模型结构及参数配置进行持续优化。

自动化调参

引入 Optuna 自动搜索超参数，相比人工调参显著提升效率。

集成学习

构建多模型融合方案，进一步提升预测精度与稳定性。

特征工程优化

结合统计分析与实验结果构建高价值特征，提高模型表达能力。

⸻

技术栈

编程语言

* Python

数据处理

* Pandas
* NumPy

机器学习

* Scikit-learn
* XGBoost
* LightGBM
* CatBoost

模型优化

* Optuna
* SHAP

数据可视化

* Matplotlib

⸻

项目收获

通过本项目系统掌握了从数据清洗、特征工程、模型训练到模型优化与模型集成的完整数据科学工作流，提升了机器学习实践能力、实验设计能力以及基于数据持续迭代优化的分析思维。

项目过程中逐步形成“提出假设 → 数据验证 → 实验优化 → 结果评估”的分析习惯，为后续用户行为分析、增长分析及商业分析项目奠定了实践基础。

⸻

相关链接

Kaggle Competition

https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques


Leaderboard Screenshot

建议上传排行榜截图作为项目成果证明
