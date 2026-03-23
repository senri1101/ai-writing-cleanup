# Portable Prompts

## Universal Prompt

```text
Revise this draft so it reads naturally and does not sound stereotypically AI-written.

Requirements:
- Detect whether the draft is Japanese or English and apply the right cleanup rules.
- Preserve factual meaning, structure, Markdown, and citations.
- Remove AI-writing signals: inflated significance, repetitive transitions, trailing interpretation after facts, roundabout copula phrases, forced triads, formulaic intro/outro, dash theatrics, chatbot residue, vague sourcing, and excessive hedging.
- Keep human specificity when the genre allows it.
- Return only the revised draft unless I ask for commentary.

Draft:
{{TEXT}}
```

## Copilot / Gemini / Claude Code / Codex Adaptation

```text
Act as an editor, not a ghostwriter. Clean the draft in place. Do not paraphrase for variety. Keep what already sounds human.
```

## Optional Follow-Up Prompt

```text
List the 3 most important AI-signaling patterns you removed and quote only the short phrases you changed.
```
