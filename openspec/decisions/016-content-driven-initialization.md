# ADR-016: 内容驱动初始化与结构极简重构 (Content-Driven Initialization and Physical Cleanup)

## Status
Accepted

## Context
目前的 `foundry-initializing` 技能仅负责物理建档，导致生成的全局标准（`global_standard.md`）和协议模板（`schemas/`）内容缺失（空文件），使用户在冷启动阶段产生困惑。此外，原有的 `meta/` 和 `common/` 嵌套目录在扁平化决策后已失去实用价值，成为阻碍 CLI 识别技能的冗余实体。

## Decision
1. **内容驱动初始化**：升级 `foundry-initializing` 职责，从“创建空文件”变更为“注入预置模板”。初始化时必须同步注入母库当前最新的全局规约与协议内容。
2. **物理去冗余**：彻底废弃并清理 `.gemini/skills/` 下的 `meta/` 和 `common/` 等嵌套物理目录，强制执行扁平化架构以确保所有技能 100% 可被 CLI 识别。
3. **自主演进闭环**：母库自身的核心文件即为分发给用户的“活模板”，确保用户在初始化后能立即继承 SOP 2.0 的最高生产力标准。

## Consequences
- **好处**：消除了“鸡生蛋”的冷启动困境；实现了母库规约的“开箱即用”；保持了项目结构的极致简洁与高可见性。
- **约束**：初始化动作现在涉及更多的物理写入；开发者在母库维护 Schema 时需意识到它们同时具有模板属性。

## Related Sub-Project
N/A (SOP 2.0 Core Initialization Refinement)
