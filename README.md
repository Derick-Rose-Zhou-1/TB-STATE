# TB-STATE Model Checkpoint

We have developed TB-STATE (Tuberculosis Single-cell Transcriptomic Analysis of Transcriptional Evolution), an AI-driven VAE framework that integrates single-cell and bulk blood transcriptomic data to identify TB-related biomarker programmes, support disease-state discrimination and stratify future progression risk through interpretable PBMC immune-state features. TB-STATE currently supports three applications: HC-TB infection-TB disease-state discrimination, future-progression risk stratification using VAE-derived cell-state features, and exploratory immune-state analysis of advanced TB branches including DTB, TPE, TBM and other active-TB manifestations.
![Uploading image.png…]()


本仓库提供训练完成的 TB-STATE model checkpoint，方便审稿人和读者确认模型文件已公开保存，并可在获得相应数据与代码后进行复现或后续分析。

## 这个仓库包含什么

- `model.pth`  
  TB-STATE 训练后的 PyTorch 模型 checkpoint。

- `README.md`  
  模型文件说明、使用范围和注意事项。

## 这个模型用于什么

TB-STATE 是一个用于结核病相关免疫状态建模的单细胞转录组模型框架。该模型 checkpoint 对应 manuscript 中使用的 TB-STATE 分析流程，可用于支持模型复现、审稿核查和后续研究参考。

## 重要说明

本仓库仅包含模型 checkpoint，不包含：

- 原始人源样本数据
- 单细胞表达矩阵
- 临床信息表
- 受试者级别数据
- 大体量中间分析结果

相关输入数据的获取方式请参考 manuscript 中的 Data Availability statement。

## 基本使用方式

如果你已经拥有对应的模型代码和输入数据，可以使用 PyTorch 加载该 checkpoint：

```python
import torch

checkpoint = torch.load("model.pth", map_location="cpu")
