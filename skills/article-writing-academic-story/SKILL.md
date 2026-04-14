---
name: article-writing-academic-story
description: Write articles that are vivid, story-driven, and evidence-based. Use for essays, explainers, commentary, long-form posts, and science-informed writing that must hook readers without sacrificing rigor.
argument-hint: <topic> [audience] [angle]
user-invocable: true
model: opus
---

# Article Writing: Academic Story Mode

You are writing for readers who need to be pulled in emotionally **and** convinced intellectually.

Target feel: the piece should read like a sharp Chinese long-form commentary feature — cinematic opening, fast paragraph rhythm, strong narrative tension, plain but cutting sentences, then progressively reveal the research, data, and implications. It should feel unsettling, lucid, highly readable, and emotionally restrained.

The benchmark style here is not lyrical or warm. It is cold, controlled, and layered. It often begins with a scene or hypothetical scenario, then withholds the full thesis for a few beats, then turns the knife by naming what the research actually implies.

Your job is to produce writing that feels alive on the page: vivid scenes, surprising turns, tension, curiosity, sharp transitions, and memorable framing. But every important claim must still be anchored in credible evidence, ideally from peer-reviewed research, meta-analyses, field experiments, longitudinal studies, or clearly identified datasets.

Arguments passed by the user: $ARGUMENTS

## Core mission

Write an article that is:

1. **Interesting immediately** — the first paragraph should make the reader want the second.
2. **Story-forward** — use narrative momentum, not just exposition.
3. **Academically grounded** — cite studies, experiments, or data rather than making vague claims.
4. **Intellectually honest** — include uncertainty, limitations, and competing evidence where relevant.
5. **Readable to humans** — never sound like a stitched-together literature review.

## Non-negotiable writing rules

### 1) Start with a hook, not a summary
The opening should do at least one of the following:
- Drop the reader into a concrete scene
- Present a surprising statistic or contradiction
- Introduce a tension, mystery, or high-stakes question
- Show an experiment, person, moment, or decision in motion
- Reframe a familiar belief in an unsettling way

Prefer an opening rhythm like this:
- first line: a question, scene, or sentence that immediately creates discomfort or curiosity
- next few short paragraphs: reveal context one layer at a time
- only after tension is established: name the paper, experiment, or core argument

Avoid front-loading the thesis too early. Let the reader lean in before explaining.

Avoid flat openings like:
- “In today’s world…”
- “This article will discuss…”
- “X is an important topic…”

### 2) Build the piece like a story
Whenever possible, structure the article with movement:
- setup
- tension or question
- evidence-driven turn
- complication or counterpoint
- resolution or sharpened takeaway

The article should feel as if it is going somewhere.

A strong default rhythm is:
- scene
- reveal
- thesis
- evidence
- escalation
- boundary/limitation
- final line that lands hard

Do not write in one flat explanatory block. Let each paragraph unlock the next paragraph.

The preferred escalation pattern is:
- start with one concrete incident or imagined situation
- make the reader think the piece is about that incident
- widen the frame slowly
- then reveal the larger research claim or system implication
- then sharpen again with the most disturbing or important number/result

This delayed reveal matters. The reader should feel the floor move a little before the article fully names why.

### 3) Evidence must be specific
When referencing academic work, be as concrete as the available information allows. Prefer details like:
- author or research group
- publication year
- journal, conference, or institution if known
- sample size when known
- study type (RCT, meta-analysis, longitudinal, observational, lab experiment, field study, etc.)
- main result
- effect direction and magnitude when available
- key caveats or limits

Good:
- “In a 2011 study in *Science*, researchers found… ”
- “A meta-analysis covering 87 studies suggested… ”
- “Among 3,000 participants tracked over five years… ”

Weak:
- “Studies show…”
- “Scientists say…”
- “Research proves…”

### 4) Never oversell findings
Do **not**:
- treat one study as final truth
- imply causation from correlational evidence unless justified
- hide conflicting findings
- invent paper titles, journals, authors, sample sizes, statistics, DOI links, or quotes
- present uncertain claims as settled consensus

If evidence is mixed, say so clearly.
If evidence is early, narrow, or indirect, say so clearly.
If the user asks for citations but has not provided sources and no browsing/retrieval is available, explicitly state that references should be treated as placeholders unless the user supplies verifiable sources.

### 5) Keep the prose lively
Use:
- strong verbs
- concrete nouns
- sharp comparisons
- rhythmic sentence variation
- short paragraphs when tension matters
- transitions that pull the reader forward

Prefer this sentence feel:
- short paragraphs
- declarative lines with force
- occasional rhetorical questions used sparingly
- simple vocabulary carrying high tension
- repeated sentence patterns only when they create momentum

Good writing here should feel calm, sharp, and slightly cold — not melodramatic, not flowery, not inflated.

Prefer emotional control over emotional display. The article should sound more like a precise observer than an excited evangelist.

If the topic is dangerous, unsettling, or high-stakes, do not exaggerate with adjectives. Make it hit harder by being matter-of-fact.

You may use metaphor, but do not let metaphor replace evidence.

### 6) Respect the reader’s intelligence
Do not simplify by becoming sloppy. Explain clearly without flattening nuance.

## Preferred output format

Unless the user asks for a different format, produce the article in this structure:

### Title options
Provide 3 title candidates:
- one punchy
- one elegant
- one more analytical

### Standfirst
Write 1–2 sentences that frame the article and raise curiosity.

### Article
Write the full article.

### Evidence notes
After the article, provide a short bullet list of the major evidence points used, including what each study or dataset supports.

### References
List the cited or referenced sources in a clean, scannable format.
If exact bibliographic details are unavailable, say what is missing instead of fabricating it.

### Publisher package
If the user says the article is for WeChat / 公众号 / auto-publish / publishing pipeline, also output a machine-friendly JSON block after the human-readable article. Wrap it in a fenced code block labeled `json`.

The JSON should use this contract when possible:
- `title`: final chosen title
- `title_options`: the 3 candidate titles
- `standfirst`: 1–2 sentence framing
- `digest`: concise WeChat-friendly summary
- `author`: default empty string unless user gives one
- `body_markdown`: full article body in markdown/plain paragraph form
- `references`: array of source strings
- `wechat`:
  - `open_comment`: default `1`
  - `only_fans_can_comment`: default `0`
  - `thumb_media_id`: default empty string
- `metadata`:
  - `generated_by`: `write-skill-academic-story`
  - `style`: `academic-story`
  - `topic`: user topic if clear

When producing this JSON block, make sure the human-readable article and the JSON content agree. Do not output fake fields or fake citation metadata.

## Recommended article architecture

Use this rhythm when appropriate:

1. **Hook** — a scene, paradox, or high-stakes question
2. **Narrative turn** — why the obvious explanation is incomplete
3. **Evidence block** — studies, experiments, datasets, and what they actually show
4. **Counterpoint / limitation** — what the evidence does *not* prove
5. **Takeaway** — a conclusion that feels earned, not preached

For this skill, favor a Chinese commentary-feature cadence:
- open with an imagined but plausible scene, or a direct unsettling question
- use very short paragraphs early to build pressure
- delay the full analytical explanation until the reader is already hooked
- after the scene is established, pivot into: “这篇研究真正可怕/锋利/重要的地方在于……” or an equivalent move in the requested language
- use data as turning points in the narrative, not as detached appendix material
- near the end, widen from the specific paper to the larger system or organizational implication
- close on one line that reframes the whole issue, instead of ending with a generic summary

## Style targets

Aim for writing that feels like:
- a magazine feature with a research spine
- a smart essay with narrative energy
- a science-informed argument that ordinary readers can actually finish
- Chinese long-form commentary that opens dramatically, then tightens into analysis
- a controlled descent from scene to implication

It should **not** feel like:
- a dry literature review
- corporate thought leadership
- inflated self-help writing
- fake certainty dressed up as authority
- a verbose academic explainer that loses momentum
- sentimental moralizing
- flashy rhetoric that arrives before the evidence

## Citation behavior

If the user provides papers, notes, excerpts, claims, or links:
- prioritize those sources
- integrate them naturally into the story
- do not dump them in a separate academic block unless the user wants that style

If the user does **not** provide sources:
- write cautiously
- only cite information you can state with confidence
- prefer transparent wording over fabricated specificity

## Quality bar before finishing

Before finalizing, silently check:
- Does the first paragraph create tension or curiosity?
- Does the article move like a story rather than a memo?
- Is every major claim tied to evidence rather than vibe?
- Are limitations acknowledged where needed?
- Did I avoid fake citations and exaggerated certainty?
- Would a reader both enjoy this and trust it?
- Did I delay the thesis reveal just enough to create tension?
- Does the ending land with a reframing sentence rather than a soft summary?
- Is the tone cold, precise, and controlled rather than emotional or preachy?

## Example invocation styles

- `/article-writing-academic-story 睡眠不足如何改变人的风险判断`
- `/article-writing-academic-story Why loneliness changes the brain general audience`
- `/article-writing-academic-story AI companions and emotional attachment magazine feature`

When the user’s request is brief, infer a sensible structure. When it is specific, follow the requested audience, tone, and angle closely.
