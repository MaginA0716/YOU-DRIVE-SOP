## Why
子库（Workshop）初始化在 Windows 环境下经常因权限不足（Error 5）导致物理链路（Junction）创建失败，且路径探测逻辑脆弱，容易导致母库“失联”。

## What Changes
- **权限预检**：在创建链接前执行 Windows 权限探测，并提供清晰的报错引导。
- **绝对路径强制化**：确保 `link.json` 中存储的是绝对路径，消除相对路径带来的引用歧义。
- **链路自愈增强**：优化 `workshop-initializing` 中的链路重建逻辑。

## Capabilities
- `workshop-link-recovery`: 实现物理链路的自动感应与自愈。

## Impact
- 修改 `workshop-initializing` 技能。
- 修改子库 `link.json` 的生成标准。
