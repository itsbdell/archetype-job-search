# Draft Outreach Messages

Draft a personalized outreach message for networking or job search purposes.

**Usage:** `/outreach {person, company, or context}`
**Example:** `/outreach Jane Smith at Acme Corp` or `/outreach cold outreach for Head of Product roles`

Arguments provided: **$ARGUMENTS**

If no context was provided, ask the user who they want to reach out to and why.

## Step 1: Understand the Context

Ask the user (if not already clear):
1. **Who** are you reaching out to? (Name, title, company)
2. **How do you know them?** (Cold, warm, mutual connection, met at event, etc.)
3. **What's the goal?** (Informational chat, referral, direct application follow-up, reconnection)
4. **What channel?** (Email, LinkedIn, Twitter DM)
5. **Any signals?** (Their recent work, a post they wrote, a talk they gave, mutual interests)

Read `materials/profile.md` for the user's background, and the relevant archetype brief if this is connected to a specific role type.

If there's a company research file (`companies/{company}.md`), read that too.

## Step 2: Choose the Right Template Pattern

Reference `templates/outreach-templates.md` for structural patterns, but always customize. Common patterns:

- **Warm reconnection:** You know them, haven't talked recently, want to catch up
- **Cold outreach (role-specific):** You don't know them, reaching out about a specific role
- **Referral request:** Asking someone you know to introduce you to someone they know
- **Follow-up after application:** You applied and want to connect with someone at the company
- **Thank you / post-conversation:** After an informational chat or interview

## Step 3: Draft the Message

**General principles:**
- **Short.** 3-5 sentences for the core message. Nobody reads long cold emails.
- **Specific.** Reference something real — their work, the company's recent news, a mutual connection. No "I'm impressed by your company's innovative approach."
- **Clear ask.** What do you want? A 20-minute call? An introduction? Just to share your resume? Say it.
- **No desperation.** You're a professional exploring opportunities, not begging for help.
- **Match the channel.** LinkedIn messages are shorter than emails. Twitter DMs are even shorter.

**Format the output as:**
```
Channel: [email/linkedin/twitter]
Subject: [if email]

[Message body]
```

## Step 4: Review with User

Present the draft and ask:
- Does this sound like you?
- Is there anything to add or cut?
- Any personal details or signals I missed?

Revise as needed.

## Step 5: Update Tracker

After the user approves the message, add a row to `trackers/networking.csv`:
```
{date},{name},{company},{channel},{context},drafted,{follow_up_date},{notes}
```

Set follow-up date to 5 days from today.

Remind the user to update the status to `sent` after they actually send it.

## Rules
- **Never send anything.** Draft only. The user sends it themselves.
- **Use the user's voice.** Read their profile and match their tone, not a template tone.
- **Be honest about the relationship.** Don't pretend familiarity that doesn't exist.
- **One message at a time.** Don't batch-generate 10 outreach messages — each one should be thoughtful.
- **If using a signal** (their recent work, a post), make sure it's genuine and specific — not "I loved your recent article" without saying which one.
