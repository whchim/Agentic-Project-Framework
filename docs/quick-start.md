# 快速开始

## 第一步：看总规则
先读：
- `AGENTS.md`
- `project/project-profile.yaml`
- `project/tech-stack.yaml`
- `project/constraints.yaml`

## 第二步：选模式
在 `project/project-profile.yaml` 里确认：
- lite
- standard
- strict

## 第三步：初始化需求
执行：
- `/sdd-init`

然后生成 Product Spec 草稿。

## 第四步：澄清需求
执行：
- `/sdd-brainstorm`

把目标、范围、验收标准问清楚。

## 第五步：设计
执行：
- `/sdd-design`

基于锁定后的 Spec 输出 Design Doc。

## 第六步：拆计划
执行：
- `/sdd-plan`

把设计拆成一个个小任务。

## 第七步：执行
执行：
- `/sdd-exec`

必要时先开独立分支或 worktree。

## 第八步：验证
执行：
- `/sdd-test`
- `/sdd-validate`

确认代码和 Spec 一致。

## 第九步：归档
执行：
- `/sdd-archive`

## 小白建议
第一次用时，不要急着写代码，先把需求和设计文档看懂。