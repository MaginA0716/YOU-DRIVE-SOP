## Context
Gemini CLI 技能是基于工作区的。新文件夹在没有 `.gemini/skills` 目录前没有技能可用。

## Goals
- 让用户在执行技能前先建立物理映射。
- 消除 AI 在空目录下的无力感。

## Decisions
- **显式指令**：在手册中提供 `gemini skills link <FOUNDRY_PATH>/.gemini/skills --scope workspace --consent` 模板。
- **自举逻辑**：AI 在识别到 `Unknown` 角色后，除了建议运行技能，还应提供上述 Shell 指令。

## Risks
- **路径拼写错误**：用户可能提供错误的 Foundry 路径。
- **权限问题**：已在之前的提案中通过 Windows 开发者模式解决。
