## Why
AI 在处理任务前如果缺乏对自己所处物理环境（母库还是子库）的清晰认知，容易导致错误的规约执行。我们需要在 AI 的“开机序列”中注入架构感知能力。

## What Changes
- **架构自检仪式**：修改 `using-superpowers` 技能，强制 AI 在欢迎语或首次处理前报告架构状态。
- **状态分级**：定义三种状态：`Foundry (母库)`、`Workshop (子库)`、`Unknown (未初始化)`。

## Capabilities
- `ai-spatial-awareness`: 使 AI 能够通过物理文件指纹识别当前架构角色。

## Impact
- 修改 `using-superpowers` 技能。
