## Why

目前，当新用户进入项目或开启新的 AI 会话时，往往需要手动引导 AI 去对齐规约。这种“非自动”的对齐过程极易导致智力断档，使得 AI 回归到“原始通用模型”的状态，无视本地已沉淀的 SOP。我们需要利用 Gemini CLI 的 native 特性，建立一套“开机即握手”的全自动物理协议。

## What Changes

- **统一入口**：在 `README.md` 顶部增加 AI 登舰区，并创建跨 AI 契约文件 `AGENTS.md`。
- **开机脚本加固**：优化 `GEMINI.md`，使用 `[CRITICAL-BOOT]` 权重标签，强制 AI 在进入目录后立即执行 `SOP_CORE_MANUAL.md` 的分析。
- **智力地图引入**：在 `SOP_CORE_MANUAL.md` 中增加“物理流程全景图”，实现源码、规约与流程的视觉化串联。

## Capabilities

### New Capabilities
- `auto-boot-handshake`: 实现 AI 启动时的零干扰规约对齐。
- `cross-agent-contract`: 确保不同 AI 引擎均能识别本项目为 SOP 驱动。

## Impact

- 彻底消除了“忘了读手册”导致的执行偏差。
- 提升了新用户 fork 后的“即插即用”体验。
- 增强了项目规约的物理存在感。
