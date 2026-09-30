---
name: qc
description: Use right after your AI has made something for you (a web page, a piece of code, a document, an essay, a spreadsheet) and you want it checked before you rely on it or share it. The AI tries it out where it can, re-reads it with fresh skeptical eyes, and ticks it off against what you actually asked for. Say "QC this", "check what you made", or "is this actually done?".
---

# QC: check what you just made

QC stands for "quality control". AI is very good at *saying* something is finished. This skill makes it prove it. You run it after something has been made and before you trust it, publish it, or send it to anyone.

Three checks, in this order:

1. **Try it** — actually open or run the thing, where that is possible.
2. **Review it** — read it again as a stranger would, looking for mistakes.
3. **Check it against the request** — go back to what was asked for and tick off each part.

Then fix the small, obvious problems and report the rest in plain words.

---

## Step 0: Work out what to check

- If the person pointed at something ("check the page you just made", a pasted file, a file name), check that.
- Otherwise, look back through **this conversation** for the most recent thing that was made. If there were several, list them and check each in turn.
- If nothing is clear, ask: "What should I check? Paste it here, or tell me which file."

Only check what the person has given you or what was made in this conversation. Don't go looking through other files or folders.

Sort it into one of these kinds, because each gets tried out differently:

| Kind | Examples |
|---|---|
| **Web page** | an HTML page, a website, an app screen |
| **Code** | a script, a small program, a formula-heavy spreadsheet |
| **Writing** | an essay, an email, a report, a post |
| **Document** | a PDF, a slide deck, a formatted file |
| **Other** | anything else: skip "try it", do the other two |

## Step 1: Try it

The goal is simple: does it actually work when you use it?

**If you can run or open things** (for example Claude Code on the person's computer, or a chat with code tools switched on):

- **Web page:** open it or preview it. Does it load? Is anything visibly broken, overlapping, missing, or unreadable? If you can, also look at it at phone width.
- **Code:** run it once the normal way with a realistic input, then once with an awkward input (empty, very long, a typo). Does it do what it should, and does it fail politely?
- **Document:** open or render it. Are all pages there? Any blank pages, cut-off text, or missing images?
- **Writing:** read it start to finish.

**Never run anything that would have real-world effects** — sending an email or message, posting online, paying for something, changing live data, deleting files. For those, write "Not tried: it would have side effects" and do the other two checks only.

**Plain-chat fallback (no way to run things):** say so honestly, then do a careful "walk-through" instead. Trace through the thing step by step as if you were the user: what happens on load, what each button or line does, what the reader sees first. Then give the person a short, specific list of things to try themselves, for example:

> Please open the page and check: 1) does the menu open on your phone? 2) does the "Send" button do anything? 3) is the text readable against the background?

If trying it reveals it is broken (it crashes, won't open, won't load), **stop here**. Report the failure clearly. There is no point polishing something that doesn't run.

## Step 2: Review with fresh eyes

Pretend you have never seen this before and someone asked you to find what's wrong with it. Look for:

**Anything:**
- Leftover placeholders: "Lorem ipsum", "TBD", "TODO", "[your name here]", example.com
- Broken links, missing images, references to things that don't exist
- Names or labels that change halfway through
- Obvious copy-paste mistakes (the same paragraph twice, the wrong product name)

**Writing and documents:**
- Claims that sound confident but aren't backed up. Flag anything that could be wrong and matters (numbers, dates, names, quotes).
- Filler phrases that make text sound machine-written: "It's worth noting that", "In today's fast-paced world", "delve", "In conclusion", stacks of hedges.
- Tone that drifts from how the person actually writes.

**Web pages:**
- Text that is hard to read (low contrast, tiny, over busy backgrounds)
- Images with no description for screen readers (called "alt text")
- Buttons and links that can't be reached with the keyboard, or give no sign they were clicked
- Layout that breaks on a narrow phone screen

**Code:**
- Errors that are silently swallowed (the program hides a problem instead of reporting it)
- Passwords, API keys, or personal details written straight into the code
- Fake or sample data left in where real data should be
- No handling for obvious bad input

## Step 3: Check it against what was asked

Find the request:

1. If the person gave a brief, plan, or list of requirements, use that.
2. Otherwise, scroll back in this conversation to the message where they asked for the thing to be made, plus any later changes they asked for.

Turn the request into a numbered list of every separate requirement, including small ones. Then mark each one:

- **Met** — say where it is
- **Missing** — say what's absent
- **Partly** — say what's there and what isn't

If a requirement is ambiguous, quote it and mark it "Partly — unclear what was meant". Don't quietly pick an interpretation.

If the request and your own taste disagree, **the request wins**. You can mention your concern under "Needs your call", but don't change something the person explicitly asked for.

## Step 4: Fix the small things, report the rest

**Fix without asking** only when you are confident and the fix doesn't change meaning:

- typos and spelling
- broken links where the right target is obvious
- leftover placeholders where the right text is obvious from context
- a clear, mechanical requirement that was simply missed (a section the request named, a missing label)

**Don't fix; report instead:**

- anything that changes the meaning, the voice, or a design choice
- anything that would take substantial new work
- anything you're not at least fairly sure the person wants

**How to fix depends on where you are:**

- **In plain chat:** give the corrected version (or just the corrected parts, clearly labelled) in your reply. You are not changing any files.
- **In Claude Code or any tool that edits files:** first **show the list of changes you intend to make**, and only make them after the person says yes. Only touch the file(s) being checked. Never change settings, install anything, or edit unrelated files.

## Step 5: The report

Keep it short and readable. Use this shape:

```
QC REPORT — [what was checked]

TRIED IT: Works / Broken / Not tried (why)
  [one line on what happened]

REVIEW: [N] issues found, [M] fixed
  Fixed:
    - [issue] -> [what I changed]
  Needs your call:
    - [issue] — [why I didn't fix it]

MATCHES YOUR REQUEST: [X] of [Y] requirements met
  Based on: [your brief / your message asking for it]
  Met: [requirement]
  Missing: [requirement] — [gap]
  Partly: [requirement] — [what's there vs. asked]

VERDICT: Ready to use / Needs a few fixes / Not working yet
```

If you checked several things, repeat the block for each and finish with a one-line overall verdict.

End with the one or two things the person should do next, in plain words.

## Good habits

- Check fully even if it's a draft. Finding problems early is the point.
- Be honest about what you could not check ("I couldn't open the PDF, so I only reviewed the text").
- Don't pad the report. If it's genuinely fine, say so in three lines.
- Don't mark your own work as passing just because you made it. Assume there is at least one mistake and look for it.

---

## What this skill does not do

- It does not replace a professional review for anything high-stakes (legal, medical, financial, security-sensitive code). It tells you when that's needed.
- It does not run anything that sends, posts, pays, deletes, or changes live data.
- It does not look at files or folders beyond what you gave it or what was made in this conversation.
- It does not change files without showing you the changes first, and it never changes settings or installs anything.
- It does not rewrite your work to its own taste. Meaning, voice, and design choices stay yours.
