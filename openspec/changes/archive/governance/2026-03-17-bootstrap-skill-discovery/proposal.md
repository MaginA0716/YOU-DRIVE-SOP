## Why
子库（Workshop）初始化时存在“先有鸡还是先有蛋”的问题：`workshop-initializing` 技能物理存放于母库中，在建立物理链路前，子库 AI 无法感知并激活该技能。目前的手册跳过了物理链接这一关键步骤。

## What Changes
- **新增物理链接步**：在 `GETTING_STARTED.md` 中明确增加 `gemini skills link` 的 Shell 指令作为子库初始化的“第 3.5 步”。
- **强化自举引导**：更新 `AGENTS.md` 和 `GEMINI.md`，告知 AI 在发现技能库缺失时主动引导用户运行物理链接指令。

## Capabilities
- `foundry-bootstrap-link`: 明确母库资产分发至子库的物理自举路径。

## Impact
- 重构 `GETTING_STARTED.md` 的子库路径。
- 修改 `AGENTS.md` 的启动序列。
