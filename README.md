# Luminolex Hand-drawn Notes Skill

Version: 1.0.0

A reusable Skill for turning long-form management, coaching, HR, leadership, research, podcast, and training content into a consistent Luminolex visual-content pipeline.

## Repository contents

- `SKILL.md` — main orchestration instructions
- `visual-style.md` — locked visual identity
- `decomposition-rules.md` — semantic decomposition and visual translation
- `prompt-template.md` — per-image prompt template
- `fish-rules.md` — Fish narration rules
- `anchor-rules.md` — semantic-anchor rules
- `publish-rules.md` — Douyin / Xiaohongshu publishing rules
- `examples/icf-example.md` — example decomposition

## Recommended usage

- “按 luminolex-handdrawn-notes 处理这篇文章，DRAW 模式。”
- “基于最终图片顺序输出 FISH。”
- “基于最终 Fish 稿输出 20 条 ANCHOR。”
- “输出 PUBLISH 版本。”

## Direct Skill file

Use the root `SKILL.md` as the main entry point.

## Feishu / external agent installation

If your agent supports installing Skills from a public GitHub repository, use:

`https://github.com/2025dba-code/luminolex-handdrawn-notes`

If it requires a direct raw Skill file, use:

`https://raw.githubusercontent.com/2025dba-code/luminolex-handdrawn-notes/main/SKILL.md`
