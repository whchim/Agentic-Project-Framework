# CI/CD 规范

## 基本要求
- 提交后自动跑测试
- 合并前自动做质量检查
- 发布前必须验证版本一致性

## Pipeline 建议
1. 安装依赖
2. lint
3. type check
4. unit test
5. integration test
6. security check
7. build
8. 发布

## 禁止事项
- 没测试就发布
- 没审查就合并
- 没验证就上线