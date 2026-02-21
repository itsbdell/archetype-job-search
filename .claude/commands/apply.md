# Generate Application Materials

Generate tailored application materials for a specific role.

**Usage:** `/apply {company} {role title}`
**Example:** `/apply acme-corp Head of Product Marketing`

Arguments provided: **$ARGUMENTS**

If company or role wasn't specified, ask the user.

## Step 1: Gather Context

Read these files (stop and ask the user to create missing ones):

1. **Company research:** `companies/{company}.md` — if missing, suggest running `/research-company` first
2. **User profile:** `materials/profile.md` — must exist (run `/setup` if not)
3. **Archetype brief:** Determine which archetype fits this role from the company research file's `relevant_archetypes`, then read `archetypes/{archetype}/positioning-brief.md`
4. **Resume template:** `templates/resume-master.md` — for structure reference

If the role maps to multiple archetypes, ask the user which positioning to lead with.

## Step 2: Analyze the Role

From the company research file (and any job posting link), identify:
- What the role actually needs (not just what the posting says)
- Which of the user's proof points map most directly
- What gaps exist and how to address them
- The company's language and tone (mirror it)

## Step 3: Generate Resume

Create a tailored resume at `applications/{archetype}/{company}_{role}/resume.md`.

**Resume principles:**
- **Reorder, don't rewrite.** Lead with the experience most relevant to *this specific role*
- **Headline/summary** should echo the archetype's core positioning, tuned to the company
- **Proof points first.** For each role in work history, lead with the accomplishments most relevant to the target job
- **Mirror keywords** from the job posting naturally (not keyword-stuffed)
- **Quantify everything possible.** Numbers, percentages, dollar amounts, team sizes
- **Cut the irrelevant.** De-emphasize or remove experience that doesn't support the positioning

## Step 4: Generate Cover Letter

Create a cover letter at `applications/{archetype}/{company}_{role}/cover-letter.md`.

**Cover letter principles:**
- **Not a resume summary.** It's a narrative argument for why *this person* + *this role* + *this company* = great fit
- **Open with a hook.** Why this company, why now, why you care. Not "I am writing to express my interest..."
- **One core argument.** Pick the strongest angle from the positioning brief and develop it
- **Specific proof.** 1-2 concrete examples that demonstrate the core argument
- **Address the gap** (if any) with a transferable-skill frame — one sentence, confident, then move on
- **Close with energy.** What you'd want to do in the first 90 days, or what excites you about the specific challenge
- **Keep it to one page.** 3-4 paragraphs max.

## Step 5: Update Tracker

Add or update the row in `trackers/applications.csv`:
```
{date},{company},{role},{archetype},preparing,,,"Materials generated"
```

## Step 6: Review with User

Present both documents and ask:
- Does the resume emphasis feel right?
- Does the cover letter sound like you?
- Anything to add, cut, or reframe?
- Ready to mark as `applied` once submitted?

Make revisions as needed.

## Rules
- **Never fabricate credentials.** Only use what's in the profile and positioning brief.
- **Don't use the same cover letter twice.** Every letter should reference something specific about *this company*.
- **Read the job posting carefully.** If the company research file includes a job description, use its exact language where natural.
- **Create the application directory** if it doesn't exist.
- **The user decides when to apply.** Generate materials, don't submit anything.
