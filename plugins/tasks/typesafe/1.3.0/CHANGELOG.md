---
changelogVersion: 1
plugin: "typesafe"
version: "1.3.0"
locale: "en"
translations:
  zh-CN: "CHANGELOG.zh-CN.md"
---
# Changelog

## [1.3.0]

### Added

- Call `Kev-4b`, `SemIf`, and `decision-model-preview` on the System One endpoint. They take the same state, questions, and assets as the Jev models, bill input tokens per million with free output like them, and reserve the same 65,792 or 262,400 input tokens as the other models.

### Migration

- Set a price for `Kev-4b`, `SemIf`, and `decision-model-preview` before offering them, with task usage expression billing like the Jev models. For a model priced at 0.042 USD per 1 million input tokens, the expression is `tier("base", u("input_tokens") * 0.042 / 1000000)`.
