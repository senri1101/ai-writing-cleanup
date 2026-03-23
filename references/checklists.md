# Shared Checklist

## Core Principles

- Preserve meaning. Rewrite the signal, not the substance.
- Prefer deletion over decorative paraphrase.
- Leave sections untouched when they already read like a person wrote them.
- Keep formatting stable for Markdown, headings, bullets, tables, and code fences.
- Avoid em dashes, en dashes used theatrically, and long double-dash interruptions in prose.

## Shared Problems To Remove

### Meaning Inflation

- Do not append generic significance statements after evidence.
- Do not upgrade ordinary observations into "critical," "pivotal," "game-changing," or "landmark" claims unless the source text explicitly argues that.

### Mechanical Structure

- Remove forced three-part lists when two or one item is enough.
- Break repetitive sentence starts and repeated connective words.
- Replace inline-heading bullets such as `- Speed: ...` with natural bullets or prose.
- Cut conclusion templates that merely restate scope and future importance.

### Chatbot Residue

- Remove assistant framing such as "certainly," "here is," "let's explore," "it is worth noting," and similar politeness filler unless the genre truly requires it.
- Remove praise or agreement aimed at the user unless it serves a real rhetorical purpose.
- Remove vague source gestures such as "studies suggest" when no source is actually given.

### Human Texture

- Allow uneven rhythm when it improves plausibility.
- Prefer one precise image, observation, or judgment over abstract emphasis.
- Keep the author's stance visible when the genre allows it.

## Final Audit Pass

1. Check the first paragraph for generic setup.
2. Check the last paragraph for formulaic closure.
3. Search for repeated transitions.
4. Search for dash-heavy constructions.
5. Search for vague words like "important," "significant," "robust," "notably," and their Japanese counterparts.
6. Read the draft once aloud in your head. If every sentence has the same temperature, loosen it.

## Portable Prompt Pattern

Use this frame when adapting the skill outside Codex:

```text
Revise the following draft so it reads like a capable human wrote it, not like an LLM averaged it.

Requirements:
- Detect whether the draft is Japanese or English and apply the matching rules.
- Preserve factual meaning and document structure.
- Remove AI-signaling patterns: significance inflation, repetitive transitions, trailing interpretation after facts, roundabout copula phrases, forced triads, formulaic intro/outro, dash theatrics, chatbot residue, vague sourcing, and excessive hedging.
- Keep human specificity when the genre allows it.
- Do not explain edits unless asked.

Draft:
{{TEXT}}
```
