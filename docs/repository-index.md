# Repository Index

> 本文件用于统一说明仓库的目录结构、文件职责、加载顺序、工作流与维护方式。  
> 它是整套框架的“总索引”，适合在进入仓库后优先阅读。
---

## 1. 仓库定位
本仓库是一套面向 **AI + 人类协作** 的项目基础框架，核心目标是：
- 统一需求、设计、执行、验证、归档流程
- 降低沟通成本
- 提升项目可追溯性
- 让 AI 在明确边界内稳定工作
- 让复杂任务可拆分、可恢复、可验证
- 让项目经验可复用、可沉淀
---

## 2. 设计原则

本仓库遵循以下原则：

### 2.1 Spec-first
先写需求，再写设计，再写执行计划，再进入实现。

### 2.2 Evidence-first
所有关键结论尽量有记录、有验证、有证据。

### 2.3 Isolated work
复杂任务优先使用分支或 worktree 隔离，避免相互干扰。

### 2.4 Traceable
需求变更、设计决策、执行过程、验证结果都应可追踪。

### 2.5 Recoverable
任务中断后，应能通过断点和上下文摘要恢复。

### 2.6 Reusable
规则、模板、技能、示例都应可复用到新项目。

---

## 3. 仓库总体结构

```text
agentic-project-framework/
├── README.md
├── AGENTS.md
├── .gitignore
├── .env.example
│
├── docs/
│   ├── methodology.md
│   ├── quick-start.md
│   ├── command-reference.md
│   ├── repository-index.md
│   └── README.md
│
├── project/
│   ├── project-profile.yaml
│   ├── tech-stack.yaml
│   ├── constraints.yaml
│   ├── team-guidelines.md
│   └── architecture-decisions/
│       └── ADR-TEMPLATE.md
│
├── specs/
│   ├── SDD_BREAKPOINT.md
│   ├── CONTEXT_SUMMARY.md
│   ├── product-spec/
│   │   ├── PRODUCT_SPEC_TEMPLATE.md
│   │   └── README.md
│   ├── design-doc/
│   │   ├── DESIGN_DOC_TEMPLATE.md
│   │   └── README.md
│   ├── exec-plan/
│   │   ├── EXEC_PLAN_TEMPLATE.md
│   │   └── README.md
│   └── change-requests/
│       ├── CHANGE_REQUEST_TEMPLATE.md
│       └── .gitkeep
│
├── rules/
│   ├── git-workflow.md
│   ├── code-style-universal.md
│   ├── security-baseline.md
│   ├── testing-guidelines.md
│   ├── quality-gate.md
│   ├── dependency-management.md
│   ├── environment-management.md
│   ├── observability-guidelines.md
│   ├── ci-cd-guidelines.md
│   ├── ai-application-guidelines.md
│   └── code-style-language/
│       ├── python.md
│       ├── javascript.md
│       └── typescript.md
│
├── skills/
│   ├── brainstorm.md
│   ├── spec-writing.md
│   ├── design-review.md
│   ├── plan-writing.md
│   ├── worktree-management.md
│   ├── test-writing.md
│   ├── debugging.md
│   ├── code-review.md
│   ├── breakpoint-management.md
│   └── finishing-branch.md
│
├── logs/
│   ├── task-execution.log
│   ├── spec-changes.log
│   ├── validation.log
│   └── decision-log.md
│
├── archives/
│   └── .gitkeep
│
└── examples/
    ├── README.md
    ├── sample-project/
    │   ├── README.md
    │   ├── project-profile.yaml
    │   ├── product-spec.md
    │   ├── design-doc.md
    │   ├── exec-plan.md
    │   ├── validation-report.md
    │   └── archive-summary.md
    └── sample-change-request/
        └── change-request.md
```
---

## 4. 最终版完整仓库内容索引
下面按目录层级说明每个文件的职责。

### 4.1 根目录入口层
#### **README.md**
仓库面向人类用户的总入口。

主要用途：

- 说明仓库是什么
- 说明适用场景
- 说明推荐工作流
- 提供快速开始入口
- 引导用户进入其他文档
#### **AGENTS_CORE.md**
仓库面向 Agent 的总契约。

主要用途：

- 定义最高优先级规则
- 定义文档状态机
- 定义知识加载策略
- 定义任务边界
- 定义执行约束
- 定义标准交互模式
#### **.gitignore**
忽略本地临时文件、构建产物、缓存、日志、环境文件等。

#### **.env.example**
环境变量样例文件，用于说明项目运行时需要哪些配置。

### 4.2 docs/ 文档说明层
docs/ 用于存放说明性文档，主要面向阅读和理解。

#### **docs/methodology.md**
方法论说明文档，用于解释：

 - 这套框架为什么存在
 - 它的解决什么问题
 - 它的设计原则是什么
 - 它适合什么类型的项目
#### **docs/quick-start.md**
快速开始文档，用于帮助新用户快速理解并使用框架。
#### **docs/command-reference.md**
命令参考文档，列出工作流入口、触发词、常用指令或执行步骤。
#### **docs/repository-index.md**
仓库索引文档，本文件本身，用于说明：
- 仓库结构
- 目录职责
- 文件关系
- 加载顺序
- 工作流
- 维护策略
#### **docs/README.md**
docs/ 目录入口页，用于快速导航到各说明文档。

### 4.3 project/ 项目配置层
project/ 用于存放当前项目的专属配置和约束。

#### **project/project-profile.yaml**
项目画像文件，描述：

- 项目名称
- 项目描述
- 所属团队
- 工作模式
- 生命周期
- 协作方式
#### **project/tech-stack.yaml**
技术栈声明文件，描述：

- 编程语言
- 框架
- 数据库
- 缓存
- 部署方式
- AI 相关组件
#### **project/constraints.yaml**
项目约束文件，定义：

- 性能要求
- 安全底线
- 技术边界
- 团队约束
- 流程限制
#### **project/team-guidelines.md**
团队协作规范，定义：

- 提交习惯
- 评审要求
- 沟通规则
- 冲突处理
- 收尾标准
#### **project/architecture-decisions/ADR-TEMPLATE.md**
架构决策记录模板，用于记录关键技术选型、决策原因和权衡结果。

### 4.4 specs/ 需求与执行中枢层
specs/ 是仓库的核心中枢，承载需求、设计、执行、上下文和变更。

#### **specs/product-spec/PRODUCT_SPEC_TEMPLATE.md**
Product Spec 模板，用于描述：

- 问题定义
- 业务目标
- 用户目标
- 范围
- 验收标准
- 风险
- 风险未决问题
#### **specs/product-spec/README.md**
Product Spec 编写说明。

#### **specs/design-doc/DESIGN_DOC_TEMPLATE.md**
Design Doc 模板，用于描述：

- 总体方案
- 模块拆分
- 数据模型
- API 设计
- 安全设计
- 怂常处理
- 风险与权衡
#### **specs/design-doc/README.md**
Design Doc 编写说明。

#### **specs/exec-plan/EXEC_PLAN_TEMPLATE.md**
Exec Plan 模板，用于描述：

- 前置条件
- 任务拆解
- 执行顺序
- 验收标准
- 回滚方案
#### **specs/exec-plan/README.md**
Exec Plan 编写说明。

#### **specs/SDD_BREAKPOINT.md**
断点文件，用于保存任务中断时的状态、上下文和下一步动作。

#### **specs/CONTEXT_SUMMARY.md**
上下文摘要文件，用于记录当前目标、已确认内容、阻塞项和恢复指引。

#### **specs/change-requests/CHANGE_REQUEST_TEMPLATE.md** 
变更申请模板，用于修改已锁定的需求、设计或执行内容。

#### **specs/change-requests/.gitkeep**
占位文件，用于保持目录存在于版本控制中。

### 4.5 rules/ 治理层
rules/ 定义长期稳定的规则、边界和质量标准。

#### **rules/git-workflow.md**
Git 工作流规范，包括：

- 分支策略：主分支、功能分支、发布分支等
- 提交规范
- PR  流程
- worktree 使用建议
#### **rules/code-style-universal.md**
通用代码风格规范，适用于所有语言。

#### **rules/security-baseline.md**
安全基线规范，定义：

- 输入参数校验
- 敏感信息处理
- 密钥管理
- 鉴权原则
- Web 安全
- AI 应用安全
#### **rules/testing-guidelines.md**
测试规范，定义：

- 测试层级
- TDD 原则
- 核心逻辑覆盖
- 测试边界
- 禁止事项
#### **rules/quality-gate.md**
质量门禁规则，定义：

- 合并前必须满足的检查项
- 验证标准
- 归档门槛
#### **rules/dependency-management.md**
依赖管理规范，定义：

- 新增依赖原则
- 升级策略
- 审查要求
- 风险控制
#### **rules/environment-management.md**
环境管理规范，定义：

- .env 处理
- 本地/测试/生产隔离
- 秘钥处理
- 配置回收原则
#### **rules/observability-guidelines.md**
可观测性规范，定义：

- 日志
- 指标
- 链路追踪
- 告警
- 事件记录
#### **rules/ci-cd-guidelines.md**
CI/CD 规范，定义：

- 流水线结构
- 质量门禁
- 自动化检查
- 发布建议
#### **rules/ai-application-guidelines.md**
AI 应用规范，定义：

- Prompt 设计
- 模型调用边界
- RAG 使用
- 安全脱敏
- 评测原则
#### **rules/code-style-language/python.md**
Python 语言专属风格规范。

#### **rules/code-style-language/javascript.md**
JavaScript 语言专属风格规范。

#### **rules/code-style-language/typescript.md**
TypeScript 语言专属风格规范。

### 4.6 skills/ 执行动作层
skills/ 用于定义不同场景下的执行方式，便于 AI 或团队成员按步骤工作。

#### **skills/brainstorm.md**
需求澄清、问题拆解、方案发散技能。

#### **skills/spec-writing.md**
需求文档编写技能。

#### **skills/design-review.md**
设计评审技能。

#### **skills/plan-writing.md**
执行计划编写技能。

#### **skills/worktree-management.md**
worktree 隔离管理技能，用于复杂任务并行和风险隔离。

#### **skills/test-writing.md**
测试编写技能，强调核心逻辑测试和 TDD。

#### **skills/debugging.md**
调试技能，强调系统化定位与复现。

#### **skills/code-review.md**
代码审查技能。

#### **skills/breakpoint-management.md**
断点管理技能，用于中断保存与恢复。

#### **skills/finishing-branch.md**
任务收尾技能，用于测试确认、清理、合并和归档前检查。

### 4.7 logs/ 记录层
logs/ 用于保留执行证据和过程记录。

#### **logs/task-execution.log**
记录任务执行过程。

#### **logs/spec-changes.log**
记录需求变更过程。

#### **logs/validation.log**
记录验证结果。

#### **logs/decision-log.md**
记录关键决策、理由和结论。

### 4.8 archives/ 归档层
archives/ 用于存放最终交付后的归档内容。

#### **archives/.gitkeep**
占位文件，用于保持目录存在。

典型归档内容包括：

- Product Spec
- Design Doc
- Exec Plan
- Test Report
- Validation Report
- Release Summary
- Lessons Learned
归档的原则是：尽量稳定，尽量少改，便于回溯。

### 4.9 examples/ 示例层
examples/ 用于提供示例项目和变更请求样例，帮助新用户快速理解整套框架。

#### **examples/README.md**
示例区说明页。

#### **examples/sample-project/**
完整生命周期示例项目，用于演示从需求到归档的全过程。

其文件包括：

- README.md
- project-profile.yaml
- product-spec.md
- design-doc.md
- exec-plan.md
- validation-report.md
- archive-summary.md

#### **examples/sample-change-request/change-request.md**

变更请求示例，用于演示如何提交需求变更。

---

## 5. 文件加载顺序
下面是推荐的阅读顺序。

### 5.1 第一次进入仓库
建议按以下顺序阅读：

 1. README.md
 2. AGENTS.md
 3. docs/README.md
 4. docs/repository-index.md
 5. docs/quick-start.md
 6. project/project-profile.yaml
 7. project/constraints.yaml
 8. rules/security-baseline.md
 9. rules/testing-guidelines.md
 10. rules/quality-gate.md

### 5.2 开始一个新需求
建议按以下顺序读取：

 1. skills/brainstorm.md
 2. specs/product-spec/PRODUCT_SPEC_TEMPLATE.md
 3. specs/design-doc/DESIGN_DOC_TEMPLATE.md
 4. specs/exec-plan/EXEC_PLAN_TEMPLATE.md
 5. skills/worktree-management.md
 6. skills/test-writing.md
 7. skills/finishing-branch.md

### 5.3 任务中断后恢复
建议按以下顺序读取：

 1. specs/SDD_BREAKPOINT.md
 2. specs/CONTEXT_SUMMARY.md
 3. logs/task-execution.log
 4. logs/decision-log.md
---

## 6. 标准工作流
这套框架推荐的标准闭环如下：

```mermaid
graph LR
    A[需求提出] --> B[brainstorm]
    B --> C[Product Spec]
    C --> D[Spec Review]
    D --> E[Design Doc]
    E --> F[Design Review]
    F --> G[Exec Plan]
    G --> H[执行开发]
    H --> I[测试验证]
    I --> J[质量门禁]
    J --> K[归档]
```

### 6.1 需求提出
明确问题、目标、范围和背景。

### 6.2 brainstorm
先澄清，再发散，识别风险和未决项。

### 6.3 Product Spec
将需求写清楚，定义目标、范围、非目标和验收标准。

### 6.4 Spec Review
确认需求是否合理、完整、可验收。

### 6.5 Design Doc
把需求转成可执行设计，明确模块、接口、数据、风险和权衡。

### 6.6 Design Review
确认设计可落地，且与需求一致。

### 6.7 Exec Plan
把设计拆解成任务，明确依赖、顺序、验收和回滚策略。

### 6.8 执行开发
按照计划逐步落地实现。

### 6.9 测试验证
验证功能、边界、异常、安全和可观测性。

### 6.10 质量门禁
确认是否满足合并和归档条件。

### 6.11 归档
保留最终结果，形成可追溯闭环。
---

## 7. 目录之间的关系
### 7.1 README.md 与 AGENTS_CORE.md
- README.md 面向人类
- AGENTS.md 面向 Agent

### 7.2 AGENTS.md 与 rules/
- AGENTS.md 定义总原则
- rules/ 提供具体执行标准

### 7.3 rules/ 与 skills/
- rules/ 定义边界和底线
- skills/ 定义执行动作和流程

### 7.4 skills/ 与 specs/
- skills/ 负责生成、评审、执行和恢复
- specs/ 负责承载需求、设计、计划、上下文和变更

### 7.5 specs/ 与 logs/
- specs/ 是目标和过程
- logs/ 是证据和记录

### 7.6 logs/ 与 archives/
- logs/ 是过程留痕
- archives/ 是最终收口结果

### 7.7 examples/ 与正式目录
- examples/ 用于教学和参考
- 正式目录用于真实项目运行  
---

## 8. 推荐使用场景
### 8.1 新项目初始化
适合先看：

 1. README.md
 2. AGENTS.md
 3. docs/quick-start.md
 4. docs/repository-index.md
 5. project/project-profile.yaml
 6. examples/sample-project/

### 8.2 新增需求
建议流程：

 1. 需求澄清
 2. 写 Product Spec
 3. 评审 Spec
 4. 写 Design Doc
 5. 评审 Design
 6. 写 Exec Plan
 7. 执行开发
 8. 测试验证
 9. 归档

### 8.3 中途改需求
建议先写变更请求，再同步更新：

 1. specs/change-requests/CHANGE_REQUEST_TEMPLATE.md
 2. specs/product-spec/
 3. specs/design-doc/
 4. specs/exec-plan/
 5. logs/spec-changes.log
 6. logs/decision-log.md

### 8.4 任务中断恢复
先看：

 1. specs/SDD_BREAKPOINT.md
 2. specs/CONTEXT_SUMMARY.md
 3. logs/task-execution.log
 4. logs/decision-log.md

### 8.5 做代码审查
建议结合：

- rules/code-style-universal.md
- rules/security-baseline.md
- rules/testing-guidelines.md
- rules/quality-gate.md
- skills/code-review.md
---

## 9. 维护优先级
如果后续要修改仓库，建议按以下优先级处理：

第一优先级
- AGENTS.md
- project/constraints.yaml
- rules/security-baseline.md
- rules/quality-gate.md
第二优先级
- specs/*
- skills/*
- skills/code-review.md
- rules/testing-guidelines.md
第三优先级
- docs/*
- examples/*
- logs/*
- archives/*
---

## 10. sample-project 示例说明
examples/sample-project/ 是一个完整生命周期示例，用于演示一个典型的功能从需求到归档的全过程。

### 10.1 示例场景
示例场景为：

用户登录功能

### 10.2 包含文件
该示例包含：

- README.md
- project-profile.yaml
- product-spec.md
- design-doc.md
- exec-plan.md
- validation-report.md
- archive-summary.md
### 10.3 示例价值
它用于展示：

- 需求应该怎么写
- 设计应该怎么承接需求
- 计划如何拆任务
- 验证如何对应需求
- 最终如何归档
### 10.4 教学意义
新用户可以通过它快速理解整套框架的完整闭环。
---

## 11. 一句话总结
这个仓库可以理解为：

 - README.md：入口
 - AGENTS.md：总宪法
 - project/：项目身份
 - rules/：制度
 - skills/：动作
 - specs/：中枢
 - logs/：证据
 - archives/：收口
 - examples/：教学
---

## 12. 使用建议
如果你是第一次进入这套框架，建议按以下顺序开始：

 1. 读 README.md
 2. 读 AGENTS.md
 3. 读 docs/README.md
 4. 读 docs/quick-start.md
 5. 看 examples/sample-project/
 6. 再开始自己的项目需求
---

## 13. 结束语
本文件是仓库的总索引。
如果后续仓库结构发生变化，建议优先同步更新本文件，以保持整个框架的可读性和一致性。

