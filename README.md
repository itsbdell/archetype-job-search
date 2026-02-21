# Archetype Job Search

A framework and toolkit for running a job search organized by **capability positioning** instead of job titles. Powered by [Claude Code](https://docs.anthropic.com/en/docs/claude-code).

---

## The Problem

Most job searches start with a list of companies or a list of job titles. You find a role, write a resume for it, then find another role at a different company and write a slightly different resume. After a dozen applications, you have a dozen slightly different versions of yourself, none of them particularly compelling.

The positioning is scattered. Each application reinvents the wheel. Your cover letters are generic because there's no underlying story holding them together. And when someone asks "what are you looking for?" you give a different answer every time.

## The Archetype Approach

This system flips the axis. Instead of organizing your search by company or title, you organize it around **3-5 role archetypes** — clusters of roles that share the same capability positioning.

An archetype is not a job title. It's a **"why you" story** that applies to a set of related roles. Each archetype has:

- A **core positioning statement** — one sentence that captures your angle
- **Lead-with points** — the 3-4 strongest proof points for this cluster
- A **differentiator** — what makes your combination rare
- **Keywords, cover letter angles, and target companies** — the operational details

When you find a job to apply for, you don't start from scratch. You identify which archetype it belongs to, pull the positioning brief, and tailor from there. The story is already built. You're just fitting it to the room.

## What's an Archetype? An Example

Imagine a product manager who spent 8 years building developer tools, then 3 years running an internal innovation team at a bank. Their experience could support several different archetypes:

**"Product Strategist"** — VP of Product, Head of Product, Director of Product Management roles. Leads with market repositioning and team building. Proof points: grew market share, launched AI product line, built 40-person org.

**"Innovation Operator"** — Head of Innovation, Director of Emerging Tech, VP of Strategy roles. Leads with building innovation programs inside large organizations. Proof points: created evaluation frameworks, connected R&D to business outcomes, navigated corporate politics.

**"Technical Evangelist"** — Developer Relations Lead, Head of Developer Experience, Developer Advocate Director roles. Leads with technical credibility and community building. Proof points: conference talks, open-source contributions, developer adoption metrics.

Same person, same career history — three different "why you" stories, each coherent and compelling for its target audience. That's what archetypes do.

## How to Use This

### Prerequisites
- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) installed and configured

### Quick Start

1. **Clone the repo:**
   ```bash
   git clone https://github.com/itsbdell/archetype-job-search.git
   cd archetype-job-search
   ```

2. **Start Claude Code:**
   ```bash
   claude
   ```

3. **Run the setup wizard:**
   ```
   /setup
   ```
   This starts an interactive conversation where Claude interviews you about your background, helps you identify your archetypes, and scaffolds the entire search.

4. **Start researching companies:**
   ```
   /research-company Acme Corp
   ```

5. **Generate application materials:**
   ```
   /apply acme-corp Head of Product
   ```

## The Commands

| Command | What It Does |
|---------|-------------|
| `/setup` | Interactive onboarding — builds your profile and defines your archetypes |
| `/research-company {name}` | Researches a target company: what they do, open roles, key people, fit analysis |
| `/position {archetype}` | Creates or refines a positioning brief for one of your archetypes |
| `/apply {company} {role}` | Generates a tailored resume and cover letter for a specific role |
| `/weekly-review` | Reviews your pipeline: follow-ups due, stale applications, next actions |
| `/outreach {context}` | Drafts a personalized outreach message for networking |

## The Weekly Rhythm

A job search needs operational cadence, not just sporadic effort. Here's a recommended weekly pattern:

**Monday: Review and follow up**
- Run `/weekly-review` to see your pipeline
- Send follow-up messages for applications and outreach
- Update your trackers

**Wednesday: Build pipeline**
- Research 1-2 new companies with `/research-company`
- Complete any applications in progress with `/apply`
- Refine positioning briefs based on what you're learning

**Friday: Network**
- Draft outreach messages with `/outreach`
- Reconnect with your network
- Review the week — what's working, what needs adjustment?

## The Methodology

### Positioning Briefs Are the Foundation

Each archetype gets a positioning brief — a structured document that captures your "why you" story for that cluster of roles. The brief includes:

- **Core positioning** — one sentence that wouldn't describe anyone else in your field
- **Lead-with points** — your strongest evidence, with specifics
- **Differentiator** — what makes your combination rare or hard to replicate
- **Cover letter angles** — narrative hooks that open a conversation
- **Keywords** — terms from real job postings, for ATS optimization

The brief is a *source document*, not a final product. Every resume and cover letter under that archetype draws from it, but each is tailored to the specific company and role.

### Company Research Is Strategic, Not Bureaucratic

When you research a company, you're not just collecting facts. You're building an argument for why *you specifically* should work *there specifically*. The research file captures:

- What the company does and where it's heading
- Which of your archetypes fit and why
- Specific open roles with fit analysis (strengths, gaps, angles)
- Key people and potential warm paths in
- Your strategic positioning for this company

### Tailored Applications Tell a Story

A tailored resume isn't a different resume — it's the same career, with different emphasis. For each application:

1. Start with the archetype positioning brief
2. Read the company research and job posting
3. Reorder experience to lead with what's most relevant
4. Mirror the company's language naturally
5. Address gaps honestly with transferable-skill framing

The cover letter isn't a resume summary. It's a narrative argument: why this person + this role + this company = a great fit. One core argument, developed with specific evidence, in 3-4 paragraphs.

### Outreach Is Part of the System

Networking isn't separate from the application process. The outreach templates and networking tracker are designed to work alongside your applications:

- Research a company → identify key people → reach out
- Get a referral → apply with an internal champion
- Follow up after applying → turn a cold application into a warm one

## Project Structure

```
archetype-job-search/
├── README.md                    # This file
├── CLAUDE.md                    # Instructions for Claude Code
├── LICENSE                      # MIT
├── .claude/commands/            # Slash commands
├── templates/                   # Reference templates
├── trackers/                    # Application and networking CSVs
├── examples/                    # Fictional filled examples
│
│   --- Created by /setup ---
├── materials/profile.md         # Your background and career story
├── archetypes/{name}/           # Positioning brief per archetype
├── companies/{name}.md          # Research per target company
└── applications/{archetype}/    # Tailored materials per application
```

## Templates

The `templates/` directory contains structural guides for all the key documents. They're not empty forms — each template includes field descriptions, instructions, and tips for what makes each section effective.

| Template | Purpose |
|----------|---------|
| `positioning-brief.md` | Structure for archetype positioning briefs |
| `company-research.md` | Structure for target company research notes |
| `outreach-templates.md` | Message patterns for common outreach scenarios |
| `star-stories.md` | STAR format interview story library |
| `resume-master.md` | Resume structure with tailoring guidance |

## Examples

The `examples/` directory contains fictional but realistic filled examples showing how the templates look when completed. These use a made-up product strategist named Maya Chen — the examples demonstrate the level of specificity and thinking that makes the system work.

---

## Credits

Built by [Brian Dell](https://briandell.xyz). The archetype methodology was developed during a real job search and turned into this open-source tool. Brian co-writes [Little Futures](https://littlefutures.substack.com/) with Tom Critchlow — a newsletter about near-term technology change.

## License

MIT — use it, fork it, make it yours.
