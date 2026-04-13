# write-skill-academic-story

A Claude Code plugin that adds a writing skill for producing articles that are:

- interesting from the first paragraph
- strongly story-driven
- grounded in academic evidence
- readable without becoming shallow
- persuasive without pretending certainty

## What it does

This plugin provides a slash-command-style skill:

- `/article-writing-academic-story`

The skill is designed for writing:

- essays
- explainers
- science-informed commentary
- magazine-style longform
- social or technology analysis with research support

Its core goal is simple:

> Write something people actually want to read, while still treating research honestly.

## Writing principles built into the skill

The skill pushes Claude to:

1. open with a real hook
2. build momentum like a story
3. use studies, experiments, and datasets concretely
4. mention limitations and mixed evidence
5. avoid fake citations or overstated conclusions

## Repository structure

```text
write-skill-academic-story/
├── .claude-plugin/
│   └── plugin.json
└── skills/
    └── article-writing-academic-story/
        └── SKILL.md
```

## Usage

After making the plugin available in Claude Code, invoke:

```text
/article-writing-academic-story <topic> [audience] [angle]
```

Examples:

```text
/article-writing-academic-story 睡眠不足如何改变决策
/article-writing-academic-story Why status anxiety shapes modern work general audience
/article-writing-academic-story AI companions and emotional attachment magazine feature
```

## Notes on references

This skill is designed to encourage academically grounded writing, but it should not fabricate citations.

If you want exact, current, verifiable references, provide:

- paper titles
- links
- abstracts
- reading notes
- or a source pack

That gives the skill something concrete to work from.

## Ideal output style

The best outputs from this skill should feel like:

- a compelling feature story
- backed by research
- with enough tension to keep reading
- and enough rigor to be credible

## License

MIT
