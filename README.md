# ai-writing-cleanup

`ai-writing-cleanup` is a bilingual skill and prompt pack for reducing recognizable AI-writing patterns in Japanese and English. The source of truth lives in this repository so the same editorial logic can be used in Codex and adapted to Copilot, Gemini, or Claude Code.

## What It Does

- Detects whether a draft is primarily Japanese or English.
- Removes common AI-writing signals without changing factual meaning.
- Preserves Markdown structure, citations, and technical terminology.
- Pushes the editor toward deletion, directness, and human specificity instead of novelty for novelty's sake.

## Repository Layout

- [SKILL.md](./SKILL.md)
- [agents/openai.yaml](./agents/openai.yaml)
- [references/checklists.md](./references/checklists.md)
- [references/ja.md](./references/ja.md)
- [references/en.md](./references/en.md)
- [prompts/tool-agnostic.md](./prompts/tool-agnostic.md)

## Use In Codex

Copy or symlink this repository into your Codex skills directory, or point Codex at the skill folder directly.

Typical invocation:

```text
Use $ai-writing-cleanup to revise this draft so it reads naturally in Japanese or English without obvious AI-writing tells.
```

## Use Outside Codex

Open [prompts/tool-agnostic.md](./prompts/tool-agnostic.md) and paste the universal prompt into Copilot, Gemini, Claude Code, or another assistant. The prompt is written so the model edits in place instead of rewriting everything for stylistic novelty.

If the assistant tends to over-explain, append:

```text
Return only the revised draft unless I explicitly ask for commentary.
```

## Maintenance Notes

- Update the pattern list as public AI-writing tells change.
- Prefer examples grounded in real prose, not abstract style advice.
- Add new rules only when they help distinguish useful editing from generic paraphrasing.
