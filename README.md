# write-skill-academic-story

A Claude Code plugin that adds a writing skill for producing articles that are:

- interesting from the first paragraph
- strongly story-driven
- grounded in academic evidence
- readable without becoming shallow
- persuasive without pretending certainty
- compatible with the `wechat-mp-auto-publish` pipeline

## What it does

This plugin provides a slash-command-style skill:

- `/article-writing-academic-story`

The skill is designed for writing:

- essays
- explainers
- science-informed commentary
- magazine-style longform
- social or technology analysis with research support
- WeChat public-account drafts that need both narrative force and source discipline

## Publishing-friendly mode

If the user indicates the article is for:

- 微信公众号
- WeChat publishing
- auto publish
- publishing pipeline

then the skill should output:

1. a human-readable article
2. a machine-friendly JSON block for downstream automation

That JSON block is designed to plug into:

- [HashClawAI/wechat-mp-auto-publish](https://github.com/HashClawAI/wechat-mp-auto-publish)

via its `import-skill-output.mjs` bridge.

## Usage

```text
/article-writing-academic-story <topic> [audience] [angle]
```

Examples:

```text
/article-writing-academic-story 睡眠不足如何改变决策
/article-writing-academic-story AI companions and emotional attachment magazine feature
/article-writing-academic-story 为公众号写一篇关于 agentic misalignment 的文章
```

## Ideal output style

The best outputs from this skill should feel like:

- a compelling feature story
- backed by research
- with enough tension to keep reading
- and enough rigor to be credible
- cold, sharp, layered, and suitable for Chinese long-form commentary

## License

MIT
