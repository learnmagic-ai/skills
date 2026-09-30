---
name: websiteseogeo
description: Use when you have a web page or website (maybe one you just made with AI) and want to know how findable it is, both on search engines like Google and in AI answer tools like ChatGPT, Claude, Perplexity or Google's AI Overviews. The AI reads your page, runs a checklist, gives you a score and a plain-words list of what to fix, and can help you fix your own files. Say "check my site's SEO", "is my page findable?", or "will AI tools cite my site?".
---

# Website SEO + GEO check

Two jargon words first:

- **SEO** (Search Engine Optimisation) means making a page easy for search engines like Google and Bing to find, understand, and show in results.
- **GEO** (Generative Engine Optimisation) means making a page easy for **AI answer tools** (ChatGPT, Claude, Perplexity, Google's AI Overviews) to understand, quote, and point people to. Here "GEO" has nothing to do with geography or local search.

This skill reads a page, works through a checklist, and tells you in plain words what's good, what's missing, and what to do about it.

---

## One rule above all: no tricks

Adding information **for machines that describes what's already on your page** is good and encouraged: page titles, descriptions, structured data, a sitemap, an `llms.txt` summary file (all explained in the checklist).

Showing search engines or AI tools **different content from what human visitors see** is called **cloaking**. It's a trick, search engines penalise it, and this skill will never suggest it. Everything written for machines must be an honest summary of the visible page. If any "fix" would mean hidden or bot-only content, it's off the table. If the audit finds cloaking already on the page, the page fails the audit whatever its score.

---

## Step 1: Get the page

Ask how the person wants to share their page, and use the first option that works:

1. **Paste the page.** Works everywhere, including plain chat. In most browsers: open the page, right-click, choose **View Page Source**, select all, copy, and paste it here. (For a quick content-only check, copying the visible text also works, but the technical checks need the source.)
2. **A web address (URL) the person gives you.** This only works if your AI has web access switched on. If you try and can't fetch it, say so plainly and ask them to paste the source instead. Only fetch the address they gave you, plus these standard files on the same site if you can: `/robots.txt`, `/sitemap.xml`, `/llms.txt`.
3. **Files in their project folder** (for example in Claude Code). Read only the page files and the site's metadata files in the folder they point you at.

State what you're checking before you start: "I'm checking [page] from [pasted source / the URL you gave / your project folder]."

**Know your limits and say them:**

- A fetched or pasted page may be missing content that loads later via JavaScript (code that runs in the browser). If the page looks nearly empty, say "Some content may load with JavaScript, so this check may miss it" rather than marking everything as missing.
- If you can't see `robots.txt`, `sitemap.xml`, or `llms.txt`, mark those checks as **"not checked"**, not as failed, and tell the person how to look: type the site address followed by `/robots.txt` (and so on) into a browser and paste what appears.
- This skill can't measure real loading speed. If speed matters, point the person to Google's free PageSpeed Insights tool.

## Step 2: Run the checklist

Work through all four parts of the checklist in [references/checklist.md](references/checklist.md):

- **A. Technical basics:** can search engines find and read the page at all?
- **B. Content:** is it clear what the page is about, with enough substance?
- **C. Machine-readable extras:** the labels and summaries that help AI tools understand the page.
- **D. Quotability:** can an AI tool lift a clear, accurate sentence from the page and quote it?

For each check, mark it **pass**, **fail**, or **not checked** (couldn't see it). Only award points for passes.

For part D, every suggestion must **quote the actual weak sentence from the page** and show a better version. General advice like "add more facts" is not allowed. If the writing is already clear, say so and suggest nothing.

## Step 3: Score it

For each part, work out: points earned ÷ points possible (leaving out "not checked" items) × 100. That gives four scores out of 100.

Then combine them into one overall score using these weights: **A 30%, B 15%, C 30%, D 25%.** If a whole part couldn't be checked, leave it out and share its weight among the others. Round to a whole number and give a letter grade: 90+ A, 80+ B, 70+ C, 60+ D, below 60 F.

Show your arithmetic briefly so the person can follow it. Say clearly which items weren't checked.

## Step 4: Report

Use this shape:

```
SEO + GEO CHECK — [page]
Checked from: [pasted source / URL / your files]

Overall: [score]/100 ([grade])
  A. Technical basics      [score]/100
  B. Content               [score]/100
  C. Machine-readable      [score]/100
  D. Quotability           [score]/100
Not checked: [list, and how to check them]

Top 3 fixes (biggest improvement first):
  1. [fix] — [why it matters, in one line]
  2. ...
  3. ...

Everything else:
  Quick fixes (safe, mechanical): [list]
  Worth doing (need a small decision): [list]
  Your call (about your words and content): [list, each with why]
```

Explain every fix in plain words. Assume the person has never heard of a "meta description" before, and say what it is the first time it comes up.

## Step 5: Help fix it (only the person's own files, only with their OK)

Sort fixes into three groups:

- **Quick fixes:** missing page title, missing description, missing mobile setting, missing image descriptions, missing `robots.txt`, `sitemap.xml` or `llms.txt`, missing structured data describing what's already on the page. These are safe and mechanical.
- **Worth doing:** changing headings, adding links between pages, adding a canonical address. These change structure, so they need a quick yes.
- **Your call:** anything that rewrites your actual words. These are suggestions only. How you say things is yours to decide.

**Never overwrite something that's already there and working.** Only fill in what's missing or clearly broken (empty, placeholder text like "My App" or "Untitled").

How to help depends on where you are:

- **In plain chat:** give the ready-to-paste code or text for each fix, say exactly where it goes (for example "inside the `<head>` section, near the top"), and explain what it does. The person makes the change themselves.
- **In Claude Code or another tool that edits files:** first **show every change you plan to make** (which file, what will be added or changed), and wait for the person to say yes. Then make only the approved changes, only in their own project files. Afterwards, list what changed. Don't install anything, don't change settings, and don't touch anything outside their project.
- **For a live site you only have a URL for:** you can't change it. Give the fixes as instructions for whoever (or whatever tool) manages the site.

If the site is built with a website builder or a framework (Squarespace, Wix, WordPress, Next.js and so on), the right place for titles and descriptions is usually a settings panel or a special metadata file, not the raw HTML. Say so, and if you're not sure where it goes in their tool, tell them what to search for in that tool's help pages rather than guessing.

---

## What this skill does not do

- It never suggests cloaking, hidden text, or bot-only content.
- It does not fetch a URL unless your AI has web access and you gave it that URL. Otherwise, paste the page.
- It does not change anything outside your own files, and never changes files without showing you the changes first.
- It does not rewrite your words for you. Content suggestions are yours to accept or ignore.
- It does not track rankings, research keyword popularity, check links from other sites to yours, or measure real-world loading speed.
- It checks one page at a time, not a whole site.
- It cannot promise rankings or AI citations. It removes obstacles; results still depend on your content and on time.
