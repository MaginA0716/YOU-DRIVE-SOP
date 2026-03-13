## Context

目前，AI 在进入本仓库后主要通过 `GETTING_STARTED.md` 了解基础操作，但缺乏对核心治理规约（SOP 2.0）的自动对齐。我们需要通过物理文件锚点实现 AI 的“开机自检”。

## Goals / Non-Goals

**Goals:**
- 实现 AI 进入项目后的“零成本”规约对齐。
- 在 `GEMINI.md` 中注入强制性的自检指令。
- 在 `foundry-initializing` 技能中建立与治理手册的物理链接。

**Non-Goals:**
- 不修改 Gemini CLI 的底层逻辑。
- 不强制要求用户安装除 `gh` 以外的新工具。

## Decisions

- **Decision 1: 使用 `GEMINI.md` 作为 Context Header**
  - **Rationale**: Gemini CLI 会自动读取根目录下的 `GEMINI.md`。将其作为 AI 的“启动指令集”是最直接且低侵入性的方式。
- **Decision 2: 物理手册探测逻辑**
  - **Rationale**: 在 `foundry-initializing` 技能中加入 `Step 4`，通过 `read_file` 探测 `SOP_CORE_MANUAL.md`。这确保了初始化后的“智力链条”不中断。

## Risks / Trade-offs

- **Risk**: AI 可能忽略 `GEMINI.md` 中的强制指令。
  - **Mitigation**: 在 `GETTING_STARTED.md` 顶部增加显式引导，并使用“强制执行 (Mandatory)”等高亮词汇增强意图。
