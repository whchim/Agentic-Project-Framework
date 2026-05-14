# 测试规范

## 测试类型
- Unit Test
- Integration Test
- E2E Test
- Regression Test
- Security Test

## 基本要求
- 新增功能必须有测试
- 修复缺陷必须补回归测试
- 核心模块覆盖率 >= 80%
- 关键路径必须有集成测试
- 复杂逻辑优先测试驱动

## TDD 建议
对于核心逻辑：
1. 先写失败测试
2. 再写最小实现
3. 再重构
4. 再补边界测试

## 测试命名
- Python: `test_*.py`
- JS/TS: `*.test.ts` / `*.spec.ts`

## 禁止事项
- 用“我觉得能用”代替测试
- 没有回归测试就修 bug
- 测试和实现脱节