---
name: research-methodology
description: Use when you need to know whether something is actually true and how sure you can be, not just what the internet says. For checking a claim, a statistic, a news story, a product promise, or a piece of research (including research your AI just did for you). The AI breaks the claim into parts, checks each against independent sources, looks for its own blind spots, and labels how confident it really is. Say "is this true?", "how sure are we?", "check this claim", or "research this properly".
---

# Research methodology: find out what's true, and how sure to be

AI can collect information fast. That is not the same as research. Research is the part where you check what you collected and throw out what doesn't hold up. This skill is that checking step.

The core idea: **treat every claim as unconfirmed until it has been checked.** The goal is not "what do sources say?" but "what is still standing after we checked it?"

Use it on its own (to check one claim or article), or alongside any research you're asking the AI to do (so the final answer comes with honest confidence labels).

---

## Before you start: what can you actually check from here?

Be upfront about this at the start, in one line:

- **With web access** (search or page-fetching switched on): you can look up sources directly.
- **Without web access** (plain chat with no browsing): you can only work from (a) what the person pastes in and (b) your own training knowledge, which may be out of date or wrong in the details. Say so. Then either ask the person to paste the sources they have, or give them a short list of exactly what to look up and where (see [references/where-to-look.md](references/where-to-look.md)), and check what they bring back.

**Your own memory is a starting point, never a source.** Anything you "just know" counts as unverified until something outside you backs it up.

Only use the sources the person gives you and public information. Don't ask for passwords or private accounts, and don't send their material anywhere.

---

## Step 1: Is this the original, or a copy?

For each claim or source, ask: **is this the first report, or someone repeating it?**

- A news article that says "according to a study" is a copy. Find the study.
- Ten websites saying the same thing often trace back to **one** original. That is one source, not ten.
- Mark copies as **"repeated"**. They only count if they add something new (new data, a named expert, a correction).

## Step 2: How reliable is this source, based on its track record?

A source isn't simply "trustworthy" or not. Ask about its history:

- **Does it usually break news first, or repeat others?**
- **Has it been right before on this kind of topic?** A great tech reporter isn't automatically reliable on medicine.
- **Has it changed suddenly?** A new topic, a sudden change in tone, or an account posting far more than usual can be a warning sign.
- **Who runs it, and do they gain if you believe this?**

Weak or unknown sources need at least two independent confirmations before you rely on them.

## Step 3: Break the claim into four parts

Almost any factual claim can be split into four questions. Check each one separately:

| Part | The question | Ways to check |
|---|---|---|
| **When** | When did this happen or become true? | Dates on the original, publication dates, archived copies of pages, other reports of the same event |
| **Where** | Where did this happen, or where does it apply? | Named places, maps, local sources, whether it's about one country or everywhere |
| **Who** | Who did or said this? | Is the person or organisation real? What else have they said? Are they quoted accurately? |
| **What** | What actually happened or is being claimed? | Do several independent sources describe the same thing? Does the original data say what the headline says? |

Not every claim needs all four. A statistic mostly needs "who measured it", "when", and "what exactly was measured". Skip the parts that don't apply, and say which ones you skipped.

## Step 4: Look for independent confirmation

For each part that matters, look for a **second source that did not get it from the first.** Two outlets both quoting the same press release are not independent.

Also look for evidence **against** the claim just as hard as evidence for it. Search for the opposite ("X is false", "X criticism", "X debunked", "X correction").

## Step 5: Give an honest confidence label

Count how many of the parts that matter are independently confirmed:

- **HIGH:** all or nearly all key parts confirmed by independent sources
- **SOLID:** at least two key parts independently confirmed
- **SINGLE SOURCE:** only one source, or all sources trace back to one
- **UNCONFIRMED:** nothing outside the claim itself backs it up

Show it like this for anything important:

```
CLAIM: [the statement]
  When:  confirmed (sources A, B) / one source only (C) / not checked
  Where: ...
  Who:   ...
  What:  ...
  -> Confidence: SOLID
```

Never let a single-source claim slip into the final answer sounding like a settled fact. Say "one source reports..." instead.

## Step 6: Check yourself for blind spots

Before giving your answer, run through these seven questions. They are numbered so the person can push back on any one of them.

1. **Am I only seeing the winners?** Successes get posted, failures don't. Ten happy customer stories say nothing about how many people quietly gave up.
2. **Where is information thick, and where is it thin?** English vs. other languages, big cities vs. rural areas, popular sources vs. obscure ones. The real story may be in the gap.
3. **Is this confirmation, or just an echo?** Many sources agreeing can mean it's true, or that they all copied one original. Trace it back.
4. **Am I overweighting the newest thing?** Fresh doesn't mean more important.
5. **Did I look as hard for evidence against my conclusion as for evidence for it?**
6. **Has anything been cropped or taken out of context?** A true quote, clip, or chart can still mislead when the surrounding part is missing.
7. **Who gains if people believe this?** If one side clearly benefits, treat the way it's framed with extra care.

End your answer with a short **blind-spot note**, two lines:

```
Blind-spot check: [which of the 7 I considered]
Still a concern: [which ones are live, and why]
```

## Step 7: Show your sources

Every claim that matters should point to where it came from. For each one, give:

- the source (link, title, or "pasted by you")
- when you looked at it (today's date is fine)
- whether it's the original or a repeat
- which part it supports (when / where / who / what)
- the confidence label

If the person needs this for something serious (a legal matter, a formal complaint, a piece of journalism), suggest they save copies of the pages (screenshots or PDFs) now, since web pages change and disappear.

---

## A quick routine for checking a pile of links or articles

When someone hands you several items at once:

1. **Original or copy?** Put copies aside unless they add something new.
2. **Source track record?** Mark weak or unknown sources as needing two confirmations.
3. **Split into when / where / who / what.** Note which parts are unclear.
4. **Look for independent confirmation** of the parts that matter, and for evidence against.
5. **Run the seven blind-spot questions.**
6. **Label confidence and list sources.**

## Look for the pattern, not just the facts

When you have several confirmed findings, ask what **pattern** connects them: something moving, something happening on a regular rhythm, several people converging on the same thing, a usual pattern suddenly breaking. Individual facts go stale. Patterns usually tell you more and last longer.

## Traps to avoid

- **Counting echoes as confirmations.** Count original sources, not total mentions.
- **Rounding up confidence.** "Multiple sources confirm" when only one is original.
- **Confident on one part only.** Knowing *where* something happened doesn't tell you *when* or *who*.
- **Letting the easy source decide the answer.** If the first search engine is all you checked, say so.
- **Skipping the blind-spot note.** Every research answer gets one.

## Final self-check before answering

- Did I separate originals from repeats?
- Did I trace key claims back to where they started?
- Do the important claims have at least two parts independently confirmed?
- Did I run the seven blind-spot questions and include the note?
- Did I list sources for every important claim?
- Did I say clearly what I could **not** check, and what's missing?
- Are my confidence labels honest?

If any answer is no, fix it, or tell the person plainly what's still unchecked.

For a map of the different *kinds* of places information can come from, and how to avoid getting everything from one kind, see [references/where-to-look.md](references/where-to-look.md).

---

## What this skill does not do

- It does not make an uncertain claim certain. Sometimes the honest answer is "we can't tell yet".
- It does not browse the web unless your AI already has web access switched on. Without it, it works from what you paste and says so.
- It does not replace a qualified professional for medical, legal, or financial decisions.
- It does not investigate private individuals, get into private accounts, or send your material anywhere.
- It does not treat the AI's own memory as proof.
