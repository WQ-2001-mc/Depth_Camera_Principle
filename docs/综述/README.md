# 深度相机高影响力综述导读

本目录按“技术覆盖面、引用可见度、分类图质量、原理与优缺点比较、应用讨论”筛选综述。核心集合保持为 6 篇英文综述，另保留 1 篇适合中文快速入门的资料。

> 引用数为 OpenAlex 在 2026-07-14 的快照，只用于衡量文献的相对影响和传播度；数据库更新、文献合并及统计口径会导致数值变化。较新的论文天然尚未积累与经典文献相同的引用量。

## 先看哪几篇

如果目标是快速建立完整知识框架，推荐按以下顺序阅读：

1. 先看 `三维相机发展趋势综述_徐红鑫.pdf` 第 2 页图 1，获得中文分类全景；
2. 再看 Giancola 等的综述第 13 页图 1.1，建立“接触/非接触—光学—被动/主动—ToF/结构光/主动双目”的严谨分类；
3. 阅读 Zhang 的结构光综述，掌握编码、傅里叶轮廓术、相移和二值离焦等路线；
4. 阅读 Bamji 等的 iToF 综述，理解 AMCW、解调像素、噪声、MPI、深度处理流水线；
5. 阅读 Li 等的固态 LiDAR 综述第 3 页图 1，再用 Ma、Holzhüter 两篇补齐 dToF/iToF、扫描机构和车载系统设计。

## 核心资料

| 资料 | 影响力快照 | 主要覆盖 | 原理/优缺点/应用 | 分类图与推荐页 | 本地文件 |
|---|---:|---|---|---|---|
| Silvio Giancola et al., *A Survey on 3D Cameras: Metrological Comparison of Time-of-Flight, Structured-Light and Active Stereoscopy Technologies* (2018) | 约 152 次 | ToF、结构光、主动双目、设备与计量误差 | 强：重点比较三类相机的测量原理、精度、误差随距离变化和代表设备 | **强**：PDF 第 13 页图 1.1 为全局分类树；第 16 页图 2.1 对比三类测量原理 | [PDF](01_2018_A_Survey_on_3D_Cameras_Giancola_et_al.pdf) |
| Song Zhang, *High-speed 3D Shape Measurement with Structured Light Methods: A Review* (2018) | 约 933 次 | 结构光、主动/被动方法背景、编码、FTP、相移、二值离焦 | 强：对高速、精度、运动敏感性、硬件约束和应用有系统讨论 | 中：没有单页总思维导图，但第 2–10 页连续原理图完整展示技术演进 | [PDF](02_2018_High_speed_3D_Structured_Light_Review_Zhang.pdf) |
| Cyrus Bamji et al., *A Review of Indirect Time-of-Flight Technologies* (2022) | 约 97 次 | iToF/AMCW、像素与芯片架构、解调、噪声、深度流水线 | **很强**：系统解释环境光、运动模糊、MPI、SNR、滤波和典型应用 | 中：第 2 页给出 ToF 大类关系，第 3–10 页依次覆盖采样、解调、像素和误差处理 | [PDF](03_2022_Review_of_Indirect_ToF_Technologies_Bamji_et_al.pdf) |
| Jie Ma et al., *A Review of ToF-based LiDAR* (2024) | 约 34 次 | dToF、iToF、机械/固态 LiDAR、TX/RX、SPAD 与系统趋势 | **很强**：包含 dToF/iToF 以及机械/固态的直接优缺点表，并讨论人机交互、自动驾驶、工业、医疗、AR 和三维重建 | 强：第 2 页图 1、表 1；第 3 页表 2；第 10 页图 12 | [PDF](04_2024_Review_of_ToF_based_LiDAR_Ma_et_al.pdf) |
| Nanxi Li et al., *A Progress Review on Solid-State LiDAR and Nanophotonics-Based LiDAR Sensors* (2022) | 约 307 次 | 脉冲 ToF、AMCW、FMCW；Flash、MEMS、OPA、光开关、频率梳、超表面 | **很强**：比较传统固态与纳米光子 LiDAR 的性能、集成度、扫描方式和应用潜力 | **很强**：PDF 第 3 页图 1 是本目录最完整的 LiDAR 技术路线图；第 4 页图 2 对比三种测距原理 | [PDF](05_2022_Progress_Review_Solid_State_LiDAR_Li_et_al.pdf) |
| Hanne Holzhüter et al., *Technical Concepts of Automotive LiDAR Sensors: A Review* (2023) | 约 36 次 | 车载需求、模拟/数字 ToF、FMCW、同轴/离轴、扫描结构、波长与器件 | **很强**：按视场、测量原理和波长组织设计空间，第 28 页表 2 汇总各类方案优缺点 | **很强**：PDF 第 3 页图 2 是“视场覆盖—测距原理—波长”三轴设计空间 | [PDF](06_2023_Technical_Concepts_Automotive_LiDAR_Holzhueter_et_al.pdf) |

### 中文快速入门

徐红鑫、裴志伟、王道林、孙博，*三维相机发展趋势综述*，《信息系统工程》2022 年第 6 期，104–108 页。

- 优点：篇幅短，直接覆盖被动双目、ToF、线激光三角测量、散斑、动态结构光，并列出应用和优缺点；PDF 第 2 页图 1 是较全面的中文分类思维导图。
- 局限：期刊影响力和论证深度低于上表英文综述，部分术语与分类口径需要结合 Giancola、Zhang 和 Bamji 等资料交叉核验，适合作为入口，不应作为唯一依据。
- 文件：[三维相机发展趋势综述_徐红鑫.pdf](三维相机发展趋势综述_徐红鑫.pdf)

## 每篇文献解决什么问题

| 想回答的问题 | 优先阅读 |
|---|---|
| 深度相机到底如何分类？ | 中文综述图 1；Giancola 图 1.1 |
| ToF、结构光、主动双目在精度和误差上如何比较？ | Giancola；Ma |
| 条纹结构光有哪些高速测量路线？ | Zhang |
| iToF 如何从调制光得到逐像素深度？主要误差是什么？ | Bamji |
| dToF 与 iToF 的原理、优缺点和应用有何差别？ | Ma 表 1；Bamji |
| Flash、MEMS、OPA 等固态 LiDAR 如何归类？ | Li 图 1；Holzhüter 图 2 |
| 机械、半固态、固态 LiDAR 的系统选择依据是什么？ | Ma 表 2；Holzhüter 表 2 |
| FMCW 与 ToF LiDAR 如何比较？ | Li 图 2 及相关章节；Holzhüter 第 2 节 |

## 未下载但值得知道的综述

- Zhenzhou Wang, *Review of Real-time Three-dimensional Shape Measurement Techniques*, **Measurement** 156 (2020), 107624，[DOI](https://doi.org/10.1016/j.measurement.2020.107624)。它把实时三维测量分为结构光、双目视觉和 ToF，并系统比较优缺点；OpenAlex 快照约 145 次引用。检索时未找到可确认授权的公开 PDF，Zotero 中也没有附件，因此只保留官方索引，不把来源不明的全文放入仓库。
- Wu et al., *Advancements in Key Parameters of Frequency-Modulated Continuous-Wave Light Detection and Ranging: A Research Review* (2024)，[DOI](https://doi.org/10.3390/app14177810)。适合继续深挖 FMCW，但范围较窄，未纳入本轮 6 篇核心集合。
- Qiao et al., *RGB Guided ToF Imaging System: A Survey of Deep Learning-based Methods* (2024)，[arXiv](https://arxiv.org/abs/2405.10357)。适合研究 RGB-ToF 深度补全与融合，不属于基础测距原理综述。

## 来源与版权边界

- Giancola 综述可在 [KAUST 机构知识库](https://repository.kaust.edu.sa/items/82af2c91-3ca2-491a-9648-4f2e2a8b9988)公开访问；本地文件来自个人 Zotero 附件。
- Zhang 综述从[普渡大学作者主页公开 PDF](https://engineering.purdue.edu/ZhangLab/publications/papers/2018-ole-realtime.pdf)下载。
- Ma 综述在 [Journal of Semiconductors 文章页](https://www.jos.ac.cn/en/article/doi/10.1088/1674-4926/24040015)提供 HTML 和 PDF 全文；本地文件来自个人 Zotero 附件。
- Li 综述为开放获取文章，文章标注 CC BY；本地文件来自个人 Zotero 附件。
- Holzhüter 综述可从 [SPIE Digital Library](https://doi.org/10.1117/1.OE.62.3.031213)公开阅读 PDF，但页面未显示明确的开放许可；本地文件来自个人 Zotero 附件。
- Bamji 的 IEEE 版本在 OpenAlex 中为闭源，当前本地文件来自个人 Zotero，仅用于个人学习研究。**若仓库公开发布，应先移除该 PDF 或取得明确传播授权，只保留 DOI 与导读。**
- 中文综述的公开传播许可未能确认。**若仓库公开发布，应先核验来源和授权。**

收录 PDF 不改变原始版权。对于没有明确开放许可证的文件，不应仅因“网络可下载”或“个人 Zotero 已有附件”而推定可以重新公开分发。

## 文件校验

| 文件 | 页数 | SHA-256 |
|---|---:|---|
| `01_2018_A_Survey_on_3D_Cameras_Giancola_et_al.pdf` | 97 | `befeb7d99c810531286d0d67344e5e59e2d406de9d7eff734610fd8ede475ea1` |
| `02_2018_High_speed_3D_Structured_Light_Review_Zhang.pdf` | 13 | `194bba4e3c783172ca9627c9135308b9cb77394ec3b40969f68823cde5d10c29` |
| `03_2022_Review_of_Indirect_ToF_Technologies_Bamji_et_al.pdf` | 15 | `5c76045d9bec222adb5ae422e2c3e92a0c3523629298d4b1f4e419a8e71069b4` |
| `04_2024_Review_of_ToF_based_LiDAR_Ma_et_al.pdf` | 13 | `226fee595b179cba48d0cd6b1695f733ef5dca69b7800e5b3a223ce0fd739c1a` |
| `05_2022_Progress_Review_Solid_State_LiDAR_Li_et_al.pdf` | 24 | `e979f78aa3ad7381a0e39dfe7e53b47f213b959e0100767e8591f6150a651570` |
| `06_2023_Technical_Concepts_Automotive_LiDAR_Holzhueter_et_al.pdf` | 34 | `e57aacf8c723b9d0ac7c2e112bc3c43ee8ab392a17dd49ddfac14cc648708ff4` |
| `三维相机发展趋势综述_徐红鑫.pdf` | 5 | `e6e3b23eff065ba67107dfa5eaaeea29b58191d1bc4532dd5d73f26498d7a0f4` |

## 检索说明

- 检索范围：多源互联网学术检索、出版社/作者/机构页面、OpenAlex 引用快照，以及本机 Zotero 的“深度相机、结构光、双目、ToF、dToF/SPAD、iToF、LiDAR”相关集合。
- Zotero 数据库使用 SQLite `immutable=1` 只读查询；没有修改条目、集合、标签或附件。
- 选择逻辑：优先保留能解释物理原理、分类、误差、优缺点和应用的综述，剔除只讨论单一网络、单一数据集或单一产品的文章。
