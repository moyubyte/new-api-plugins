---
changelogVersion: 1
plugin: "typesafe"
version: "1.3.0"
locale: "zh-CN"
---
# Changelog

## [1.3.0]

### Added

- 支持 `Kev-4b`、`SemIf` 和 `decision-model-preview` 三个模型，调用 System One 接口。它们接受和 Jev 模型相同的 state、questions 和 assets，计费方式也相同：输入按每百万 token 计费，输出免费，并按相同的 65,792 或 262,400 输入 token 预留额度。

### Migration

- 提供 `Kev-4b`、`SemIf` 和 `decision-model-preview` 前，先为它们定价，和其他模型一样使用任务用量表达式计费。例如每 100 万输入 token 0.042 美元的价格，表达式为 `tier("base", u("input_tokens") * 0.042 / 1000000)`。
