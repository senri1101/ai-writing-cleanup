# ai-writing-cleanup

`ai-writing-cleanup` は、日本語と英語の文章に含まれる「AIが書いたっぽさ」を減らすための bilingual skill と prompt pack です。source of truth はこのリポジトリにあり、同じ編集ルールを Codex でそのまま使いながら、Copilot、Gemini、Claude Code にも流用できます。

## 何をするものか

- 下書きが主に日本語か英語かを見分けます。
- 事実の意味を変えずに、よくある AI 文体のシグナルを削ります。
- Markdown の構造、引用、専門用語をできるだけ保ちます。
- むやみに言い換えるのではなく、削除・単純化・具体化を優先します。

## リポジトリ構成

- [SKILL.md](./SKILL.md)
- [agents/openai.yaml](./agents/openai.yaml)
- [references/checklists.md](./references/checklists.md)
- [references/ja.md](./references/ja.md)
- [references/en.md](./references/en.md)
- [prompts/tool-agnostic.md](./prompts/tool-agnostic.md)

## Codex で使う

このリポジトリを Codex の skills ディレクトリにコピーするか symlink してください。あるいは、skill フォルダとして直接参照させても動きます。

典型的な呼び出し方:

```text
Use $ai-writing-cleanup to revise this draft so it reads naturally in Japanese or English without obvious AI-writing tells.
```

## Codex 以外で使う

[prompts/tool-agnostic.md](./prompts/tool-agnostic.md) を開き、共通プロンプトを Copilot、Gemini、Claude Code などに貼り付けて使ってください。全面リライトではなく、その場で文章を整える前提の書き方にしてあります。

説明しすぎるモデルには、以下を追加してください。

```text
Return only the revised draft unless I explicitly ask for commentary.
```

## 保守メモ

- AI 文体のシグナルは変わるので、公開知見に合わせてルールも更新してください。
- 抽象的な文体論より、実際の文章に即した例を優先してください。
- ただの言い換え支援にならないルールだけを増やしてください。

## English Summary

`ai-writing-cleanup` is a bilingual skill and prompt pack for reducing recognizable AI-writing patterns in Japanese and English. It preserves meaning, structure, citations, and terminology while removing common LLM tells such as inflated significance, repetitive transitions, formulaic intros and outros, dash-heavy phrasing, chatbot residue, and vague sourcing.
