# RMA Trace

Consumer Electronics After-Sales and Product Traceability System

消费电子产品售后维修与产品追溯管理系统。项目以产品 SN 为入口，覆盖产品数据管理、保修查询、售后申请、RMA、检测、维修、结案和生产批次追查。

## 项目状态

- 当前阶段：需求与数据库设计
- 数据库检查：2026-10-13
- 系统答辩：2026-10-23
- 报告提交：2026-11-01 前

## 技术方案

- Java + Spring Boot
- MyBatis-Plus
- MySQL 8
- HTML + CSS + 原生 JavaScript + Bootstrap
- Maven

浏览器通过 Fetch API 调用 Spring Boot API，服务端负责业务校验和数据库操作。

## 项目文档

- [项目章程](docs/project/PROJECT_CHARTER.md)
- [MVP Spec](docs/spec/MVP_SPEC.md)
- [五人任务包](docs/management/WORK_BREAKDOWN.md)
- [A 任务书](docs/assignments/A.md)
- [B 任务书](docs/assignments/B.md)
- [C 任务书](docs/assignments/C.md)
- [D 任务书](docs/assignments/D.md)
- [E 任务书](docs/assignments/E.md)
- [领域说明](CONTEXT.md)
- [协作规则](CONTRIBUTING.md)

## 协作方式

B、C、D、E Fork 本仓库，在个人 Fork 的功能分支开发，然后向本仓库的 `main` 发起 Pull Request。A 负责审核并使用 merge commit 合并。

开始开发前请先阅读 [协作规则](CONTRIBUTING.md)。

## 配置规则

仓库只提交配置示例。个人数据库账号和密码写入 `application-local.yml`，该文件不会进入 Git。

数据库使用当前快照：

```text
sql/schema.sql
sql/demo-data.sql
```

第一版使用九张表。B、C、D、E 先提交本人负责表的字段初稿，A 检查实体关系和完整性后更新当前 SQL 快照。
