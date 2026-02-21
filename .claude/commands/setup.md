# Interactive Onboarding — Setup Your Job Search

You are setting up a personalized job search system. Guide the user through an interactive interview to understand their background, then help them define role archetypes and scaffold the entire search.

## Step 1: Learn About the User

Ask the user about themselves in a conversational way. Cover these areas (you don't need to ask them all at once — have a natural back-and-forth):

**Career story:**
- What's your professional background? Walk me through the highlights.
- What are you most proud of building, leading, or creating?
- What specific results or metrics can you point to?

**Skills and capabilities:**
- What do you do better than most people in your field?
- What's the common thread across your different roles?
- What skills do people come to you for?

**What you're looking for:**
- What kind of work do you want to do next?
- What industries or company types interest you?
- Are there deal-breakers (location, company size, remote vs. in-person)?
- What's your timeline?

Take notes as they talk. Ask follow-up questions to get specific — push past vague statements like "I'm a good leader" to concrete examples with outcomes.

## Step 2: Identify Archetypes

Based on the interview, propose 3-5 role archetypes. Explain the concept first:

> "An archetype isn't a job title — it's a cluster of roles that share the same 'why you' story. For example, one archetype might group 'Head of Content Strategy,' 'VP of Brand,' and 'Director of Communications' because they all need the same positioning: someone who builds editorial-quality narratives at scale."

For each proposed archetype:
- Give it a short, memorable name (e.g., "Innovation Leader," "Narrative Strategist")
- Describe the positioning in one sentence
- List 3-5 example job titles that fall under it
- Explain why their background makes them credible for this cluster

Discuss with the user. They may want to add, remove, or rename archetypes. Iterate until they're happy with the set.

## Step 3: Scaffold the Search

Once archetypes are agreed upon, create the following:

### 3a. User Profile
Create `materials/profile.md` with:
- Professional summary (2-3 sentences, in their voice)
- Career highlights (bullet points with specifics)
- Key skills and capabilities
- What they're looking for
- Defined archetypes (names + one-line descriptions)

### 3b. Archetype Folders
For each archetype, create `archetypes/{archetype-name}/positioning-brief.md` using the template from `templates/positioning-brief.md`. Fill in what you can from the interview — mark anything that needs more detail with `[TODO: ...]`.

### 3c. Working Directories
Create these directories:
- `companies/`
- `applications/{archetype-name}/` for each archetype
- `materials/`

### 3d. Initialize Trackers
Create `trackers/applications.csv` and `trackers/networking.csv` with headers only (if they don't already exist).

## Step 4: Orientation

After scaffolding, give the user a brief orientation:
- Show them what was created and where it lives
- Explain the recommended workflow: research companies → position → apply → review weekly
- Suggest they run `/research-company` next for 2-3 companies they're already interested in
- Remind them that `/position` can refine any archetype's positioning brief as they learn more

## Rules
- Write in the user's voice, not in corporate-template voice
- Be specific — push for concrete examples and metrics
- Don't fabricate anything — only use what the user provides
- If the user is vague about an area, mark it `[TODO]` rather than making something up
- Keep the conversation moving — don't over-interview. 10-15 minutes should be enough.
