# 博客 / 社区 / 非正式来源 (Blogs & Community Sources)

> 目的：列出启发性但非正式出版物的来源（博客文章、社区约定、演讲），与书籍/论文/标准分离，确保溯源层次清晰。
>
> 仅当缺乏书籍/论文佐证时临时引用；后续应回补权威来源。
>
> 标签：temporary=待用正式来源替换；influential=社区常用；background=背景材料。

| 标识       | 名称 / 文章标题                             | 作者 / 社区           | 年份  | 标签        | 关键概念                       | 可能映射规则              | 状态       |
| ---------- | ------------------------------------------- | --------------------- | ----- | ----------- | ------------------------------ | ------------------------- | ---------- |
| JOEL-LA    | The Law of Leaky Abstractions               | Joel Spolsky          | 2002  | influential | 抽象泄漏不可避免               | 网络/远程调用防御         | active     |
| ROR-CONV   | Rails Convention over Configuration         | Rails Community / DHH | 2004+ | influential | 约定优于配置                   | 项目脚手架默认结构        | active     |
| GO-PROV    | Go Proverbs (Go 习语合集)                   | Rob Pike 等           | 2015  | influential | 接口小/错误就是值/不要滥用继承 | 接口法数阈值/错误处理习惯 | active     |
| CHAOS-BLOG | Principles of Chaos Engineering (blog form) | Netflix / Community   | 2016+ | background  | 主动故障注入                   | 演练计划指引              | background |
| TRUNK      | Trunk-Based Development (site)              | Community             | 201x  | influential | 小批量集成，减少分支漂移       | 提交/PR 策略              | active     |

## 引用格式
- 使用 `source:BLOG:<标识>`。
- 若后续找到对应书籍/论文，将规则引用迁移并将该条降级为 background。

## 审查策略
- 每季度审查是否仍需保留 temporary/influential 条目。
