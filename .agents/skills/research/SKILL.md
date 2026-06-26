---
name: research
description: Research a topic from the live web and produce a cited Markdown report. Use when the user asks you to research, investigate, look into, or write a summary/report on a specific topic, question, product, technology, person, or event using web sources.
argument-hint: "What topic should I research?"
---

The user has asked you to research a topic and produce a written summary backed by web sources. Your job is to run a disciplined, multi-pass research workflow and deliver a **cited Markdown report**.

Never answer from parametric memory alone. Every non-obvious claim in the report must trace back to a source you actually fetched during this session.

## Output

Write the report to `research/<YYYY-MM-DD>-<topic-slug>.md` in the current working directory (create the `research/` folder if it doesn't exist). Use the structure in [REPORT-FORMAT.md](./REPORT-FORMAT.md).

After writing, tell the user the file path and give them a 3-5 bullet executive summary in chat.

## Workflow

Research is iterative, not a single search. Work in passes and let what you learn shape the next pass.

### 1. Scope the question

Before searching, restate the topic as a precise research question and identify 3-6 **sub-questions** that a good report must answer. If the topic is ambiguous (e.g. an acronym, a common name, a fast-moving event), ask the user one clarifying question before burning searches.

Note the **as-of date** — today's date — and treat recency as a first-class concern. For anything that changes over time (prices, versions, leadership, statistics, "best X"), prefer recent sources and say when each fact was true.

### 2. Broad pass — map the landscape

Run `WebSearch` on the main question and its sub-questions. Skim results to identify:

- The most authoritative / primary sources (official docs, original studies, primary reporting, standards bodies)
- The range of viewpoints or any active disagreement
- Better search terms you didn't know to use at the start

### 3. Deep pass — read the sources

Use `WebFetch` to actually read the strongest 4-8 sources. Do not summarize from search-result snippets — snippets are leads, not evidence. For each source, extract the specific claims, figures, dates, and quotes relevant to your sub-questions, and record the URL for citation.

### 4. Cross-check pass — verify and fill gaps

- **Corroborate** important or surprising claims against a second independent source. Flag anything you could only find in one place.
- **Resolve conflicts**: when sources disagree, report the disagreement rather than silently picking one. Prefer primary and more recent sources, and explain your reasoning.
- **Close gaps**: run targeted follow-up searches for sub-questions that are still thin. Iterate passes 2-4 until each sub-question is answered or you've established it's genuinely unknown.

### 5. Synthesize the report

Write the Markdown report per [REPORT-FORMAT.md](./REPORT-FORMAT.md). Synthesize across sources into a coherent narrative — do not just stack per-source summaries. Every claim gets an inline citation `[n]` mapping to the Sources list.

## Quality bar

- **Cite everything.** Each factual claim has an inline `[n]` citation. No citation, no claim.
- **Source quality over quantity.** Three primary sources beat ten blog posts reciting each other. Prefer original/primary sources; be explicit when something rests on a single weak source.
- **Separate fact from inference.** Mark your own analysis or extrapolation clearly (e.g. "Analysis:") so it's never mistaken for a sourced fact.
- **Surface uncertainty.** State what you couldn't confirm, what's contested, and what's likely to go stale. A calibrated "this is unclear" is more useful than false confidence.
- **Date-stamp volatile facts.** For anything time-sensitive, say when it was true and link the most recent source.
- **No fabrication.** Never invent a URL, statistic, quote, or source. If you didn't fetch it, don't cite it.

## Scaling depth

Default to the multi-pass workflow above. Adjust to the request:

- **Quick lookup** — the user wants a fast answer: one broad pass + one deep pass on the top source, shorter report.
- **Deep dive** — broad, contested, or high-stakes topic with many sub-questions: consider fanning out the deep pass across parallel background research agents (one cluster of sub-questions each), then merge their cited findings into one report. Confirm with the user before spawning agents, since it costs more.
