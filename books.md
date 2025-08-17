# 编码 / 重构 / 测试 实践原则来源书单 (Books Sourcing Our Coding, Refactoring & Testing Rules)

> 目标：列出本仓库中“实现与代码质量”“重构模式”“测试与质量保障”相关可操作规则与度量的主要来源书籍；为进一步扩展知识库与溯源提供索引。仅收录与**代码结构、命名、复杂度控制、重构技法、测试策略/覆盖、演进遗留代码**直接相关的典型著作。

## 快速导航
- [核心必读 Top 5](#核心必读-top-5)
- [按领域分组清单](#按领域分组清单)
- [详细书目索引](#详细书目索引)
- [规则 / 度量 映射表](#规则--度量-映射表)
- [推荐阅读路径](#推荐阅读路径)
- [扩展/可选书籍](#扩展可选书籍)

---
## 核心必读 Top 5
| 顺序 | 书名                                       | 关键理由                                           | 直接影响规则                                              |
| ---- | ------------------------------------------ | -------------------------------------------------- | --------------------------------------------------------- |
| 1    | 《代码整洁之道》Clean Code                 | 小函数、少参数、命名、SRP、避免布尔旗标            | 函数行数/参数阈值, boolean flag 禁止, 单一抽象层级 (SLAP) |
| 2    | 《重构》Refactoring                        | 系统化重构目录（提取函数/引入参数对象/内联变量等） | 重构建议动作库, 复杂度下降策略                            |
| 3    | 《程序员修炼之道》The Pragmatic Programmer | DRY, 正交性, 断言式思维, 约定优于配置              | 规则去重、工具化思维、脚本化自动化                        |
| 4    | 《代码大全》Code Complete                  | 设计构造技巧、规模控制、可读性与维护成本模型       | 函数/类规模、命名一致性、注释策略参考                     |
| 5    | 《Working Effectively with Legacy Code》   | “缝合测试”、隔离变更、防回归保护性测试             | 遗留代码重构前置测试策略、变更安全网                      |

---
## 按领域分组清单
### A. 编码规范 / 设计细节（Code Construction）
- 《代码整洁之道》Clean Code (Robert C. Martin)
- 《代码大全》Code Complete (Steve McConnell)
- 《程序员修炼之道》The Pragmatic Programmer (Andrew Hunt, David Thomas)
- Effective Java (Joshua Bloch)
- Effective Python (Brett Slatkin)
- Effective C++ / More Effective C++ (Scott Meyers)
- Fluent Python (Luciano Ramalho)
- The Go Programming Language (Alan A. A. Donovan, Brian W. Kernighan)
- Design Patterns: Elements of Reusable Object-Oriented Software (GoF) — 仅限其对解耦与替换条件逻辑的影响
- Software Metrics (多作者/汇编) — 度量基线参考

### B. 重构 / 结构演进
- 《重构：改善既有代码的设计》Refactoring (Martin Fowler & catalog contributors)
- Working Effectively with Legacy Code (Michael Feathers)
- Refactoring to Patterns (Joshua Kerievsky)
- Clean Architecture (Robert C. Martin) — 分层边界、依赖方向
- Growing Object-Oriented Software, Guided by Tests (Freeman & Pryce) — 测试驱动演进结构

### C. 测试策略 / 测试设计
- Test-Driven Development: By Example (Kent Beck)
- xUnit Test Patterns (Gerard Meszaros)
- Unit Testing Principles, Practices, and Patterns (Vladimir Khorikov)
- Growing Object-Oriented Software, Guided by Tests (Freeman & Pryce)
- Working Effectively with Legacy Code (覆盖缝合测试策略)

### D. 语言特化/惯用法（支持参数/接口/抽象决策）
- Effective Java / Effective Python / Effective C++ / Fluent Python / The Go Programming Language

### E. 度量与质量经济性
- Accelerate (Forsgren et al.) — 仅用于交付与失败率、MTTR 等宏观指标（辅助，但不列入编码直接规则）
- Software Metrics — 本地结构性指标的历史阈值参考（函数行数、复杂度、接口大小）

### F. 结构 / 交付 / 运维（Structure / Delivery / Operations）
> 该区段聚焦跨代码层面的“架构边界、交付流水线、可用性/可靠性”支撑书籍；暂不全部纳入核心规则，仅做候选来源。你可根据是否需要相关规则（架构依赖扫描、变更失败率、恢复时间、领域边界一致性等）决定是否提升为核心。

- Clean Architecture (Robert C. Martin) — 分层边界、依赖方向（已在上文引用）
- Accelerate (Forsgren, Humble, Kim, 2018) — 交付四关键指标（变更失败率/部署频率等）
- Continuous Delivery (Humble & Farley, 2010) — 部署流水线、环境一致性（扩展）
- Site Reliability Engineering / SRE Workbook (Beyer et al., Google) — 错误预算 / SLO / MTTR（扩展）
- Domain-Driven Design (Eric Evans, 2003) — 限界上下文、通用语言（可选）
- The DevOps Handbook (Kim et al.) — 三条路径/反馈/持续学习（可选）
- Chaos Engineering (Basiri et al./Principles of Chaos Eng.) — 主动故障演练（可选）

标签说明：未标注 = 当前已部分引用；“扩展”= 可能支持中期新增规则；“可选”= 暂不直接生成代码级或 PR 级自动化信号。

> 注：本书单聚焦代码层实践；架构、流程、团队类书籍（如 DDD、Peopleware、Mythical Man-Month）暂不列入——除非其段落直接被用作函数/类/测试规则来源。

---
## 详细书目索引
| 标识   | 中文 / 英文书名                                                                                  | 作者                        | 主领域标签   | 核心贡献关键词                                                 |
| ------ | ------------------------------------------------------------------------------------------------ | --------------------------- | ------------ | -------------------------------------------------------------- |
| CC     | 代码整洁之道 / Clean Code                                                                        | Robert C. Martin            | 编码, 测试   | 小函数, SRP, 参数最少, 命名, FIRST 测试, Boy Scout Rule        |
| REF    | 重构 / Refactoring                                                                               | Martin Fowler               | 重构         | 重构目录, 小步修改, 无行为改变保障                             |
| PP     | 程序员修炼之道 / Pragmatic Programmer                                                            | Hunt & Thomas               | 编码         | DRY, Orthogonality, Automate, Tracer Bullets                   |
| CCOMP  | 代码大全 / Code Complete                                                                         | Steve McConnell             | 编码         | 构造层实践, 规模/复杂度讨论, 命名与注释策略                    |
| WELC   | Working Effectively with Legacy Code                                                             | Michael Feathers            | 重构, 测试   | 缝合测试, 依赖隔离缝 seam, 防回归安全网                        |
| TDD    | Test-Driven Development: By Example                                                              | Kent Beck                   | 测试, 设计   | Red-Green-Refactor 循环, 三法则 (Fake it / Obvious / Refactor) |
| XUP    | xUnit Test Patterns                                                                              | Gerard Meszaros             | 测试         | 测试坏味道, Fixture 模式, 测试隔离                             |
| UTPP   | Unit Testing Principles, Practices, and Patterns                                                 | Vladimir Khorikov           | 测试         | 可维护测试结构, 测试分类, 价值聚焦                             |
| GOO    | Growing OO Software, Guided by Tests                                                             | Freeman & Pryce             | 测试, 设计   | Outside-In, London School TDD, Mock 协作                       |
| R2P    | Refactoring to Patterns                                                                          | Joshua Kerievsky            | 重构         | 由坏味道 → 模式过渡策略                                        |
| ASD    | 敏捷软件开发：原则、模式与实践 / Agile Software Development: Principles, Patterns, and Practices | Robert C. Martin            | 结构, 设计   | SOLID 汇总, 组件设计 (CCP/CRP), 组件依赖 (ADP/SDP/SAP)         |
| EA-J   | Effective Java                                                                                   | Joshua Bloch                | 编码         | 不可变性, Builder, equals/hashCode 合约                        |
| EA-Py  | Effective Python                                                                                 | Brett Slatkin               | 编码         | Pythonic idioms, 函数签名优化, 可读性                          |
| EA-C++ | Effective C++ 系列                                                                               | Scott Meyers                | 编码         | RAII, Rule of Three/Five/Zero, const 正确性                    |
| FPY    | Fluent Python                                                                                    | Luciano Ramalho             | 编码         | 数据模型协议, 可迭代协议, Pythonic 设计                        |
| GO     | The Go Programming Language                                                                      | Donovan & Kernighan         | 编码         | 接口 ≤3 方法, error 处理, 并发模型                             |
| DP     | Design Patterns                                                                                  | GoF                         | 设计, 重构   | 用策略/状态等消除条件, 解耦可替换性                            |
| CA     | Clean Architecture                                                                               | Robert C. Martin            | 结构         | 分层边界, 依赖倒置, 环形架构                                   |
| ACC    | Accelerate                                                                                       | Forsgren, Humble, Kim       | 交付, 度量   | DORA 四指标 (部署频率, 变更前置时间, 变更失败率, MTTR)         |
| CD     | Continuous Delivery                                                                              | Humble & Farley             | 交付, 流水线 | 部署流水线, 环境一致性, 自动化推广                             |
| SRE    | Site Reliability Engineering (含 Workbook)                                                       | Beyer et al. (Google)       | 运维, 可靠性 | 错误预算, SLO, 事件响应, MTTR 降低                             |
| DDD    | Domain-Driven Design                                                                             | Eric Evans                  | 领域, 架构   | 限界上下文, 通用语言, 上下文映射                               |
| DVOPS  | The DevOps Handbook                                                                              | Kim, Humble, Debois, Willis | 交付, 协作   | 三条路径, 快速反馈, 持续学习                                   |
| CHAOS  | Chaos Engineering (Principles/Practice)                                                          | Basiri et al. / Community   | 可靠性, 韧性 | 主动故障注入, 韧性验证                                         |
| SM     | Software Metrics                                                                                 | (Compilation)               | 度量         | 常见尺寸/复杂度指标参考基线                                    |
| R2P-L  | (可选) Refactoring Legacy Code Bases*                                                            | *参考条目                   | 重构         | 进一步遗留策略 (如需扩展)                                      |

---
## 规则 / 度量 映射表
| 规则/度量 (Spec 引用)                 | 主要来源书籍标识 | 说明                                  |
| ------------------------------------- | ---------------- | ------------------------------------- |
| function_line_count ≤20 (warn)        | CC, CCOMP, SM    | 小函数可读性 + 经验阈值 & 度量历史    |
| function_param_count ≤2 常态          | CC, CCOMP        | 低参数 = 降认知负荷/测试复杂度        |
| 禁止 boolean_flag_params              | CC, REF          | Flag 暗示多职责 / 分裂函数            |
| 引入参数对象 (≥3 相关参数)            | REF              | 重构目录：Introduce Parameter Object  |
| Extract Function 使用频率             | REF, CC          | 控制函数长度/职责单一                 |
| Cyclomatic Complexity warn>10 fail>15 | SM, CCOMP, 社区  | 行业内常用上限（可项目化调整）        |
| Cognitive Complexity warn>15 fail>20  | SM (衍生)        | 基于理解成本度量衍生阈值              |
| 接口方法 ≤3 (Go)                      | GO               | Idiomatic Go + ISP 信号               |
| 类 LOC <300                           | CCOMP, SM        | 过大类耦合增长/维护难度上升           |
| Boy Scout Rule                        | CC               | 持续微重构文化                        |
| Red-Green-Refactor 循环               | TDD              | 测试驱动节奏                          |
| FIRST 测试原则                        | CC, XUP, TDD     | 测试质量基准                          |
| 遗留代码缝合测试策略                  | WELC             | 先建保护网再重构                      |
| Outside-In 设计 (服务/Mock)           | GOO              | 自顶向下驱动设计                      |
| 测试坏味道检测                        | XUP              | 识别 Brittle/Obscure/Test Duplication |
| 通过模式重构条件                      | DP, R2P          | Strategy/State 替换复杂条件链         |
| 不可变对象偏好                        | EA-J, EA-Py      | 减少共享可变状态错误                  |
| 资源自动管理 (RAII)                   | EA-C++           | 保证异常安全与释放                    |
| Pythonic 数据模型协议                 | FPY              | 利用魔术方法和协议增强可读性          |
| 依赖倒置/层边界                       | CA               | 防架构腐蚀；月度漂移扫描参考          |
| 组件内聚 (CCP/CRP)                    | ASD              | 组件分组与演化稳定性指导              |
| 组件依赖 (ADP/SDP/SAP)                | ASD              | 无环依赖/稳定方向/抽象与稳定性平衡    |

---
## 推荐阅读路径
1. 入门与心智模型：Clean Code → Pragmatic Programmer → Code Complete (选读章节)
2. 系统化重构：Refactoring → (并行实践) TDD By Example（练节奏）
3. 测试深化：xUnit Test Patterns → Unit Testing PPP → Growing OO Software
4. 遗留系统演进：Working Effectively with Legacy Code（与现有代码基结合）
5. 结构边界与依赖：Clean Architecture → Refactoring to Patterns（择需）
6. 语言特化：Effective 系列 / Fluent Python / Go 语言书（根据实际技术栈）
7. 指标与持续改进：Software Metrics（确定或调整阈值），必要时结合 Accelerate（更高层交付度量）

> 同步实践建议：每读一章节 → 提炼“可自动化信号”与“潜在重构动作” → 更新内部规则 JSON / 度量阈值说明（附来源标识）。

---
## 扩展/可选书籍
| 书名                            | 用途                 | 是否直接影响现行编码/测试规则 |
| ------------------------------- | -------------------- | ----------------------------- |
| Clean Architecture              | 层次与依赖方向约束   | 间接（架构扫描/依赖分析）     |
| Accelerate                      | 交付与稳定性宏观指标 | 否（非代码级）                |
| Domain-Driven Design            | 领域建模/上下文拆分  | 否（编码规则延伸）            |
| Peopleware / Mythical Man-Month | 团队效率与沟通       | 否                            |

---
## 如何在 PR / 规则中引用
统一用 `source:[标识]`；多来源用逗号分隔，例如：
```
"references": ["source:CC", "source:REF"]
```

## 维护策略
- 新增规则必须指向 ≥1 核心书籍章节或页码（可后补）。
- 若规则仅有网络文章来源 → 标注 `source:WEB:<简短slug>` 并优先寻找书籍佐证。
- 每季度审查：未被引用的书籍条目 / 低触发规则 → 评估是否下线或合并。

---
## 术语速览（与书籍交叉）
| 术语               | 源书籍 / 标识 | 简述                                       |
| ------------------ | ------------- | ------------------------------------------ |
| SRP                | CC, REF, ASD  | 单一职责，单一改变原因                     |
| OCP                | ASD           | 对扩展开放，对修改封闭                     |
| LSP                | ASD           | 子类型可替换基类型保持语义正确             |
| ISP                | ASD           | 多个专用接口而非臃肿大接口                 |
| DIP                | ASD, CA       | 高层不依赖具体实现，抽象稳定依赖方向       |
| SOLID              | ASD           | 五原则协同降耦合/提升可维护性              |
| CCP/CRP            | ASD           | 组件内聚/重用发布：同变更原因聚合/一起使用 |
| ADP/SDP/SAP        | ASD           | 无环依赖/依赖稳定/稳定=高抽象度            |
| DRY                | PP            | 消除重复，集中真理来源                     |
| Orthogonality      | PP            | 维度解耦，减少联动修改                     |
| Boy Scout Rule     | CC            | 每次改动顺手改善                           |
| Red-Green-Refactor | TDD           | 最小反馈循环                               |
| Seam               | WELC          | 可注入/替换点，利于测试                    |
| Test Smell         | XUP           | 降低测试价值或稳定性的模式                 |
| Parameter Object   | REF           | 聚合相关参数以降复杂度                     |
| Strategy Pattern   | DP, R2P       | 用多态替代分支                             |

---
### 版权与使用
本清单仅列出公开出版物的书名与高层次实践摘要，不复制受版权保护的原文内容。

> 若需补充具体章节/页码，请在后续 PR 中附加 `page:` 或 `chapter:` 元信息。

---
更新日期：2025-08-17
