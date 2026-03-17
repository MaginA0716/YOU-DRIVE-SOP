## Context
Windows 系统在非开发人员模式下限制普通用户创建符号链接/联接点。目前的 `workshop-initializing` 缺乏对该错误的物理拦截。

## Goals
- 提供可靠的 Windows 权限报错拦截。
- 确保子库与母库的物理连接是刚性的（绝对路径）。

## Decisions
- **New-Item Junction**: 使用 PowerShell 的原生指令，并捕获特定的 `UnauthorizedAccessException`。
- **Path Resolve**: 在写入 `link.json` 前执行 `Resolve-Path -Path ...`。

## Risks
- **[Risk]** 权限提升失败 -> **[Mitigation]** 引导用户开启 Windows 开发者模式。
