---
name: ai-writing-cleanup
description: Revise AI-generated or AI-assisted prose so it reads less stereotypically LLM-written in Japanese or English. Use when Codex needs to humanize drafts, remove recognizable AI-writing patterns, preserve meaning while improving naturalness, or run a final anti-AI editorial pass on articles, docs, notes, Markdown, or polished prose.
---

# AI Writing Cleanup

## Overview

Reduce recognizable AI-writing patterns without flattening the author's meaning or voice. Detect the draft language first, load the matching reference file, apply the shared cleanup checklist, and only explain the edits when the user asks.

## Workflow

1. Detect whether the draft is primarily Japanese or English.
2. Read [references/checklists.md](references/checklists.md).
3. Read [references/ja.md](references/ja.md) for Japanese drafts or [references/en.md](references/en.md) for English drafts.
4. Preserve factual meaning, emphasis, and structure unless the structure itself is one of the AI-signaling problems.
5. Rewrite line by line where needed instead of paraphrasing the whole piece for novelty.
6. Run the final self-audit before returning the result.

## Language Routing

- Treat mixed-language drafts by cleaning each language in place. Do not force the whole piece into one language.
- Keep domain terminology untouched unless it is itself one of the AI-favored filler phrases.
- Preserve Markdown, headings, lists, code blocks, quotations, and citations.

## Rewrite Rules

- Remove significance inflation. Cut claims like "highlights the importance," "offers important implications," or "注目されます" when the evidence already speaks for itself.
- Remove AI-favored connective padding. Avoid repetitive "additionally," "furthermore," "さらに," and "加えて" when a simple sentence order works.
- Remove trailing interpretation after facts. Replace add-on clauses that explain what the data "underscores" or "suggests" unless the author is explicitly making an argument.
- Prefer direct predicates. Collapse roundabout copula-avoidance such as "serves as," "stands as," "〜として位置づけられています," and "〜の役割を果たしています" when plain phrasing is enough.
- Break forced triads and synonym cycles. Keep only the one noun or adjective that carries the point.
- Remove formulaic openings and endings. Avoid stock intro and outro sentences that sound preloaded.
- Ban em dashes and similar dash theatrics in prose. Replace them with commas, parentheses, sentence breaks, or Japanese punctuation.
- Remove chatbot residue. Delete flattery, compliance language, meta assistant phrasing, and inline-heading bullet patterns like `- Speed: ...`.
- Reduce hedging and vague sourcing. Keep uncertainty only when it is real and attributable.
- Add human specificity where the piece needs it. Prefer concrete observation, opinion, texture, rhythm shifts, and asymmetry over sterile smoothness.

## Output

- Return the cleaned draft first.
- Do not add a change log unless the user asks for one.
- If the user asks for rationale, give only the highest-impact fixes in a short list.
- If a section already reads naturally, leave it alone.
- If the draft is weak because it lacks point of view rather than because of AI tells, say so plainly instead of over-editing.

## Final Self-Audit

- Re-read the introduction and conclusion first. Those are the most likely places for stock AI framing.
- Scan for banned dash usage, inline-heading bullets, and transition-word repetition.
- Ask whether every sentence sounds like someone chose it, not like a model averaged it.
- Keep one or two moments of human texture when the genre allows it. Do not inject fake intimacy into formal writing.
- Stop when the text feels natural. Do not keep polishing into blandness.

## Resources

- Shared checklist and self-audit: [references/checklists.md](references/checklists.md)
- Japanese-specific patterns and examples: [references/ja.md](references/ja.md)
- English-specific patterns and examples: [references/en.md](references/en.md)
