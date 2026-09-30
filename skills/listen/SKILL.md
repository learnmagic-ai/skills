---
name: listen
description: Use when you give your AI several pieces of feedback or requests in one message (a list, a long paragraph, notes after reviewing something) and want every single point handled, none skipped or merged. The AI numbers your points, checks it heard them all, works through them in order, and ends with a ticked-off checklist. Say "listen", "make sure you get all of these", or just send a message with lots of points.
---

# Listen: never drop a point

When you send an AI a message with six things in it, it will often do four of them well, blend two together, and quietly forget the last one. This skill stops that. It turns your message into a numbered list, confirms the list with you, handles each point one by one, and shows you a checklist at the end.

## When to use it

- You've reviewed something the AI made and have a batch of changes.
- You've written a long message with several requests mixed into it.
- You've been burned before by points going missing.

The AI can also start this on its own when your message clearly contains **four or more separate requests**, or you say things like "a few things", "several points", or "also...". If it does, it should say so in one line first: "There are several points here, so I'll list them to make sure I get them all."

---

## Step 1: Pull out every point and number them

Read the whole message and pull out **every** separate request, change, question, or piece of feedback. Include small asides: if the person mentioned it, it counts.

- One point per line. If one sentence contains two requests ("fix the header and make the button blue"), that's two points.
- Restate each point briefly in plain words, close to how they said it. Don't reinterpret.
- If a point is a question rather than a request, keep it as a point: it needs an answer.

Show the list like this:

```
I found 5 points in your message:

1. Make the title shorter
2. Change the button colour to blue
3. Remove the second paragraph
4. Question: can this work on phones?
5. Add a contact email at the bottom

Is that everything? Add or correct anything before I start.
```

## Step 2: Wait for a yes

Don't start working until the person confirms the list. If they add or correct points, update the list and show it again.

The only exception: if the person has already said "just go" or "no need to confirm", go ahead, but still show the list first so they can see what you're working from.

## Step 3: Handle each point, in order

Work through the list from 1 to the end. For each point:

- Start with its number and a short label: **"1. Shorter title:"**
- Do what it asks (make the change, answer the question, give your view).
- Say briefly what you did.

Rules while you work:

- **Never merge points.** Even if two are related, each gets its own number and its own answer.
- **Never skip a point** because it seems small or obvious.
- **Keep the numbers fixed.** Point 3 stays point 3 from start to finish, even if you add more.
- **If a point is unclear, ask about that point by number** ("On point 4, did you mean X or Y?") and carry on with the others. Don't guess on something that matters.
- **If the person adds something mid-way** ("oh, and also..."), add it as the next number (6, 7, ...) and include it.
- **If two points conflict** (point 2 says blue, point 5 says keep the original colours), don't pick one silently. Name the clash and ask.
- **If you can't do a point** (you don't have access, it needs information you don't have), mark it blocked with the reason instead of leaving it out.

In plain chat, "doing" a point usually means giving the revised text, answer, or suggestion right there in your reply. If you are working in a tool that edits files, only change the files the person is talking about.

## Step 4: The final checklist

When all points are handled, finish with:

```
Done: 1. Shorter title
Done: 2. Button colour changed to blue
Blocked: 3. Remove second paragraph — you asked to keep it in point 5, which one wins?
Done: 4. Answered: yes, it works on phones (details above)
Done: 5. Contact email added

4 of 5 done, 1 needs your decision.
```

- Every point from Step 1 appears, with the same number.
- The count at the bottom must add up. Never recount to hide a miss.
- If you realise you missed one, say so by number, do it, and show the checklist again.

---

## Tips for the person giving feedback

This skill works whatever form your message takes, but these habits make any AI follow you better. The AI can share them if you ask "how should I write my feedback?".

1. **Use a numbered list.** Numbers beat bullet points, and bullet points beat a paragraph. Each number becomes something that can be ticked off.
2. **End with a count.** "That's 6 changes, please do all 6." It makes skipping obvious.
3. **One thing per point.** "Fix the header and rename the file and maybe add a photo" is three points.
4. **Say what you want, not only what you don't.** "Use a friendlier tone, like talking to a neighbour" works better than "don't be so formal".
5. **Add the why.** "Shorten the intro, people won't scroll past it" helps the AI get the next similar thing right too.
6. **Put background first and your request last.** AI pays most attention to the start and end of a message.
7. **Be direct.** "Change X to Y" is clearer than "could you maybe look at X?".
8. **Save capital letters for the one thing that truly matters.** If everything is URGENT, nothing is.
9. **If you've corrected the same thing twice and it's still wrong,** start a fresh chat and restate what you want clearly. A long, tangled conversation makes AI worse, not better.

A simple template:

```
Feedback on the draft:
1. [change] — because [why]
2. [change] — because [why]
3. [change]

That's 3 changes. Please do all 3 and show me a checklist at the end.
```

And if points still go missing:

```
You missed points 3 and 5. Please go back and do:
3. [restate point 3]
5. [restate point 5]
```

---

## What this skill does not do

- It does not decide which of your points matter. Every point gets handled or clearly marked as blocked.
- It does not guess at unclear points that matter. It asks about them by number.
- It does not change anything outside what your feedback is about.
- It does not remember your preferences between conversations. Each time, it works from the message in front of it.
