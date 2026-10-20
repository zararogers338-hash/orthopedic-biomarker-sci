# Orthopedic Biomarker SCI

面向骨科生物标志物与转化机制研究的 **Codex 技能与研究工程规划**，围绕选题、公共数据审计、统计设计、实验验证和论文准备组织工作。

*A Codex skill and research planning framework for orthopedic biomarkers, public omics data, experimental validation, and scientific manuscript preparation.*

本项目采用“公共数据＋可补充实验”路线。技能可用于骨关节炎、骨质疏松、椎间盘退变等研究；迁移到新工程时，应重新确认问题、资源和期刊。

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
建议依次推进：可行性与资源核验 → 方案锁定与小规模试运行 → 发现与候选收敛 → 独立复现与实验 → 证据整合和稿件 → 投稿准备。每一阶段的研究结论都应由实际证据决定。

