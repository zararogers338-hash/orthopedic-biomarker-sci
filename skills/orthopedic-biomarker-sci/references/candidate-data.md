# 候选公开数据

核查日期：2026-10-14。已核对官方记录，未下载完整矩阵、核验文件校验和或完成供体级质量审计。样本量按原始记录表述，不等于最终可纳入 n。以下是选题线索，不是默认必须全部使用的数据清单。

## 首选 膝骨关节炎

| 来源 | 已核实设计与文件 | 用途与限制 |
|---|---|---|
| [GSE255460](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE255460) | 人膝软骨 scRNA-seq；19份组织来自8名OA及3名非OA供体，8名OA各有WB/NWB区域配对样本。提供 MTX/TSV、metadata、counts及SRA入口 | 发现与细胞来源定位。19不是19名供体；负重/非负重不能直接改名病变/正常；非OA仅3人 |
| [GSE152805](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE152805) | 3名膝OA供体，9份配对滑膜、相对完整外侧胫骨软骨、受损内侧胫骨软骨；MTX/TSV及SRA | 辅助定位与组织互作假设；无健康供体，不能作独立健康对照 |
| [GSE114007](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE114007) | 人膝软骨 bulk RNA-seq，18正常及20 OA样本；两个测序平台。提供 raw_counts.xlsx、标准化计数及SRA | 候选复现；需核实供体、年龄、性别、平台混杂及与其他研究的独立性。若用于筛候选则记为开发数据 |
| [GSE117999](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE117999) | Agilent软骨芯片，存档12 APM非OA＋12 TKA末期OA；原记录排除 P4-010、P4-012、P4-104、P4-108。提供原始TXT及标准化矩阵 | 拟保留的跨平台验证；先查排除和最终分组，不能直接报24纳入。APM不等于完全健康；与GSE98918需核查同院同编号供体重叠 |
| [PXD023708](https://proteomecentral.proteomexchange.org/cgi/GetDataset?ID=PXD023708) | 人滑液DIA蛋白组。[PRIDE入口](https://www.ebi.ac.uk/pride/archive/projects/PXD023708)；[原始研究](https://pmc.ncbi.nlm.nih.gov/articles/PMC8941261/)列7例退变性半月板撕裂/研究定义早期OA、11例晚期TKA、13名无OA证据尸体供体 | 真正第二组学候选。文件与run映射尚未审计；小样本、横断面、尸体与手术取材差异及年龄偏倚。与GEO不能伪造供体配对 |

建议问题：在膝OA中，哪些有明确细胞来源的分泌或基质相关因子，获得跨队列转录与滑液蛋白证据，并能在独立样本或功能实验中被检验？它目前不是早诊、预后或临床应用已验证的命题。

拟定分工是 GSE255460 发现、GSE152805支持、GSE114007候选复现/开发、GSE117999保留评价、PXD023708跨层筛选。最终角色在矩阵审计和独立性核查后冻结。选入候选依据包含哪个数据，该数据就不能同时被称为完全独立的候选验证。

## 备选

| 来源 | 已核实设计与文件 | 用途与限制 |
|---|---|---|
| [GSE153066](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE153066) | 人髓核scRNA-seq，16条记录 CTL1–8/IDD1–8；AllSample.counts.tsv.gz及SRA | 椎间盘退变候选。独立供体数、对照来源、年龄和分级尚待原文/GSM核实 |
| [GSE56081](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE56081) | 人髓核lncRNA/mRNA芯片，5对照＋5退变，记录说明生物学重复；原始TIFF/TXT及处理值 | 小型组织验证。[GSE63492](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE63492)与[GSE67566](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE67566)明确同批5＋5样本，不能当外部验证 |
| [GSE56814](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE56814) | 73名47–56岁白人女性血单核细胞，42高髋BMD、31低髋BMD，包含绝经前后；CEL及处理值 | 骨代谢备选。高/低BMD不是确诊OP/健康分组；血细胞不是骨组织，检查同SuperSeries供体重用 |
| [GSE169396](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE169396) | 人股骨头scRNA-seq，4个sample；MTX/TSV及SRA | 暂限图谱参考。官方series没有可靠OP/非OP标签；二次论文分组不一致，必须追回临床表，不能猜分组 |

2026-10-14启动工程的初始优先级：膝OA、椎间盘退变、骨质疏松。这只是当时资源可行性判断，不是新工程的固定排序。用户有其他样本或平台时重排。

## 使用前验收

逐项完成数据登记、下载可用性、许可、样本/供体映射、病例定义、各组有效n、批次混杂与研究重叠审计。对未知诊断或无法映射供体的数据，不进行假装已确定分组的疾病推断。

若蛋白组无法获取可解释的定量矩阵及样本映射，先寻找另一真实分子层；仍不足时降为跨尺度转录组研究并调整标题与结论，不能用单点蛋白验证冒充第二组学。尚未完成系统新颖性检索，不能把这份可行性清单当作创新证明。
