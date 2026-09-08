# Semantic Anchor Rules

## Standard format

# 章节标题

语义锚点 || 关键词1,关键词2,关键词3

## Parsing rule

- Lines starting with `#` are section headings
- Empty lines are ignored
- Only lines containing `||` are effective anchors
- Headings do NOT count toward anchor count

For a 20-image production:
- exactly 20 effective anchor lines

The production parser should count only `||` lines.

## Anchor selection

Anchors must:
- appear in the FINAL Fish narration
- follow narration chronology
- be distributed across the whole duration
- be semantically unique
- be short enough to avoid Whisper segment-crossing problems
- be long enough to avoid false matches

Good:
“把目标从我要说服你换成我想理解”

Risky (too long):
“成熟有时候意味着你可以尊重一个人同时拒绝这件事而且不破坏关系”

Risky (too generic):
“所以”
“接下来”
“这个问题”
“重要性”

## Whisper stability

Prefer approximately:
- 6–18 Chinese characters when possible
- a distinctive semantic phrase
- no unnecessary punctuation dependence

If an anchor repeatedly fails:
1. confirm Fish audio matches the final script
2. confirm chronology
3. shorten to the distinctive core phrase
4. avoid lowering fuzzy threshold as first response

## Distribution

For 20 anchors, a good structural pattern is:
4 + 4 + 4 + 4 + 4
or another even distribution based on real sections.

Do not place 6–8 anchors inside a tiny final time window.

## Keywords

Keywords describe the visual / semantic function:
- 2–4 terms
- comma-separated
- concise

Example:
`为什么没有人早点告诉我 || 延迟反馈,沉默成本,信任破裂`

## Production parser recommendation

Conceptual logic:

```python
anchors = [
    line.strip()
    for line in text.splitlines()
    if line.strip()
    and not line.strip().startswith("#")
    and "||" in line
]
```

For more robust parsing, preserve headings separately and parse anchors by `||`.
