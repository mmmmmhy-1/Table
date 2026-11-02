# Table Papers

表格理解、复杂表格问答与电子表格智能体论文索引。

首批收录 **11 篇论文**，按主要研究贡献分为 4 类。每篇提供英文标题、作者、发表信息、中文简介及原始论文链接；代码和数据仅列出已确认的项目入口。

更新日期：2026-11-02。分类与中文简介为本仓库整理，不代表作者原文。未列代码链接表示本次未确认，不代表作者未开源。

## 目录

- [表格结构与表示](#表格结构与表示)（2 篇）
- [复杂表格问答方法](#复杂表格问答方法)（2 篇）
- [电子表格智能体](#电子表格智能体)（2 篇）
- [评测基准](#评测基准)（5 篇）
- [阅读路线](#阅读路线)
- [维护方式](#维护方式)

## 表格结构与表示

### 1. Orthogonal Hierarchical Decomposition for Structure-Aware Table Understanding with Large Language Models

- **作者 / 发表**：Bin Cao 等 · ICML 2026（arXiv 页面标注）。
- **关键词**：OHD、行列树、层次结构、结构保真。
- **核心内容**：把不规则表格分解为列树与行树，分别表达纵向和横向层次依赖，再通过双路径关联恢复单元格的语义关系。
- **资源**：[论文](https://arxiv.org/abs/2602.01969) · [PDF](https://arxiv.org/pdf/2602.01969)

### 2. Same Content, Different Representations: A Controlled Study for Table QA

- **作者 / 发表**：Yue Zhang、Seiji Maekawa、Nikita Bhutani · ICLR 2026；预印本 2025。
- **关键词**：表格表示、结构化与半结构化数据、RePairTQA、控制变量研究。
- **核心内容**：保持内容一致，仅改变表格表示，比较 SQL、LLM 与混合方法；通过 RePairTQA 分析规模、连接、查询复杂度和模式质量的影响。
- **资源**：[论文](https://arxiv.org/abs/2509.22983) · [PDF](https://arxiv.org/pdf/2509.22983) · [OpenReview](https://openreview.net/forum?id=QTgx2ThiAb)

## 复杂表格问答方法

### 3. ASTRA: Adaptive Semantic Tree Reasoning Architecture for Complex Table Question Answering

- **作者 / 发表**：Xiaoke Guo 等 · ACL 2026 Main。
- **关键词**：语义树、自适应结构重建、树搜索、代码验证。
- **核心内容**：AdaSTR 根据表格规模自适应构建逻辑语义树；DuTR 将树上的文本导航与符号代码执行结合，用于复杂表格推理。
- **资源**：[论文](https://arxiv.org/abs/2604.08999) · [PDF](https://arxiv.org/pdf/2604.08999) · [代码](https://github.com/zjukg/ASTRA)
- **标题备注**：此处沿用 arXiv 标题；官方代码仓库使用 “Adaptive Structured Tree” 的标题表述。

### 4. SMART: Semantic Header Flattening and Pseudo-Code-Style Reasoning for LLM-based Complex Table Question Answering

- **作者 / 发表**：Yongshuo Zhang 等 · Findings of ACL 2026。
- **关键词**：语义表头扁平化、全局理解、伪代码推理。
- **核心内容**：将多层表头转成明确的单层描述，结合表格与问题的全局理解，再以伪代码式步骤推理，并通过外部工具验证中间计算。
- **资源**：[论文](https://aclanthology.org/2026.findings-acl.1474/) · [PDF](https://aclanthology.org/2026.findings-acl.1474.pdf)

## 电子表格智能体

### 5. SheetCompass: Hierarchical Relation Graphs for Agentic Spreadsheet Reasoning

- **作者 / 发表**：Panjing He 等 · arXiv 2026（本次核实版本）。
- **关键词**：层次关系图、跨工作表关系、记忆、电子表格自动化。
- **核心内容**：显式建模工作表内与工作表间的结构关系，并用记忆保留任务相关信息，支持复杂工作簿中的智能体推理与操作。
- **资源**：[论文](https://arxiv.org/abs/2608.14452) · [PDF](https://arxiv.org/pdf/2608.14452)

### 6. Towards Robust Real-World Spreadsheet Understanding with Multi-Agent Multi-Format Reasoning

- **作者 / 发表**：Houxing Ren 等 · ACL 2026。
- **关键词**：SpreadsheetAgent、多智能体、多格式输入、渐进阅读。
- **核心内容**：先逐步读取局部区域，结合代码执行结果、图像和 LaTeX 构建结构草图与行列摘要，再执行任务推理；通过验证模块检查结构提取结果。
- **资源**：[论文](https://arxiv.org/abs/2604.12282) · [PDF](https://arxiv.org/pdf/2604.12282) · [代码](https://github.com/renhouxing/SpreadsheetAgent)

## 评测基准

### 7. RealHiTBench: A Comprehensive Realistic Hierarchical Table Benchmark for Evaluating LLM-Based Table Analysis

- **作者 / 发表**：Pengzuo Wu 等 · Findings of ACL 2025。
- **关键词**：真实层次表格、多模态评测、HTML / LaTeX / PNG、TreeThinker。
- **核心内容**：在多种输入格式下评估复杂层次表格分析能力，并提出以树组织层次表头的 TreeThinker 方法。
- **资源**：[论文](https://arxiv.org/abs/2506.13405) · [会议 PDF](https://aclanthology.org/2025.findings-acl.371.pdf) · [代码与数据](https://github.com/cspzyy/RealHiTBench)

### 8. CompTab: A Comprehensive Benchmark for Real-World TableQA with Complex Reasoning and Irregular Tables

- **作者 / 发表**：Zhen Yang 等 · ACL 2026。
- **关键词**：不规则表格、复杂推理、语义歧义、CompTabLLM。
- **核心内容**：覆盖语义歧义、多跳推理、转置表格、合并单元格、缺失值与异常值六类场景，同时提出两阶段训练框架 CompTabLLM。
- **资源**：[论文](https://aclanthology.org/2026.acl-long.1279/) · [PDF](https://aclanthology.org/2026.acl-long.1279.pdf)

### 9. SpreadsheetBench 2: Evaluating Agents on End-to-End Business Spreadsheet Workflows

- **作者 / 发表**：Jian Zhu 等 · NeurIPS 2026（官方仓库公告）。
- **关键词**：端到端工作流、跨工作表依赖、财务建模、调试、可视化。
- **核心内容**：包含 321 个专家构建的真实业务任务，关注多步协作和跨工作表推理，评估最终交付的工作簿结果。
- **资源**：[论文](https://arxiv.org/abs/2606.29955) · [PDF](https://arxiv.org/pdf/2606.29955) · [代码与数据入口](https://github.com/RUCKBReasoning/SpreadsheetBench-2) · [项目主页](https://spreadsheetbench.github.io/)

### 10. How Far Can LLM Agents Reason with Tables? Benchmarking Multi-Turn Agentic Table Question Answering in the Wild

- **作者 / 发表**：Jingwang Huang 等 · ICML 2026。
- **关键词**：TableAgent-Bench、多轮问答、多表环境、工具调用轨迹、TAEF。
- **核心内容**：基于 2,275 张工业表格构建 1,310 组多轮对话，评估动态用户意图下的表格定位、工具调用与整段交互表现。
- **资源**：[论文与相关资源](https://proceedings.mlr.press/v306/huang26cf.html) · [PDF](https://raw.githubusercontent.com/mlresearch/v306/main/assets/huang26cf/huang26cf.pdf)

### 11. CITBench: A Comprehensive Benchmark for Interactive Tabular Data Processing with LLMs

- **作者 / 发表**：Zihan Nan 等 · arXiv 2026；列入 [ICDE 2027 已接收论文名单](https://icde2027.github.io/accepted-papers.html)。
- **关键词**：交互式数据处理、多轮交互、表格清洗、匹配、增强、转换。
- **核心内容**：包含匹配、清洗、增强和转换四大类、18 种任务及 1,296 个实例，支持离线和在线评测，关注用户需求变化下的连续数据处理。
- **资源**：[论文](https://arxiv.org/abs/2608.00018) · [PDF](https://arxiv.org/pdf/2608.00018)

## 阅读路线

以下按研究问题组织，属于本仓库的阅读建议：

| 研究问题 | 相关论文 |
| --- | --- |
| 表格表示怎样影响模型表现？ | Same Content, Different Representations → OHD |
| 如何保留层次表头并完成复杂推理？ | OHD → ASTRA → SMART |
| 如何理解和操作真实电子表格？ | SpreadsheetAgent → SheetCompass |
| 如何评估复杂表格结构与推理？ | RealHiTBench → CompTab |
| 如何评估多轮交互与端到端工作流？ | TableAgent-Bench → CITBench → SpreadsheetBench 2 |

## 维护方式

- 按论文主要贡献归入一个主分类，可添加多个关键词。
- 优先链接 arXiv、会议论文集、OpenReview 或作者官方项目。
- 预印本年份与会议年份分别记录；未确认的发表状态、代码地址不做推测。
- 新条目沿用“标题 → 作者 / 发表 → 关键词 → 核心内容 → 资源”格式。
- 本仓库收录论文索引与原创简述，论文、代码和数据的权利归原作者；访问资源时遵循各自许可。
