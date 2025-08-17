# 论文 / 学术与经典技术文献来源 (Papers & Academic / Classic Technical Sources)

> 目的：集中列出被引用或潜在引用、但不属于书籍的论文 / 技术报告 / RFC / 白皮书，用于规则、度量、设计原则的权威出处。与书籍分离，避免混淆。
>
> 分类标签：
> - core: 已在规则或度量中直接引用
> - candidate: 未来可能转化为规则/度量
> - optional: 仅背景参考，不直接转化

| 标识       | 引用形式                                                                                       | 年份      | 类型              | 标签      | 关键贡献                  | 适用潜在规则/度量            | 备注                   |
| ---------- | ---------------------------------------------------------------------------------------------- | --------- | ----------------- | --------- | ------------------------- | ---------------------------- | ---------------------- |
| LISKOV87   | Barbara Liskov - Data Abstraction & Hierarchy / Liskov Substitution Principle (with Wing 1994) | 1987/1994 | paper             | core      | 子类型行为语义约束 (LSP)  | OCP/LSP 适配性检查（未来）   | 语义正确性难自动判定   |
| PARNAS72   | David Parnas - On the Criteria To Be Used in Decomposing Systems into Modules                  | 1972      | paper             | core      | 信息隐藏 / 模块化分解     | 信息隐藏扫描（封装泄漏启发） | 可与依赖方向结合       |
| DIJKSTRA74 | E. W. Dijkstra - On the role of scientific thought (关注点分离)                                | 1974      | paper             | candidate | SoC/结构化思维            | 分层/关注点扫描              | 概念抽象程度高         |
| YOURDON79  | Yourdon & Constantine - Structured Design                                                      | 1979      | book/paper hybrid | core      | 高内聚/低耦合 定义        | 耦合/内聚度量基线            | 已在速查表出现         |
| SALTZER75  | Saltzer & Schroeder - The Protection of Information in Computer Systems                        | 1975      | paper             | optional  | 最小特权 (POLP)           | 权限最小化策略               | 安全非当前核心编码规则 |
| POSTEL80   | RFC 761 / 1122 (Postel's Law)                                                                  | 1980/1989 | RFC               | optional  | 发送保守接收宽容          | 输入解析健壮性指导           | 现代需安全收敛策略     |
| SEMVER     | Semantic Versioning 2.0.0 Spec                                                                 | 2013      | spec              | core      | 版本号兼容语义            | 发布变更分类校验             | 解析简单，可自动化     |
| HTTP7231   | HTTP/1.1 Semantics and Content (RFC 7231)                                                      | 2014      | RFC               | optional  | 幂等/安全/可缓存 动词语义 | 幂等性检测策略               | 需接口描述文件支持     |
| SRE        | Google SRE Book & Workbook                                                                     | 2016+     | book/site         | candidate | 错误预算 / SLO / MTTR     | MTTR/失败率基线来源          | 架构/运维层            |
| CHAOS      | Principles of Chaos Engineering                                                                | 2017      | site/paper        | optional  | 主动故障注入理念          | 未来演练检测                 | 非代码静态规则         |
| ACCEL      | Accelerate (四关键指标研究方法)                                                                | 2018      | research/book     | core      | DORA 指标统计方法         | change_failure_rate 等       | 与度量体系对接         |

## 维护策略
- 新增引用先加入 candidate；落地规则后升 core。
- 若 2 个季度未被任何规则/指标引用 → 降为 optional 或移除。
- 统一引用格式：`source:PAPER:<标识>` / `source:RFC:<标识>` / `source:SPEC:<标识>`。

