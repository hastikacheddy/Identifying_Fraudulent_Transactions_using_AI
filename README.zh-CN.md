# 基于人工智能的欺诈交易识别

[English](README.md) | 简体中文

信用卡欺诈每年给企业和消费者造成巨大的经济损失。机器学习为欺诈检测提供了有效途径，但真实数据往往**类别极度不平衡**：正常交易的数量远远超过欺诈交易，这给建模带来了很大挑战。

## 项目概述

本仓库评估了四种机器学习算法在信用卡欺诈检测中的效果：

- K 近邻（KNN）
- 决策树（Decision Tree）
- 随机森林（Random Forest）
- XGBoost

实验同时使用**真实数据集**和**合成数据集**。两者都存在严重的类别不平衡，其中合成数据集包含 91.3% 的正常交易和 8.7% 的欺诈交易。

## 实验方法

为保证评估稳健，每种算法分别采用以下四种训练方式：

1. 重复 5 折交叉验证
2. 分层 5 折交叉验证
3. 随机过采样 + 分层 5 折交叉验证
4. SMOTE 过采样 + 分层 5 折交叉验证

评估指标包括：准确率（Accuracy）、精确率（Precision）、召回率（Recall）、F1 值和 ROC 值。

## 实验结果

- **合成数据集**：XGBoost 和决策树表现最佳，准确率、精确率、召回率和 F1 值均达到 1.00，在识别欺诈交易的同时将误报降到最低。
- **真实数据集**：表现有所差异，随机森林和 XGBoost 综合表现最好，各项指标均较高，ROC 值接近 1，显示出很强的区分能力。

## 结论

XGBoost 和决策树在信用卡欺诈检测方面展现出良好潜力。但要确认其泛化能力和稳健性，仍需在更多样化的真实数据集上进一步验证，然后才能考虑集成到实际的反欺诈系统中。

## Web 界面演示

项目附带一个简单的 Web 界面，用于演示模型的实际判断效果：

- 输入**正常交易**数据时，系统正确判定为“非欺诈”：

![FDS2](https://github.com/hastikacheddy/Identifying_Fraudulent_Transactions_using_AI/assets/59787014/284d2b8e-7dc2-4d69-b878-88a6c13f5c1f)

- 输入**欺诈交易**数据时，系统正确判定为“欺诈”：

![FDS1](https://github.com/hastikacheddy/Identifying_Fraudulent_Transactions_using_AI/assets/59787014/79c17ba4-b015-4c79-938f-11d3bb0dac72)

## 项目结构

| 路径 | 说明 |
| --- | --- |
| `Real_dataset_of_Identifying_Fraudulent_Transactions_using_AI.ipynb` | 真实数据集上的实验 |
| `Synthetic_dataset_Identifying_Fraudulent_Transactions_using_AI.ipynb` | 合成数据集上的实验 |
| `web_ui.ipynb` | Web 演示界面 |
| `model/` | 训练好的模型文件（`.pkl`） |
| `templates/`、`static/` | Web 页面模板与静态资源 |
| `Dataset/` | 数据集说明 |
