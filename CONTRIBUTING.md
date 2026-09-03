# Contributing

## 仓库角色

- A 管理上游仓库，可以从本机直接提交并推送 `main`，同时审核和合并成员 PR。
- B、C、D、E 使用个人 Fork 开发。
- GitHub Issues 记录任务、负责人、依赖、截止日期和验收条件。

## A 的本机操作

A 使用上游仓库的本地检出，不需要为自己的改动创建 PR：

```bash
git switch main
git pull --ff-only origin main
# 修改并检查相关文件
git status --short
git diff
git add <本次相关路径>
git commit -m "<type>: <summary>"
git push origin main
```

每次提交只包含当前任务相关文件。直接推送不改变 B、C、D、E 的 Fork + PR 流程。

## 首次设置

先在 GitHub Fork `Jul1en-Lin/rma-trace`，然后执行：

```bash
git clone https://github.com/<你的用户名>/rma-trace.git
cd rma-trace
git remote add upstream https://github.com/Jul1en-Lin/rma-trace.git
git remote -v
```

`origin` 指向个人 Fork，`upstream` 指向 A 的仓库。

## 开始 Issue

```bash
git switch main
git fetch upstream
git merge upstream/main
git push origin main
git switch -c feat/<issue-number>-<short-name>
```

分支示例：

```text
feat/12-warranty-query
fix/27-rma-status-check
docs/31-product-er
```

## 提交与推送

提交信息使用英文类型和简短说明：

```text
feat: add warranty query API
fix: reject repair on closed RMA
docs: update product ER diagram
test: add service request validation cases
```

开发完成后推送个人分支：

```bash
git push -u origin feat/<issue-number>-<short-name>
```

## Pull Request

创建 PR 时确认：

```text
base repository: Jul1en-Lin/rma-trace
base branch: main
head repository: <你的用户名>/rma-trace
compare branch: 你的功能分支
```

PR 必须满足：

- 关联对应 Issue。
- 写明实现内容和验收结果。
- 提供接口结果、测试输出或页面截图。
- 表结构变化同步更新模块 ER 图和字段说明。
- 个人配置、密码、IDE 文件和生成目录未进入提交。
- A 提出的审核意见已经处理或说明原因。

A 合并成员 PR 时使用 merge commit，保留 no-ff 的分支历史。

## 文档同步

代码修改影响业务规则、表结构、接口或职责时，在同一个 PR 内更新对应文档。个人任务书不记录每日进度，实时状态只写入 GitHub Issues。

## 求助方式

卡住时先在 Issue 写清：

1. 当前现象
2. 期望结果
3. 已经尝试的办法
4. 相关日志或截图

然后 @A 或 @B。A、B 先提供提示或示例，原负责人继续完成任务。
