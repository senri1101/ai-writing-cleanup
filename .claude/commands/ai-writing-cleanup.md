---
argument-hint: "[draft text or file path]"
description: Clean Japanese or English prose so it reads less stereotypically AI-written
---

Use the `ai-writing-cleanup` rules in this repository to revise prose so it reads naturally and does not sound stereotypically AI-written.

Read these references before editing:
- @SKILL.md
- @references/checklists.md
- @references/ja.md
- @references/en.md

Task:
- Detect whether the draft is primarily Japanese or English.
- Apply the matching language rules plus the shared checklist.
- Preserve factual meaning, Markdown structure, citations, and technical terms.
- Remove AI-signaling patterns such as inflated significance, repetitive transitions, trailing interpretation after facts, roundabout copula phrasing, forced triads, formulaic intros and outros, dash theatrics, chatbot residue, vague sourcing, and excessive hedging.
- Keep human specificity when the genre allows it.
- Return only the revised draft unless the user explicitly asks for commentary.

Input handling:
- If `$ARGUMENTS` contains prose, revise that prose directly.
- If `$ARGUMENTS` looks like a file path, read that file and revise the prose from it.
- If no arguments are supplied, operate on the draft the user pasted in the current conversation.
