# 标准 / 规范来源 (Standards & Specifications)

> 目的：集中列出非书籍的正式标准/行业规范（RFC、ISO、语言规范等）供规则映射使用。
>
> 标记：core=当前规则已引用；candidate=可能纳入；optional=背景。

| 标识     | 名称                                       | 机构/作者      | 年份 | 标签     | 相关领域    | 用途示例                | 状态      |
| -------- | ------------------------------------------ | -------------- | ---- | -------- | ----------- | ----------------------- | --------- |
| RFC1122  | Internet Host Requirements                 | IETF           | 1989 | 协议     | 网络健壮性  | Postel Law 上下文       | optional  |
| SEMVER   | Semantic Versioning 2.0.0                  | Preston-Werner | 2013 | 版本     | 发布/兼容性 | 版本变更分类 gate       | core      |
| HTTP7231 | HTTP/1.1 Semantics and Content             | IETF           | 2014 | 协议     | REST 语义   | 幂等/安全/缓存 规则依据 | optional  |
| PEP8     | Python Enhancement Proposal 8              | Python.org     | 持续 | 代码风格 | Python      | 格式化/lint 统一        | candidate |
| PEP484   | Python Type Hints                          | Python.org     | 2015 | 类型     | Python      | 公共 API 类型覆盖率     | candidate |
| OCIIMG   | OCI Image Spec                             | OCI            | 2017 | 容器     | 交付        | 镜像构建合规扫描        | optional  |
| SLSA     | Supply-chain Levels for Software Artifacts | OpenSSF        | 2021 | 供应链   | 安全        | 构建来源、签名等级      | candidate |

## 维护
- 与 `books.md` 解耦；当规则 JSON 引用标准时统一 `source:STD:<标识>`。
- candidate 连续两个发布周期无落地 → optional。
