---
name: stress-test
description: Use when you have a written plan and are about to start building it, to have it checked with fresh eyes for gaps, wrong assumptions, and things that will break, before you spend time on it.
---

# Stress Test

You have a plan. Before you (or an AI) spend hours building it, it's worth having someone look at it with fresh eyes and try to find the problems. That's what this skill does.

The key idea is **fresh eyes**. Whoever wrote the plan, or helped write it, is too close to it. They fill gaps in their head without noticing. A good reviewer has never seen the plan before, has no stake in it, and has one job: find what's wrong before it costs anything.

Start by saying: "I'll stress-test this plan with fresh eyes. I'm looking for problems, so expect some."

---

## Step 1: Get the plan

This skill needs a plan to check. Ask the person to **paste it into the chat**, or point to a file they have shared with you.

- If they paste it or share a file, use that.
- If a plan was already written earlier in this conversation, offer to use that one. Confirm first.
- If there is no plan yet, say so kindly. Suggest writing one first, even a short one. A stress test on "I want to make an app" has nothing to grip.

Only use what the person gives you. Don't go searching for other files or information.

If the plan is about something they are building (a website, an app, a spreadsheet), and they have also shared the actual project files, you may look at those files to check the plan's claims. If not, work from the plan alone and say which claims you could not check.

---

## Step 2: Get fresh eyes

The review works best when the reviewer has no memory of how the plan was made.

- **If you can run a subagent** (for example in Claude Code): hand the review to a subagent. Give it only the plan, the six lenses below, the rating scale, and the output format. Do **not** give it this conversation. That clean start is the point.
- **If you can't** (for example in a normal Claude.ai chat): you have two options. Tell the person about both.
  1. **Best:** they open a brand-new chat, paste the plan, and ask for a stress test using the six lenses. A new chat has no history, so it's truly fresh.
  2. **Good enough:** do the review here. Deliberately set aside anything said earlier in this chat. Read the plan as if a stranger handed it to you. Be honest that this is less independent than a fresh chat.

---

## Step 3: Run the six lenses

Act as an experienced reviewer who has never seen this plan and is responsible for catching problems before anyone commits time. Run **every** lens. Be specific: point to the exact part of the plan and describe exactly what would happen. Not "this might be an issue." Instead: "Step 3 says 'add a sign-up form' but never says where the sign-ups are stored, so they'll be lost."

### 1. Clarity
Could two different people, with only this plan, build the same thing?
- Vague steps ("make it look nice", "add validation") where a real choice is hiding
- Words or terms that are never explained
- Options mentioned ("maybe A or B") but never decided
- Places where you'd have to guess what the writer meant

### 2. Assumptions
What is the plan taking for granted that might be wrong?
- About tools or services (does that tool actually do this? is it free? does it need an account?)
- About people (will users really do this step? will someone else really help?)
- About time, money, or skills
- About the thing being built (does that file, page, or feature really exist yet?)
- If you have the real files or facts, check the assumption. Don't just list theoretical worries.

### 3. Scope creep
Is the plan doing more, or less, than the goal?
- Extras that weren't asked for ("nice to haves" that sneaked in)
- Things the goal clearly needs but the plan forgets
- A "not included" list, if there is one: is it honest?
- Anything the plan might change or break that it shouldn't touch

### 4. Edge cases
What happens off the happy path?
- Empty input, or no data at all
- Way too much input (a huge file, thousands of users)
- Something fails halfway through. What state is it left in?
- No internet, a service is down, a login expires
- Someone types something weird or tries to misuse it
- Two people doing the same thing at the same time

### 5. Fit
Does this plan match what already exists?
- If they have an existing project: does the plan follow the way it already works, or bring in a clashing new approach?
- Does it add new tools when existing ones would do?
- Does it follow any rules or conventions the person told you about?
- If there's nothing existing, say "no existing project to fit" and move on.

### 6. Feasibility
Can this actually be done as written?
- Are the steps in a workable order? Does anything depend on a later step?
- Are the tools, accounts, and pieces it needs really available?
- Are time estimates realistic, especially for a beginner?
- Is there a way to tell each step worked? ("Open the page and see the list" is checkable. "It works" isn't.)
- Are setup steps missing (making an account, getting a key, installing something)?

---

## Step 4: Rate each finding

Every problem gets one label:

- **BLOCKER:** Must fix before starting. It would make the plan fail, lose data, or cause real damage.
- **RISK:** Should fix. The plan might work without it, but it's a known weak spot.
- **NOTE:** Worth knowing. No action needed.

Don't inflate. A missing comma is not a blocker. Don't deflate either. If it will break, call it a blocker.

---

## Step 5: Write the report

Use this shape:

```
# Stress Test: [plan name]
Date: [today]

## BLOCKERS (fix before starting)
- [finding, pointing to the exact part of the plan]
(or "None found.")

## RISKS (should address)
- [finding and why it matters]
(or "None found.")

## NOTES (good to know)
- [observation]
(or "None.")

## Summary
Blockers: [n]   Risks: [n]   Notes: [n]

## Verdict
PASS / PASS WITH RISKS / FAIL
```

**Verdicts in plain words:**
- **PASS:** The plan is solid. Go build it.
- **PASS WITH RISKS:** You can go ahead, but look at the risks first. The person decides which to fix now and which to accept.
- **FAIL:** There are blockers. Fix those, then build.

Put the report in the chat. If you are in a tool that can save files, you may offer to save it next to the plan (for example as `stress-test.md`). Only save if they say yes.

---

## Step 6: Hand it back

Give a short plain summary after the report:

- **If blockers:** "I found [N] blockers. The biggest is [one sentence]. I'd fix these before building. Want to work through them together?"
- **If risks only:** "The plan can go ahead. There are [N] risks worth a look. Here's the one I'd fix first: [one sentence]."
- **If clean:** "This plan passed. It's clear enough to build from. Go for it."

When fixing blockers, change only what the findings point to. Don't rewrite the parts that were fine. Plans often get worse when a fix touches everything.

---

## What this skill does not do

- It does not write the plan. It needs a plan to exist first.
- It does not fix the plan by itself. It reports problems; the person decides what to change.
- It does not build anything or run anything.
- It does not look at files or information the person didn't give it.
- It is not a guarantee. A plan that passes can still hit surprises. It just has fewer obvious ones.
