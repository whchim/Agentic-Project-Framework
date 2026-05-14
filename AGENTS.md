# AGENTS.md

这是整个框架的总契约。任何 Agent 在执行任务前都应先阅读。

## 1. 方法论原则
- Spec 即真相
- 先澄清，再设计，再执行
- 分层管理
- 渐进式加载
- 可追溯
- 证据优先
- 人类确认关键决策

## 2. 文档状态机
- Draft
- In Review
- Locked
- Change Requested
- Deprecated
- Archived

## 3. 标准指令集
- /sdd-init
- /sdd-brainstorm
- /sdd-design
- /sdd-plan
- /sdd-breakpoint
- /sdd-recover
- /sdd-review
- /sdd-exec
- /sdd-test
- /sdd-validate
- /sdd-archive
- /sdd-help

## 4. 指令执行总规则
1. 上层文档未锁定，不得生成下层文档
2. Locked 文档修改必须走变更流程
3. 执行前必须检查安全基线和技术约束
4. 关键任务必须写日志
5. 关键阶段必须更新断点
6. 验证必须基于证据，不得口头确认通过

## 5. 权限边界
### Agent 可直接执行
- 创建草稿
- 生成模板
- 写测试
- 写非破坏性代码
- 写日志
- 做验证报告
- 做文档补全

### 必须人类确认
- 修改 Locked 文档
- 新增依赖
- 删除文件
- 修改鉴权/加密/权限逻辑
- 数据库迁移
- 生产发布
- 回滚生产环境

### 禁止自动执行
- 删除生产数据
- 泄露密钥
- 绕过测试/安全检查
- 擅自改审计记录

## 6. 知识加载策略
### 默认加载
- rules/git-workflow.md
- rules/code-style-universal.md
- rules/security-baseline.md
- project/tech-stack.yaml
- project/constraints.yaml
- project/project-profile.yaml

### 按需加载
- rules/testing-guidelines.md
- rules/quality-gate.md
- rules/observability-guidelines.md
- rules/ai-application-guidelines.md
- skills/*.md

## 7. 执行闭环
- Product Spec 定义做什么
- Design Doc 定义怎么做
- Exec Plan 定义先做什么后做什么
- Test 定义怎么证明正确
- Validate 定义是否和 Spec 一致
- Archive 定义如何收口

## 8. 重要补充
- 复杂任务优先使用独立分支或 worktree 隔离
- 核心逻辑优先测试驱动
- 收尾必须完整：测试、审查、文档、日志、归档
- 不确定时先澄清，不要猜