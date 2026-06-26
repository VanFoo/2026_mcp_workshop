# Report Format

Research reports are Markdown files saved to `research/<YYYY-MM-DD>-<topic-slug>.md`.

Use the structure below. Keep prose tight — a report is for someone who wants the answer, not a transcript of your searching. Every factual claim carries an inline citation `[n]` that maps to the **Sources** list at the bottom.

```markdown
# <Topic Title>

> **Research question:** <the precise question this report answers>
> **As of:** <YYYY-MM-DD>  ·  **Confidence:** <high / medium / low>

## Executive summary

3-6 bullets capturing the key findings. A reader should get the whole answer
from this section alone. Cite the load-bearing claims [1][3].

## Key findings

### <Sub-question or theme 1>
Synthesized answer with inline citations [2]. Report disagreement between
sources where it exists, and prefer primary/recent sources [4].

### <Sub-question or theme 2>
...

## Analysis

Your own interpretation, implications, or extrapolation — clearly separated
from the sourced facts above. This is the one section that may go beyond the
sources, and it must be labeled as analysis.

## Open questions & caveats

- What you could not confirm or found only in a single weak source.
- Points where sources conflict and why you leaned the way you did.
- Facts likely to go stale, and roughly how fast.

## Sources

1. [<Title>](<url>) — publisher, date. One line on what it supports and how
   trustworthy it is (primary/secondary, official/independent).
2. [<Title>](<url>) — ...
```

## Rules

- **Inline citations are mandatory.** `[n]` after each claim, matching the Sources list. No source, no claim.
- **Only cite what you fetched.** Every URL in Sources is one you actually read this session. Never fabricate a link, title, date, quote, or statistic.
- **Annotate each source** with publisher, date, and a note on its reliability (primary vs secondary, official vs independent).
- **Date volatile facts inline** ("as of <date>") when they can change.
- **Be honest in the Confidence field** — base it on source quality and corroboration, not on how much you wrote.
