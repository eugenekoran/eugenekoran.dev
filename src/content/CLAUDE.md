# Content Style Guide

## Project pages (`projects/*.md`)

### Frontmatter
- `title`: Short, noun-phrase title — no verbs, no trailing punctuation
- `description`: One sentence, starts with a past-tense verb ("Developed...", "Designed..."), states what was built and the key outcome
- `pubDate`: Use the actual date of the work, not today
- `tags`: Technology/topic tags, title-cased. Keep to 4–5 max, sorted alphabetically
- `category`: `research` for academic work, omit (defaults to `personal`) for side projects

### Section structure
Use this order when applicable:
1. `## Overview` — 2–3 sentences, third-person or neutral, describes the project scope and context
2. `## Contributions` — first-person implied ("Developed...", "Designed..."), 3–5 bullets, high-level and method-agnostic unless a specific method is central to the contribution
3. `## Results` — only for research projects; lead with the core insight in plain language, anchor with key numbers, explain *why* the metric matters rather than assuming the reader knows
4. `## Links` — GitHub repo and/or paper links
5. `## Technologies` — comma-separated list, no bullet points

### Writing style
- **Contributions**: Focus on agency, not what the research found. Keep bullets high-level
- **Results**: Lead with the insight, then the number — not the other way around.
- **Bold** used sparingly: key numbers and the core takeaway phrase
- Avoid jargon acronyms
- **Flow**: Each sentence should be easy to parse on first read. Prefer short sentences over long ones with multiple embedded clauses. The Overview especially should be accessible — avoid dense noun stacks and unexplained technical terms
