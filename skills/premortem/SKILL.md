---
name: premortem
description: Use before you start a project, launch, or decision that matters, to imagine it has already failed, work out why, and fix those weak spots now while it is still cheap to change course.
---

# Premortem

A postmortem looks at what went wrong after something failed. A premortem does the opposite. You imagine the thing has **already failed**, and you work backwards to explain why. You do this before you start, while you can still change the plan.

The method comes from psychologist Gary Klein. It works because of a simple trick of the mind. Ask people "what could go wrong?" and they give careful, vague answers. Tell them "it failed, explain how" and they switch into storytelling mode. The reasons get more specific, more creative, and more honest. Researchers call this "prospective hindsight": looking back from an imagined future.

It matters extra when you work with an AI. AI assistants tend to be agreeable and optimistic. Ask "is this a good plan?" and you will usually hear yes. The premortem breaks that habit. The AI stops looking for reasons your plan will work and starts explaining how it fell apart.

---

## When to use it

Good targets:
- Something you are about to build, launch, or share with people
- A plan where money, time, or your reputation is on the line
- A change to how you price, sell, or run something
- A hire, a partnership, or a big personal decision
- Anything where being wrong would really cost you

Not a good fit:
- A vague idea with no plan yet. Help the person shape a plan first, then premortem it.
- A question with one right answer. Just answer it.
- Feedback on a piece of writing. That is editing, not a premortem.
- A decision that is already made and can't be undone. A premortem only helps while you can still change course.

---

## Step 1: Get enough context (the minimum bar)

A premortem is only as good as what it knows. Vague input gives vague failures that help nobody.

First, use what is already here. Read back through this conversation. The person may already have described the plan. Use anything they pasted or attached. Do not go looking for other files or information they did not give you.

Then check you know three things:

1. **What is it?** You should be able to describe the plan back in one sentence.
2. **Who is it for, or who does it affect?** Customers, friends, a team, a family, the person themselves.
3. **What does success look like?** Failure is the opposite of success. If you don't know what a win looks like, you can't say what failure looks like.

If you have all three, go straight to Step 2. Don't ask questions you don't need.

If something is missing, ask for the most important missing piece. **One question at a time.** After each answer, check again. Keep it friendly, like a conversation, not a form. If you can reasonably work something out from what they said, do that instead of asking.

Example questions:
- "What exactly are you about to launch, build, or decide?"
- "Who is this for?"
- "What would a win look like for you here?"

---

## Step 2: Set the frame

Say the premise out loud. Something like:

> "OK, I have enough to go on. Here's the premise: it's six months from now. [The plan] has failed. It's over. We're looking back to understand what went wrong."

Don't skip this. The "it already failed" frame is the whole trick. Without it, the analysis slides back into polite, hedged risk-talk.

---

## Step 3: List every real reason it failed

Now list every genuine reason the plan could have died. One or two sentences each.

Each reason should be:
- **Specific to this plan.** Not generic advice that fits anything.
- **Grounded in details the person gave you.**
- **A real threat.** Not a tiny annoyance, not a wildly unlikely disaster.

Don't pad the list with weak reasons, and don't stop early if there are more. Some plans have 4 real failure modes. Some have 9. The number is whatever is true for this plan.

---

## Step 4: Go deep on each reason

Take each failure reason and investigate it on its own. For each one, write:

1. **The failure story.** Two or three short paragraphs telling how this failure actually played out. Use real details from the plan. Name the moments where things went wrong. Make it read like a true case study.
2. **The hidden assumption.** In one sentence: what was the person taking for granted that let this happen?
3. **Early warning signs.** One or two things they could actually see or count that would show this failure is starting. Not vague feelings. Things like "fewer than 5 sign-ups after the first week."

Keep each deep-dive short, under about 300 words. Be direct. Don't sugarcoat.

**How to run this step:**
- **If you can run subagents or parallel agents** (for example in Claude Code), give each failure reason to its own agent, all at the same time. Give each one the full plan context, the "it already failed" frame, its one assigned reason, and the three-part format above. Running them separately keeps one story from colouring the next.
- **If you can't** (for example in a normal Claude.ai chat), do the deep-dives one after another right here in the conversation. Treat each one as a fresh investigation. Don't let an earlier story shape a later one.

---

## Step 5: Pull it together (the premortem report)

This is the part most people will actually read, so make it sharp and specific. Write:

1. **The most likely failure.** Which story is most probable, given what you know? Why? This is where to focus first.
2. **The most dangerous failure.** Which one would do the most damage, even if it's less likely? This is the one worth insuring against.
3. **The hidden assumption.** Across all the stories, what's the single biggest thing the person is assuming without questioning it? This is often where the real value lives: the thing so obvious to them they forgot it was an assumption.
4. **The revised plan.** Concrete changes that make the plan tougher. Each change should link to a specific failure story. Not "think about your pricing." Instead: "test the price with 20 people before announcing it publicly." Every change should be something they could do this week.
5. **The before-you-start checklist.** Three to five things to check, test, or set up before going ahead. Each one should prevent or catch one of the failures.

---

## Step 6: Deliver it

Put the full report in the chat, synthesis first, then the individual failure stories underneath for anyone who wants the detail.

Then add a short plain summary on top, three sentences at most:
- the most likely failure,
- the hidden assumption,
- the single most important change to make.

**Saving it (optional):** If you are in a tool that can save files, you may offer to save the report as a document in the person's project folder. Only do this if they say yes. In a normal chat, the report in the conversation is the finished product. They can copy it wherever they like.

---

## A short example

**Person:** "Premortem this: I'm launching a $40 online class teaching parents how to use AI to plan family meals. 30 spots. I'll promote it in two local parent groups."

**Some failure reasons:**
1. The parent groups allow only one promotional post a month, so most people never see it.
2. Parents who most need meal planning have the least free time to attend a live class.
3. The people who sign up are already comfortable with AI and find the class too basic.
4. Preparing good examples for different diets (vegetarian, allergies, picky kids) takes three times longer than planned.

**Synthesis, in brief:** The most likely failure is reach: two groups with posting limits won't fill 30 spots. The most dangerous is the time mismatch: if busy parents can't attend live, the whole format is wrong, not just the marketing. The hidden assumption is that "parents who want help with meals" will show up for a scheduled class. The revised plan: offer a recorded version alongside the live one, and ask five parents this week whether they would pay $40 and when they could attend, before building anything.

---

## Things to keep in mind

- **Always set the frame.** "This already failed" is what makes the method work.
- **Be thorough, not padded.** Find every real reason. Don't invent extra ones to look impressive.
- **The synthesis is the product.** Make it specific and something the person can act on.
- **Don't sugarcoat.** The point is to tell the person what they don't want to hear, before reality does. Be kind in tone, honest in content.
- **Respect the minimum bar.** One more question beats a generic premortem.
- **Stay inside what you were given.** Work only from the conversation and anything the person shared.

---

## What this skill does not do

- It does not make the decision for the person. It shows the risks; they choose.
- It does not predict the future. The failure stories are useful imaginings, not forecasts.
- It does not replace expert advice on legal, medical, or financial questions. If a failure story points there, say so and suggest talking to a professional.
- It does not change any files or plans on its own. It hands back a report and a revised plan for the person to use.
- It is not for editing writing or answering simple factual questions.
