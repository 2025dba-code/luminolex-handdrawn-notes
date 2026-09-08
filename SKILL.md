---
name: luminolex-handdrawn-notes
description: >
  Convert long-form management, coaching, HR, leadership, research, podcast,
  and training content into a complete set of Luminolex-style hand-drawn
  business illustration prompts. Supports DRAW, FISH, ANCHOR, and PUBLISH modes.
version: 1.0.0
language: zh-CN
---

# Luminolex Hand-drawn Notes Skill

## 1. Purpose

This Skill converts source material into a reusable visual-content production system:

Source material
→ semantic understanding
→ knowledge decomposition
→ visual-node planning
→ Luminolex hand-drawn prompts
→ optional Fish narration
→ optional semantic anchors
→ optional social publishing copy

The Skill is designed for:
- ICF coaching course materials
- HBR / management articles
- podcasts and transcripts
- HR policies and frameworks
- leadership / performance / organization content
- training manuals
- long-form research or professional learning materials

The Skill must NOT mechanically generate one image per paragraph.
The Skill must first understand the source, identify the conceptual structure,
and only then decide what needs to be visualized.

# 2. Trigger conditions

Activate this Skill when the user asks for language similar to:
- “按之前相同风格生成手绘图 Prompt”
- “整理成手绘笔记”
- “根据这篇文章生成绘画提示词”
- “这个章节很长，根据需要绘制，不限20张”
- “输出 Fish 旁白”
- “输出语义锚点”
- “输出抖音/小红书标题、内容和关键词”

If the user explicitly asks for 国际版 / 英文版 / international / English version,
switch to the international visual-language rules.
Otherwise always use the Chinese Luminolex visual mode.

# 3. Modes

## DRAW
Default mode. Read the complete source and generate a complete sequence of illustration prompts.

## FISH
Generate Fish-ready narration based on the final visual sequence and source content.

## ANCHOR
Generate semantic anchors based on the FINAL Fish narration.

## PUBLISH
Generate social publishing copy for Douyin / Xiaohongshu.

A user may request one mode or multiple modes.

# 4. Core principle

## Understand first. Draw second.

Never start by mapping paragraphs directly to images.

First identify:
1. Core thesis
2. Primary sections
3. Secondary concepts
4. Frameworks / models
5. Contrasts
6. Causes and effects
7. Risks / failure modes
8. Correct practices
9. Cases / examples
10. Key questions
11. Learning points
12. Final synthesis

Then decide the image sequence.

# 5. Image-count rule

Image count is determined by conceptual completeness, NOT by a fixed quota.

Suggested range:
- Short article / podcast: 12–20 images
- Medium chapter: 20–30 images
- Complex training chapter: 30–45 images
- Large textbook chapter: 40–60 images

The question is:

> If this image is removed, will an important concept, example, model, risk,
> distinction, or action disappear from the visual explanation?

If yes, keep the image.
Do not force a long chapter into 20 images.

# 6. Default narrative architecture

When applicable, structure the visual sequence as:
1. Opening tension / misconception
2. Core concept
3. Why it matters
4. Underlying mechanism
5. Common failure modes
6. Cases / examples
7. Correct professional behavior
8. Practical method / tool
9. Advanced-level distinction
10. Summary / synthesis

For professional competency chapters, also consider:
- Definition
- Boundary
- Positive behavior
- Disqualifying behavior
- Assessment criteria
- Common mistakes
- Correction method
- Level progression
- Learning points

# 7. Mandatory visual style

Read and obey `visual-style.md`.
Do not rewrite or dilute the visual style unless the user explicitly asks.

# 8. Visual translation rules

Read and obey `decomposition-rules.md`.

Core rule:
Never let 3 or more consecutive images become generic “two people sitting and talking”
unless the source itself requires it.

Convert abstract ideas into spatial metaphors, paths, boundaries, maps,
bridges, light, layers, scales, mirrors, compasses, roots, or other meaningful
editorial-business visual devices.

# 9. Per-image output structure

Each image prompt should normally contain:

## 图XX｜短标题
1. Scene
2. Character(s)
3. Character action / posture
4. Key objects
5. Visual metaphor
6. Spatial relationship
7. Highlight color usage
8. Core Chinese phrase
9. Intended meaning
10. Global style reminder when useful

Use natural prose rather than JSON unless the user explicitly asks for structured data.

# 10. Coverage rules

Before finalizing DRAW output, verify:
- [ ] Every major section is represented
- [ ] Every critical model is visualized
- [ ] Important cases are represented
- [ ] Failure modes are represented
- [ ] Correct practices are represented
- [ ] Boundaries / risks are represented where relevant
- [ ] Final learning points are represented
- [ ] There is at least one synthesis / final image
- [ ] No major source concept is silently dropped
- [ ] Image sequence follows a coherent learning journey

If the chapter is long, increase the number of images instead of compressing
multiple unrelated concepts into one frame.

# 11. Source fidelity

When source files are provided:
- Preserve source terminology and logic.
- Do not silently replace the source framework with general knowledge.
- Do not invent assessment criteria that are not in the source.
- Distinguish source-derived content from model-added explanatory framing.
- When needed, say that a specific point is an interpretation rather than source text.

# 12. Fish workflow

If the user requests Fish narration:
1. Use the source + final image sequence.
2. Do NOT narrate “图1、图2”.
3. Build one continuous argument.
4. Keep sentence length short.
5. Use natural spoken Mandarin.
6. Avoid repetitive rhetorical filler.
7. Keep total text within 15,000 Chinese characters.
8. Preferred working range: 5,000–8,000 Chinese characters for a 20-image longform episode.
9. Preserve the important visual transitions so anchors can be distributed evenly.

Read `fish-rules.md`.

# 13. Anchor workflow

Semantic anchors MUST be generated from the FINAL Fish text, not from an earlier draft.

Format:

# 章节标题

语义锚点 || 关键词1,关键词2,关键词3

Rules:
- Section headings start with `#`
- Headings do NOT count as anchors
- For a 20-image production, output exactly 20 anchor lines
- Anchors must follow narration chronology
- Prefer phrases actually present in final narration
- Avoid long phrases likely to cross Whisper segments
- Avoid generic words that may repeat
- Distribute anchors across the full duration
- Keywords describe the visual meaning, not merely repeat anchor text

Read `anchor-rules.md`.

# 14. Publishing workflow

When requested, generate:
- Douyin title
- Douyin description
- Douyin hashtags
- Xiaohongshu title
- Xiaohongshu post body
- Xiaohongshu keywords / hashtags
- Cover headline recommendation

Keep cover headline and platform title complementary rather than identical.
Read `publish-rules.md`.

# 15. Quality standard

The output should feel like:
- a premium management book
- a professional coaching manual
- a consulting insight report
- an editorial visual essay

It should NOT feel like:
- children's educational illustration
- cartoon notes
- generic AI clip art
- PowerPoint icon collection
- repetitive meeting-room screenshots

# 16. Final self-check

Before output, silently ask:
1. Did I actually understand the source?
2. Is image count sufficient for the source length?
3. Is each frame built around one core idea?
4. Did I vary scene / metaphor / model / process?
5. Do the images form a coherent narrative?
6. Did I preserve the Luminolex visual identity?
7. If Fish is requested, does it sound spoken rather than written?
8. If anchors are requested, are they generated from the final Fish draft?
9. Does the final set preserve the user's requested language mode?
10. Is the output production-ready?

If not, revise before returning.
