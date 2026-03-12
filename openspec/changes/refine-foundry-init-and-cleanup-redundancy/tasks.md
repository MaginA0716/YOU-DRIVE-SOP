# Tasks

## 1. 结构化清理 (Physical Cleanup)
- [ ] 物理删除母库根目录下的空冗余目录 `.gemini/skills/meta/` 和 `.gemini/skills/common/`。
- [ ] 检查并移除 `foundry-initializing` 中关于创建上述目录的指令代码。

## 2. 技能内容化重构 (Skill Content Refinement)
- [ ] 对 `D:\code\2026\Base-AI-Driven-Template\.gemini\skills\foundry-initializing\SKILL.md` 进行 Patch。
- [ ] 在 `Workflow` 中明确“内容注入”动作：从内置模板（即母库当前核心文件）同步至目标路径。
- [ ] 更新 `Implementation Workflow`，使其在每一步都描述具体的“注入”细节。

## 3. 规约与标准同步 (Spec & ADR)
- [ ] 将 Delta Spec 合并至母库 `foundry-protocols/spec.md`。
- [ ] 创建 ADR `016-content-driven-initialization.md`。

## 4. 验证与归档 (Archive)
- [ ] 执行全量初始化模拟验证。
- [ ] 执行 `/opsx:archive`。
