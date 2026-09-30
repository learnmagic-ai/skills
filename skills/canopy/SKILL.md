---
name: canopy
description: Use when you have a plan and want to see which parts are strong and which are fragile, by imagining three different futures for it (it failed, it barely succeeded, a reviewer judges each decision) and comparing where they agree.
---

# Canopy

Canopy looks at your plan from the future, three times, from three different angles. Then it compares the three stories.

- **The failure story:** six months on, the project quietly fizzled out. What went wrong?
- **The near-miss story:** six months on, it worked, but only just. What almost sank it?
- **The decision review:** a sharp reviewer grades each big decision in the plan.

Any one of these stories on its own can mislead you. A failure story will always find *something* to blame, because it was told to. A success story can gloss over real problems. The value comes from **comparing** them:

- Where all three agree something is a problem, it's almost certainly real.
- Where all three agree something is solid, protect it. Don't "fix" it.
- Where only the failure story sees a problem, it may be made up.
- Where only the success story leans on something, that's a hidden dependency: the plan quietly relies on it.

Canopy shows what's fragile **and** what's strong. Both matter.

---

## Step 1: Get the plan

Canopy needs a plan. Ask the person to **paste it into the chat**, or point to a file they have shared with you. If a plan was already written earlier in this conversation, offer to use that one.

- If it's shorter than a paragraph, ask for more detail first: what they're making, the main steps, the key choices. There's nothing to test in one line.
- If it's very long (several pages), first boil it down to the key decisions and main steps, and use that summary.

Only use what the person gives you. Don't look for other files or information.

## Step 2: Ask how much is at stake

Ask one question: "How big a deal would it be if this failed?"

- **Just for fun:** "You dropped it after a month. Nothing lost but some time."
- **For someone else** (a friend, client, or group): "They were polite, but it didn't meet what they needed, and they didn't come back."
- **Others rely on it:** "It broke when people needed it. Trust took a real hit."
- **A big deal:** "The whole effort was dropped. The time and money are gone."

If they're unsure, use "for someone else". Don't guess the level for them. This only shapes the failure story.

---

## Step 3: Write the three stories

Each story must refer to **specific parts of the plan** by name. Generic stories are useless.

**How to run this step:**
- **If you can run subagents or parallel agents** (for example in Claude Code): give each story to its own agent, all at once. Give each one only the plan and its own instructions below. They must not see each other's work. Separate agents keep the stories truly independent.
- **If you can't** (for example in a normal Claude.ai chat): write the three stories one after another right here. Write each one as if you hadn't written the others. Don't reuse phrases or borrow ideas across them. Tell the person, in one line, that the stories are less independent than they'd be with separate agents, so the comparison is a bit less reliable.

### Story 1: The failure story

> It's six months from now. The project was wound down after four months. Not a disaster. A quiet, disappointing fade. It took longer and cost more than planned, and people lost faith in it. [Add the stakes line from Step 2.]
>
> Write what happened. Cover: what cracked first; the root cause versus the surface cause; warning signs that were ignored; assumptions that turned out wrong; and the one decision that set the path.

Rules for this story:
- Be specific and realistic. Concrete details, not "communication was poor."
- No dramatic disasters that wouldn't really happen.
- **Every failure must trace to one of three things:** something outside the person's control, a limit on time or money, or an assumption that could turn out false. "They just made a bad call" doesn't count. That's hindsight talking.
- Don't blame a decision that was sensible given what was known at the time.

### Story 2: The near-miss story

> It's six months from now. The project succeeded, but it was close. Three things nearly derailed it.
>
> For each near-miss: what was the risk; how was it caught; what would have happened if it wasn't; and when was it caught?

Rules for this story:
- The value is in the near-misses, not the celebration. A success story with no close calls is fiction.
- No generic praise ("everyone worked hard").
- Each near-miss should connect to a specific part of the plan.

### Story 3: The decision review

> You're writing for a review panel that will read this in six months. You're known for clear, bold calls that age well. Hedging has hurt your reputation before.
>
> For each major decision in the plan: what was decided; what the alternatives were; what was and wasn't known at the time; a grade (STRONG, ADEQUATE, WEAK, or NOT ENOUGH INFO); and whether it will age well, and why.

Rules for this story:
- Commit. "It depends" and "time will tell" are not answers.
- Judge the **decision**, not the outcome. A good decision can have bad luck. A bad decision can get lucky.
- Don't miss a major decision.

---

## Step 4: Compare the stories (the divergence map)

Now look at all three side by side. List every risk, strength, or decision that **any** story mentions. For each one, check whether the other stories mention it too, even in different words. "The sign-up form lost people's details" and "we caught the sign-up bug early" are the **same** factor.

For every match, **quote the words** from each story you're connecting, so the person can check your matching at a glance.

Build a table like this:

```
| # | Factor            | Failure | Near-miss | Review | Signal          | Evidence                  |
|---|-------------------|---------|-----------|--------|-----------------|---------------------------|
| 1 | [specific name]   | yes     | yes       | yes    | ALL AGREE       | "[quote]" / "[quote]" ... |
| 2 | [specific name]   | yes     | no        | yes    | REAL RISK       | "[quote]" / "[quote]"     |
| 3 | [specific name]   | yes     | no        | no     | PROBABLY IMAGINED | "[quote]"               |
| 4 | [specific name]   | no      | yes       | no     | HIDDEN DEPENDENCY | "[quote]"               |
```

What each signal means:

- **All agree it's a problem → Serious risk.** Act on it.
- **All agree it's sound → Strength.** Protect it. Don't weaken it when revising.
- **Failure + review agree, near-miss ignores it → Real risk.** Optimism may be hiding it.
- **Only the failure story sees it → Probably imagined.** That story was told to find failure. Treat it with doubt unless it rests on something you can actually check.
- **Only the near-miss story relies on it → Hidden dependency.** Success quietly depends on this. Make sure it's real.
- **Failure and near-miss disagree → Key uncertainty.** The outcome hinges on this.
- **Near-miss + review agree it's sound → Strength.** The thinking is good; doing it well is what matters.

Name each factor specifically ("the price of $40", not "risk 1"). Aim for at least three factors. **Find at least two strengths.** Plans have strong parts, and pointing them out is as useful as finding the weak ones.

Before moving on, quickly check: at least three factors; every row has quoted evidence; factor names are specific; each story pointed at real parts of the plan. If one story came out vague, redo just that story.

---

## Step 5: The report

Write this in the chat:

```
# Canopy: [plan name]
Date: [today]    Stakes: [level]

## Divergence map
[the table]

## Strengths (all stories agree these work - protect them)
## Serious risks (all stories agree)
   [risk, how it fails, how it was caught in the near-miss, the reviewer's grade, what to do]
## Key uncertainties (stories disagree)
## Hidden dependencies (only the near-miss story relies on these)
## Probably imagined (only the failure story sees these - and what evidence would make them real)
## Decision grades (strongest decisions first, then weakest)
## What to do next
   [a short, ordered list, including "protect X" as well as "fix Y"]
```

**The protect rule:** every "fix this" recommendation must also say what to **leave alone**. Plans get weaker when a revision touches everything. Keep changes narrow.

End with one plain next step:
- **Clean:** "Your plan holds up. Its strengths are confirmed. Go build it."
- **A few risks, solid base:** "Fix [these specific risks] with small changes. Don't touch [the strengths]. Then go ahead."
- **Key uncertainty:** "Settle [this question] first. The plan's base is sound; this is a question to answer, not a flaw."
- **Serious problems:** "Rework [this specific section] before building. Keep [these strengths] as they are."

Also give a two-or-three-sentence summary on top: the biggest strength, the biggest risk, and the one thing to do next.

**Saving it (optional):** If you are in a tool that can save files, you may offer to save the report as a document. Only do it if they say yes. In a normal chat, the report in the conversation is the finished product.

**If something goes wrong:** if one story can't be completed, compare the two you have and say which is missing. If the comparison step fails, show the three stories side by side and help the person spot the patterns together.

---

## What this skill does not do

- It does not change the plan. It shows where it's strong and where it's fragile. The person decides what to change.
- It does not predict the future. The stories are thinking tools, not forecasts.
- It does not check whether each step is technically doable. For that, use a stress test.
- It does not work well on code itself. It's for plans and decisions.
- It does not look at anything beyond the plan the person gives it.
