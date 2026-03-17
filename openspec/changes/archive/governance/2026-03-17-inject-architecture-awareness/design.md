## Context
目前的 `using-superpowers` 仅检查初始化文件是否存在，但不要求 AI 显式向用户报告其识别结果。

## Goals
- 实现 AI 对工作区角色的自动识别并报告。

## Decisions
- **指纹识别逻辑**：
    - 存在 `.gemini/global_standard.md` 且无 `link.json` -> **Foundry**。
    - 存在 `link.json` -> **Workshop**。
    - 均不存在 -> **Unknown**。

## Risks
- **[Risk]** 路径探测错误导致误判 -> **[Mitigation]** 优先以物理文件存在为准。
