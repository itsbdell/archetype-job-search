# Weekly Pipeline Review

Review the job search pipeline, identify follow-ups, and plan next actions.

## Step 1: Read the State

Read these files:
1. `trackers/applications.csv` — all applications and their status
2. `trackers/networking.csv` — all outreach and networking contacts
3. `materials/profile.md` — for context on archetypes and goals

If trackers are empty or don't exist, tell the user and suggest starting with `/research-company` and `/setup`.

## Step 2: Application Pipeline

Present a summary table:

**By status:**
| Status | Count | Companies |
|--------|-------|-----------|
| Researching | | |
| Preparing | | |
| Applied | | |
| Interviewing | | |

**Follow-ups needed:**
- Applications submitted 5+ days ago with no response → suggest follow-up
- Applications in "preparing" for 3+ days → remind to finish or drop
- Any application marked "interviewing" → check for upcoming dates, prep needed

**Stale items:**
- Company research files with no associated applications (researched but never applied)
- Applications stuck in the same status for 10+ days

## Step 3: Networking Pipeline

**Outreach summary:**
- Messages sent this week
- Responses received
- Meetings scheduled or completed
- Follow-ups due (sent 5+ days ago with no reply)

**Suggestions:**
- People to reach out to based on target companies
- Follow-up messages for stale conversations

## Step 4: Archetype Health

For each archetype:
- How many applications are active?
- Is the positioning brief complete or still has `[TODO]` items?
- Are there enough target companies researched?

Flag any archetype that has zero activity or incomplete positioning.

## Step 5: Recommended Actions

Prioritize and present a concrete action list for the week:

1. **Follow-ups to send** (specific companies/people, draft messages if helpful)
2. **Applications to complete** (materials in progress)
3. **Companies to research** (suggested based on archetype gaps)
4. **Positioning to refine** (if briefs need work)
5. **New targets to explore** (if pipeline is thin)

Rank by impact — an interview follow-up beats a cold research task.

## Step 6: Weekly Rhythm Check

Remind the user of the recommended cadence:
- **Monday:** Review pipeline, send follow-ups, update tracker
- **Wednesday:** New applications, company research
- **Friday:** Networking outreach, weekly review

Ask if they want to adjust the rhythm based on how the search is going.

## Rules
- Be honest about momentum — if the pipeline is thin, say so
- Don't generate busywork — only suggest actions that move the search forward
- If there's nothing to follow up on, that's fine — focus on building pipeline
- Read actual file dates/timestamps when checking for staleness
- Present information concisely — this is a review, not a report
