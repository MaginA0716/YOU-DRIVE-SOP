## Why

在初次部署或新 AI 接入时，由于缺乏强制性的上下文引导，AI 引擎往往无法自动识别 `SOP_CORE_MANUAL.md` 等治理文档，导致“智力链条”断裂，用户必须手动下达复杂的引导指令。建立一套“开机即握手”的物理协议势在必行。

## What Changes

- **核心治理手册**：创建 `SOP_CORE_MANUAL.md`，固化四层治理逻辑。
- **AI 登录看板**：创建 `GEMINI.md`，注入强制性的 `Boot Sequence`。
- **初始化挂钩**：在 `foundry-initializing` 技能中增加“AI Context Onboarding”步骤。
- **引导加固**：在 `GETTING_STARTED.md` 顶部增加 AI 自检步骤。

## Capabilities

### New Capabilities
- `ai-onboarding-protocol`: 定义 AI 进入工作区后的物理握手与自检流程。
- `governance-manual`: 建立项目全局治理逻辑的物理参考文档。

### Modified Capabilities
- `foundry-protocols`: 更新初始化流程，加入对治理手册的自动探测与汇报要求。

## Impact

- 影响 `.gemini/skills/foundry-initializing/SKILL.md` 的执行逻辑。
- 影响项目根目录的引导文档结构。
- 提高了所有 AI 代理（Gemini, Claude 等）的初始化对齐速度。
