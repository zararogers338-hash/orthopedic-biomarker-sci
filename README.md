# Orthopedic Biomarker SCI

面向骨科生物标志物与转化机制研究的 **Codex 技能与研究工程规划**，围绕选题、公共数据审计、统计设计、实验验证和论文准备组织工作。

*A Codex skill and research planning framework for orthopedic biomarkers, public omics data, experimental validation, and scientific manuscript preparation.*

本项目以 BioFactors 特刊 **Next-Generation Biomarkers: From Multi-Omics Discovery to Clinical Translation** 为初始目标，采用“公共数据＋可补充实验”路线。技能可用于骨关节炎、骨质疏松、椎间盘退变等研究；迁移到新工程时，应重新确认问题、资源和期刊。

**当前版本只有技能、资料索引和研究规划。尚未完成原始数据分析、实验、完整创新性核查或论文投稿，也没有可报告的研究结果。SCI 发表是研究目标，不是录用保证。**

## 可以帮助什么

- 从临床用途、已有研究和真实资源出发，筛选可检验的骨科研究问题。
- 审计公共组学数据的供体、分组、重复采样、批次、队列重叠和数据可用性。
- 区分探索与验证，规划单细胞、跨队列分析及真正不同分子层的证据整合。
- 将每项实验对应到需要检验的主张，明确对照、统计单位与停止条件。
- 整理可追溯的研究记录、英文稿件、图表和投稿材料。

核心约束包括：细胞数不等于病例数，accession 数不等于独立队列数，横断面关联不等于进展预测，组织表达不直接证明体液标志物价值。技能不用于患者个体诊疗。

## 目录

```text
.
├── README.md
├── docs/
│   ├── PROJECT_PLAN.md              # 初始工程规划、阶段交付与条件性排期
│   └── VALIDATION.md                # 技能验证记录与发布检查
└── skills/
    └── orthopedic-biomarker-sci/
        ├── SKILL.md                 # 技能入口、路由与决策规则
        ├── agents/openai.yaml       # 显示名称与默认调用提示
        ├── assets/research-records.md
        └── references/
            ├── target-journal.md
            ├── study-design.md
            ├── candidate-data.md
            ├── analysis-validation.md
            ├── wet-lab-translation.md
            └── publication.md
```

## 安装与调用

1. 下载或克隆本仓库。
2. 将整个 `skills/orthopedic-biomarker-sci` 文件夹复制到自己的 Codex 技能目录：通常为 `~/.codex/skills/`；若配置了 `CODEX_HOME`，则使用其下的 `skills/` 目录。复制后应保留 `SKILL.md`、`agents/`、`assets/` 和 `references/` 的层级。
3. 在 Codex 中显式调用 `$orthopedic-biomarker-sci`。工程规划位于仓库 `docs/`，按任务需要一同提供。

续接本工程的示例：

```text
使用 $orthopedic-biomarker-sci，读取当前仓库的 docs/PROJECT_PLAN.md，
从第一阶段开始，完成膝骨关节炎首选路线的创新性检索、
数据供体关系审计和补实验资源清单；暂不建立预测模型。
```

用于新项目的示例：

```text
使用 $orthopedic-biomarker-sci，为一个椎间盘退变生物标志物项目
比较研究问题与公共数据可行性。先确认本项目的期刊目标、
临床用途和实验条件，不沿用示例工程的疾病排序或队列分工。
```

## 初始研究路线

首选路线是**膝骨关节炎候选分泌因子的跨队列发现、滑液蛋白证据整合与功能验证**。具体候选分子尚未确定，需要先通过新颖性检索、供体与数据审计、可检测性和实验可行性评估。

完整设计、候选队列分工、风险与验收条件见[工程计划](docs/PROJECT_PLAN.md)。技能内的[候选数据索引](skills/orthopedic-biomarker-sci/references/candidate-data.md)收录 9 个候选资源，并记录其对照、重复和解释限制；这些线索不能代替原始矩阵及供体对应关系审计。

建议依次推进：可行性与资源核验 → 方案锁定与小规模试运行 → 发现与候选收敛 → 独立复现与实验 → 证据整合和稿件 → 投稿准备。每一阶段的研究结论都应由实际证据决定。

## 研究状态与使用边界

资料快照日期为 **2026-10-14**。初始计划暂按 Wiley 所列 **2027-03-15** 截止日期排期，同时保留 IUBMB 旧月报日期冲突的记录；特刊状态、截止日期、指南、数据权限、收录和费用须在实际使用时复核。来源和读取限制见[目标期刊记录](skills/orthopedic-biomarker-sci/references/target-journal.md)。

[验证记录](docs/VALIDATION.md)说明了技能结构、引用及行为场景的检查范围。它不证明数据质量、研究创新性、实验可行性或可发表性。仓库不包含患者数据、原始组学矩阵、已完成的分析流程或实验结果；公共数据需按其来源条款取得和使用。

## 主要来源

- [BioFactors 指定特刊](https://iubmb.onlinelibrary.wiley.com/hub/journal/18728081/call-for-papers/si-2025-001652)与[征稿列表](https://iubmb.onlinelibrary.wiley.com/hub/journal/18728081/call-for-papers)。
- [BioFactors 作者指南](https://iubmb.onlinelibrary.wiley.com/hub/journal/18728081/author-guidelines.html)。
- [NCBI GEO](https://www.ncbi.nlm.nih.gov/geo/) 与 [ProteomeXchange](https://www.proteomexchange.org/)：具体 accession 和原始研究链接保存在候选数据索引。
- [FDA–NIH BEST](https://www.ncbi.nlm.nih.gov/books/NBK326791/)、[TRIPOD+AI](https://www.bmj.com/content/385/bmj-2023-078378)、[PROBAST+AI](https://www.bmj.com/content/388/bmj-2024-082505)：按研究问题选择适用定义与方法要求。

本项目为研究辅助材料，与期刊、出版商及上述数据库不存在官方隶属或认可关系。
