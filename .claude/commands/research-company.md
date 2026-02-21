# Research a Target Company

Research **$ARGUMENTS** and create structured notes for the job search.

If no company name was provided, ask the user which company to research.

## Step 1: Gather Information

Use web search to research the company. Focus on:

**Company basics:**
- What they do (1-2 sentences — be specific, not marketing-speak)
- Industry, stage (startup/growth/public), approximate headcount
- HQ and office locations
- Recent funding, revenue, or growth signals

**Why they're interesting:**
- What makes this company a compelling target for the user?
- What's their strategic direction? What are they building toward?
- Any recent news, product launches, or leadership changes?

**Open roles:**
- Search for current job postings that match the user's archetypes
- For each relevant role: title, location, key requirements, salary if listed
- Link to the job posting if available

**Key people:**
- Who leads the teams relevant to the user's target roles?
- Any mutual connections or warm paths in?

## Step 2: Map Archetypes

Read the user's profile (`materials/profile.md`) and archetype positioning briefs (`archetypes/*/positioning-brief.md`).

For each relevant archetype:
- How well does this company fit?
- Which specific roles map to which archetypes?
- What's the user's angle — why would this company want *them specifically*?
- What gaps need to be addressed?

## Step 3: Write the Research File

Create `companies/{company-name}.md` using the structure from `templates/company-research.md`.

Include YAML frontmatter:
```yaml
---
company: "Company Name"
industry: ""
stage: ""  # startup, growth, public
headcount: ""
hq: ""
relevant_archetypes: []
priority: ""  # high, medium, low
status: research  # research, targeting, applied, interviewing
---
```

Fill in all sections with what you found. Be honest about gaps — "Could not find salary data" is better than guessing.

## Step 4: Assess Fit

For each relevant open role, write a brief fit analysis:
- **Strong fit:** What parts of the user's background map directly?
- **Gaps to address:** Where is the user light? How can they frame transferable skills?
- **Angle:** What's the narrative hook for the application?

## Step 5: Update Tracker

If `trackers/applications.csv` exists, add a row for each relevant role with status `researching`.

## Step 6: Suggest Next Steps

Tell the user:
- Which role(s) look strongest and why
- Whether they should apply now or gather more intel
- If there are warm paths in (mutual connections, events, content to reference)
- Suggest running `/apply {company} {role}` for the strongest fit

## Rules
- Read `materials/profile.md` before writing anything — the fit analysis depends on knowing the user
- Be honest about fit — don't hype a weak match
- Include direct links to job postings when found
- If the company has no relevant open roles, say so clearly — research is still valuable for networking and future applications
- Don't include the user's personal information in the company research file
