# Agentic Project Framework

> 一个面向 **AI + 人类协作** 的项目基础框架，用于统一需求、设计、执行、验证、归档流程。  
> 适用于需要可追溯、可恢复、可复用、可审查的项目。

---

## 目录

- [这是什么](#这是什么)
- [核心目标](#核心目标)
- [适用场景](#适用场景)
- [仓库结构总览](#仓库结构总览)
- [推荐阅读顺序](#推荐阅读顺序)
- [标准工作流](#标准工作流)
- [如何开始一个新项目](#如何开始一个新项目)
- [如何处理变更](#如何处理变更)
- [如何恢复中断任务](#如何恢复中断任务)
- [示例项目](#示例项目)
- [维护原则](#维护原则)
- [相关文档](#相关文档)

---

## 这是什么

这是一个用于组织项目全生命周期的框架仓库。

它不是单纯的代码仓库，也不是单纯的文档仓库，而是一套把以下内容标准化的系统：

- 需求表达
- 方案设计
- 任务拆解
- 开发执行
- 测试验证
- 过程记录
- 变更控制
- 最终归档

它的目标是让 AI 和人类在同一个规则系统下协作，减少混乱、返工和上下文丢失。

---

## 核心目标

这套框架主要解决以下问题：

- 需求不清晰
- 设计与实现脱节
- 任务没有拆解
- 过程没有记录
- 中断后难以恢复
- 变更缺少控制
- 交付后缺少归档

因此，本仓库强调：

- **Spec-first**：先需求，再设计，再计划
- **Evidence-first**：以验证和记录作为依据
- **Traceable**：所有关键决策可追踪
- **Recoverable**：任务中断后可恢复
- **Reusable**：模板、规则、技能可复用
- **Isolated work**：复杂任务尽量隔离处理

---

## 适用场景

适合以下类型的项目：

- AI 辅助开发项目
- 多人协作项目
- 长周期项目
- 需要审计与追踪的项目
- 需要规范需求变更的项目
- 需要文档、设计、执行闭环的项目

也适合作为：

- 团队项目模板
- Agent 工作流模板
- 复杂任务执行框架
- 文档治理框架
- 需求与设计沉淀框架

---

## 仓库结构总览

- `README.md`：仓库入口
- `AGENTS.md`：Agent 总契约
- `.gitignore`：忽略本地临时文件、构建产物、缓存等
- `.env.example`：环境变量样例

- `docs/`：说明性文档
  - `docs/methodology.md`：方法论说明
  - `docs/quick-start.md`：快速开始文档
  - `docs/command-reference.md`：命令参考文档
  - `docs/repository-index.md`：仓库索引文档
  - `docs/README.md`：`docs/` 目录入口页

- `project/`：当前项目画像与约束
  - `project/project-profile.yaml`：项目画像
  - `project/tech-stack.yaml`：技术栈声明
  - `project/constraints.yaml`：项目约束
  - `project/team-guidelines.md`：团队协作规范
  - `project/architecture-decisions/ADR-TEMPLATE.md`：架构决策记录模板

- `specs/`：需求、设计、计划、上下文、变更
  - `specs/SDD_BREAKPOINT.md`：断点文件
  - `specs/CONTEXT_SUMMARY.md`：上下文摘要
  - `specs/product-spec/PRODUCT_SPEC_TEMPLATE.md`：需求模板
  - `specs/product-spec/README.md`：Product Spec 编写说明
  - `specs/design-doc/DESIGN_DOC_TEMPLATE.md`：设计模板
  - `specs/design-doc/README.md`：Design Doc 编写说明
  - `specs/exec-plan/EXEC_PLAN_TEMPLATE.md`：执行计划模板
  - `specs/exec-plan/README.md`：Exec Plan 编写说明
  - `specs/change-requests/CHANGE_REQUEST_TEMPLATE.md`：变更申请模板
  - `specs/change-requests/.gitkeep`：目录占位文件

- `rules/`：治理规则与质量标准
  - `rules/git-workflow.md`：Git 工作流规范
  - `rules/code-style-universal.md`：通用代码风格规范
  - `rules/security-baseline.md`：安全基线规范
  - `rules/testing-guidelines.md`：测试规范
  - `rules/quality-gate.md`：质量门禁规则
  - `rules/dependency-management.md`：依赖管理规范
  - `rules/environment-management.md`：环境管理规范
  - `rules/observability-guidelines.md`：可观测性规范
  - `rules/ci-cd-guidelines.md`：CI/CD 规范
  - `rules/ai-application-guidelines.md`：AI 应用规范
  - `rules/code-style-language/python.md`：Python 风格规范
  - `rules/code-style-language/javascript.md`：JavaScript 风格规范
  - `rules/code-style-language/typescript.md`：TypeScript 风格规范

- `skills/`：执行动作与场景方法
  - `skills/brainstorm.md`：需求澄清与方案发散
  - `skills/spec-writing.md`：需求文档编写
  - `skills/design-review.md`：设计评审
  - `skills/plan-writing.md`：执行计划编写
  - `skills/worktree-management.md`：worktree 管理
  - `skills/test-writing.md`：测试编写
  - `skills/debugging.md`：调试
  - `skills/code-review.md`：代码审查
  - `skills/breakpoint-management.md`：断点管理
  - `skills/finishing-branch.md`：任务收尾

- `logs/`：过程记录与决策留痕
  - `logs/task-execution.log`：任务执行过程
  - `logs/spec-changes.log`：需求变更记录
  - `logs/validation.log`：验证结果记录
  - `logs/decision-log.md`：关键决策记录

- `archives/`：归档结果
  - `archives/.gitkeep`：目录占位文件

- `examples/`：示例项目与变更样例
  - `examples/README.md`：示例区说明
  - `examples/sample-project/`：完整示例项目
    - `examples/sample-project/README.md`
    - `examples/sample-project/project-profile.yaml`
    - `examples/sample-project/product-spec.md`
    - `examples/sample-project/design-doc.md`
    - `examples/sample-project/exec-plan.md`
    - `examples/sample-project/validation-report.md`
    - `examples/sample-project/archive-summary.md`
  - `examples/sample-change-request/change-request.md`：变更请求示例

---

## 推荐阅读顺序

如果你是第一次进入这个仓库，建议按以下顺序阅读：

1. `README.md`
2. `AGENTS.md`
3. `docs/repository-index.md`
4. `docs/quick-start.md`
5. `project/project-profile.yaml`
6. `project/constraints.yaml`
7. `rules/security-baseline.md`
8. `rules/testing-guidelines.md`
9. `rules/quality-gate.md`
10. `examples/sample-project/README.md`

---

## 标准工作流

推荐的标准闭环如下：

- 需求提出
- brainstorm
- Product Spec
- Spec Review
- Design Doc
- Design Review
- Exec Plan
- 执行开发
- 测试验证
- 质量门禁
- 归档

### 工作流说明

- **brainstorm**：先澄清目标和边界
- **Product Spec**：把需求写清楚
- **Design Doc**：把方案设计清楚
- **Exec Plan**：把任务拆解清楚
- **执行开发**：按计划实现
- **测试验证**：验证是否满足需求
- **质量门禁**：确认是否可合并或交付
- **归档**：沉淀最终结果

---

## 如何开始一个新项目

建议按以下步骤进行：

### 1. 填写项目画像

编辑：

- `project/project-profile.yaml`
- `project/tech-stack.yaml`
- `project/constraints.yaml`

### 2. 确认团队规则

如有需要，更新：

- `project/team-guidelines.md`

### 3. 编写需求

使用：

- `specs/product-spec/PRODUCT_SPEC_TEMPLATE.md`

### 4. 编写设计

使用：

- `specs/design-doc/DESIGN_DOC_TEMPLATE.md`

### 5. 编写执行计划

使用：

- `specs/exec-plan/EXEC_PLAN_TEMPLATE.md`

### 6. 执行开发与验证

同步更新：

- `logs/task-execution.log`
- `logs/decision-log.md`
- `logs/validation.log`

### 7. 完成归档

将最终产物收口到：

- `archives/`

---

## 如何处理变更

如果需求、设计或计划发生变化，建议不要直接口头修改，而是按流程处理：

1. 先写变更请求
2. 说明变更原因
3. 说明影响范围
4. 更新相关 Spec
5. 更新相关 Design
6. 更新相关 Plan
7. 记录日志
8. 重新验证

相关文件包括：

- `specs/change-requests/CHANGE_REQUEST_TEMPLATE.md`
- `logs/spec-changes.log`
- `logs/decision-log.md`

---

## 如何恢复中断任务

如果任务执行到一半被打断，建议先查看：

1. `specs/SDD_BREAKPOINT.md`
2. `specs/CONTEXT_SUMMARY.md`
3. `logs/task-execution.log`
4. `logs/decision-log.md`

恢复时的目标是：

- 找回当前状态
- 找回已确认决策
- 找回未完成事项
- 继续执行，而不是重复开始

---

## 示例项目

仓库提供了一个完整的示例项目：

- `examples/sample-project/`

该示例以“用户登录”为场景，展示完整闭环：

- 项目画像
- Product Spec
- Design Doc
- Exec Plan
- Validation Report
- Archive Summary

如果你是第一次使用这套框架，建议先看示例项目，再开始自己的项目。

---

## 维护原则

### 1. 规则优先

如果习惯和规则冲突，优先遵守仓库规则。

### 2. 需求优先

任何实现都应能追溯到需求。

### 3. 设计优先

不要跳过设计直接写实现。

### 4. 计划优先

大任务必须拆解，避免盲目推进。

### 5. 验证优先

“能跑”不等于“正确”。

### 6. 归档优先

交付结束后要沉淀结果，形成闭环。

---

## 相关文档

建议优先阅读以下文件：

- `AGENTS.md`
- `docs/repository-index.md`
- `docs/quick-start.md`
- `docs/methodology.md`
- `docs/command-reference.md`

---

## 一句话总结

这套框架可以理解为：

- `README.md`：入口
- `AGENTS.md`：总宪法
- `project/`：项目身份
- `rules/`：制度
- `skills/`：动作
- `specs/`：中枢
- `logs/`：证据
- `archives/`：收口
- `examples/`：教学

---

## 结束语

这不是一个只给人看的仓库，也不是一个只给 AI 用的仓库，  
而是一套让 **需求、设计、执行、验证、归档** 形成闭环的协作框架。