## 1. 规约与环境自检 (Mandatory Setup)
- [x] 1.1 确认当前分支为 `issue-031-architecture-awareness`
- [x] 1.2 确认 `.gemini/ops_changelog.md` 审计表格已更新
- [x] 1.3 执行 `activate_skill verification-before-completion` 预载验证逻辑

## 2. 技能加固 (Awareness Injection)
- [x] 2.1 修改 `using-superpowers` 技能，在 `Initialization Check` 章节增加对 [Foundry/Workshop] 的识别逻辑。
- [x] 2.2 要求 AI 在检测成功后显式报告架构对齐度。
- [x] 2.3 **Validation**: 在母库环境下运行自检，检查是否正确报告“Foundry”。

## 3. 过程合规性校验
- [x] 3.1 确认所有写操作均有审计记录
- [x] 3.2 归档并完成路线图
