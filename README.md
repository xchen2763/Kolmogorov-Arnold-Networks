# 6699-temporary

下载ipynb到根目录 用kan原repo自带环境跑 https://github.com/KindXiaoming/pykan

报告地址： https://www.overleaf.com/project/6802f4d90c6da62df6cba6e7

PPT地址： https://docs.google.com/presentation/d/1KRAc_hzuNN3Qyb8FiqA5tyHeOLLvO2VHIWnsMwUsRtQ/edit#slide=id.g1b9529cbea5_0_0

DDL: **四月29号汇报 尽量下周末把大致搞出来**

-------------------------------------------------------------------------------------------------------------
# KAN vs. MLP: Report Structure Overview  
*Exploring Kolmogorov–Arnold Networks for Interpretable Scientific Regression*

---

## 1. Introduction / 引言

- Motivation for symbolic function approximation
- Limitations of MLP in interpretability and structured inductive bias
- Why we need KAN
- Overview of this paper: symbolic regression comparison using Feynman equations

## 2. Related Work / 相关工作

- Interpretability in neural networks: symbolic regression, Neural ODEs, rational approximators
- Prior works: DeepSymbolicRegression, SciNet, RationalNet
- How KAN differs and extends previous approaches

## 3. Kolmogorov–Arnold Networks / KAN 原理

### 3.1 Theoretical Foundation / 理论基础

- Kolmogorov–Arnold Theorem: any multivariate function can be decomposed into compositions of univariate functions
- Implications for network design

### 3.2 Network Design / 网络结构

- Composition of 1D spline activations
- Grid structure and interpretable symbolic paths
- Comparison with MLP design

## 4. Experimental Setup / 实验设置

- Dataset: Feynman symbolic equations (1–30)
- Metric: RMSE on train/test sets
- Uniform architecture (same hidden size, depth, training steps)
- Training settings: 15 steps, LBFGS, same width

## 5. Results / 实验结果

### 5.1 Interpretability of KAN / KAN 的可解释性

- Network diagrams generated via `expr2kan`
- Matching network paths to mathematical terms
- Example with Problem 36: structure reveals symbolic components

### 5.2 Comparison with MLP / 与 MLP 对比

- Detailed case analysis: training/test curve + structure visualization
- Table: RMSE of KAN vs. MLP on 10 problems
- Same-size KAN achieves better or equal RMSE with more interpretable structure

### 5.3 Extended Experiments / 扩展实验（简要）

- Classification task (e.g. MNIST)
- Continual learning with modular symbolic structure
- Optional: reward function modeling in RL

## 6. Analysis & Discussion / 分析与讨论

- Why KAN performs better: inductive bias from spline and symbolic composition
- When to use KAN: small data, symbolic reasoning, interpretability-required tasks
- When to prefer MLP: large-scale classification, general-purpose deployment

## 7. Conclusion / 结论

- KAN brings interpretability and expressive efficiency into neural networks
- Promising direction for symbolic regression and scientific learning
- Future work: stability, automatic symbolic architecture search, hybrid models

---

*This structure is suitable for a publishable paper or technical report.
