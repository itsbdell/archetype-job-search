# Archetype Job Search

A Claude Code-powered job search system organized by **role archetypes** — clusters of roles that share a capability positioning.

---

## Core Concept

Most job searches are organized by company or title, leading to scattered positioning and generic applications. This system flips the axis: organize around 3-5 archetypes that each tell a coherent story about what you do. Every application inherits its positioning from the relevant archetype, so your materials are always focused and consistent.

**An archetype is not a job title.** It's a capability cluster — a set of related roles that share the same "why you" story.

---

## Project Structure

```
archetype-job-search/
├── materials/
│   └── profile.md              # User background, skills, career story (created by /setup)
├── archetypes/
│   └── {archetype-name}/
│       └── positioning-brief.md  # The positioning strategy for this archetype
├── companies/
│   └── {company-name}.md       # Research notes per target company
├── applications/
│   └── {archetype}/{company}_{role}/
│       ├── resume.md            # Tailored resume
│       └── cover-letter.md      # Tailored cover letter
├── trackers/
│   ├── applications.csv         # Application pipeline tracker
│   └── networking.csv           # Outreach and networking tracker
├── templates/                   # Reference templates (don't edit directly)
└── examples/                    # Filled examples for reference
```

### File Naming Conventions
- Archetype folders: lowercase, hyphenated (e.g., `narrative-gtm`, `innovation-leadership`)
- Company files: lowercase, hyphenated (e.g., `acme-corp.md`)
- Application folders: `{archetype}/{company}_{role}` (e.g., `narrative-gtm/acme-corp_head-of-content`)

---

## User Data

After running `/setup`, the user's background and career story live in `materials/profile.md`. Always read this file first when generating any materials. It contains:
- Professional summary
- Career history highlights
- Key skills and capabilities
- What they're looking for
- Their defined archetypes (with cross-references to archetype folders)

---

## Tracker Formats

### applications.csv
```
date,company,role,archetype,status,contact,follow_up_date,notes
```

**Status values:** `researching`, `preparing`, `applied`, `interviewing`, `offered`, `rejected`, `withdrawn`

### networking.csv
```
date,name,company,channel,context,status,follow_up_date,notes
```

**Channel values:** `email`, `linkedin`, `twitter`, `intro`, `event`
**Status values:** `drafted`, `sent`, `replied`, `meeting_scheduled`, `met`, `follow_up_needed`

---

## Voice and Tone

When generating materials for the user:
- **Be specific, not generic.** "I led a 25-person team that built X" beats "I am a proven leader with extensive experience"
- **Lead with outcomes.** What happened because of what you did?
- **No buzzword soup.** Skip "synergy," "leverage," "passionate about." Say what you mean.
- **Match the company's language.** Mirror terminology from job postings and company communications.
- **The user's voice matters.** After setup, write in a style that matches how they described themselves — don't impose a corporate template voice.

---

## Working With Archetypes

Each archetype has a positioning brief in `archetypes/{name}/positioning-brief.md` containing:
- **Core Positioning:** One sentence that captures the "why you" story
- **Lead With:** 3-4 strongest proof points for this archetype
- **Key Proof Points:** Specific accomplishments with metrics
- **Differentiator:** What makes this positioning rare or hard to replicate
- **Cover Letter Angles:** Narrative hooks for cover letters
- **Target Companies:** Types of companies this archetype fits
- **Keywords:** Terms to match in job descriptions and ATS systems

When generating application materials:
1. Read the relevant archetype's positioning brief
2. Read the company research file
3. Tailor the positioning to the specific role — the brief is a source, not a script
4. Emphasize proof points that match the job description's requirements
5. Address gaps honestly with transferable-skill framing

---

## Commands

| Command | Purpose |
|---------|---------|
| `/setup` | Interactive onboarding — build your profile and define archetypes |
| `/research-company` | Research a target company and create structured notes |
| `/position` | Create or refine a positioning brief for an archetype |
| `/apply` | Generate tailored resume and cover letter for a specific role |
| `/weekly-review` | Pipeline review, follow-ups, and next actions |
| `/outreach` | Draft personalized outreach messages |

---

## Templates

Reference templates live in `templates/`. These are structural guides — use them when creating new files, but always customize to the user's voice and context. Never copy a template verbatim.

---

## Important Rules

1. **Never fabricate credentials.** Only use accomplishments the user has provided.
2. **Always read before writing.** Check `materials/profile.md` and relevant archetype briefs before generating anything.
3. **Update trackers.** After creating applications or outreach, update the relevant CSV.
4. **Create directories as needed.** If an archetype or company folder doesn't exist, create it.
5. **No personal data in templates or examples.** The `templates/` and `examples/` directories should never contain real user information.
