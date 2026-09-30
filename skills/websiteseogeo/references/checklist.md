# SEO + GEO checklist

Four parts. Each check has **points**, a **fix type**, and a one-line **why**.

Fix types:
- **Quick** — safe, mechanical, fine to fix once the person has seen the change
- **Decide** — changes structure; needs a quick yes
- **Your call** — about the person's own words or a judgment only they can make; suggest only

Each part's score = points earned ÷ points possible (excluding "not checked") × 100.
Overall = A 30% + B 15% + C 30% + D 25% (re-share weights if a whole part is unchecked).

**Cloaking rule:** anything written for machines (titles, descriptions, structured data, `llms.txt`) must honestly describe what humans see on the page. If the page shows machines different content from humans, it fails the audit regardless of points.

---

## A. Technical basics (110 points)

Can search engines find, read, and list the page?

| Check | Points | Fix | Why |
|---|---|---|---|
| Page has a `<title>` | 8 | Quick | It's the headline in search results. Without one, search engines guess. |
| Title is different from other pages' titles | 5 | Decide | Identical titles make pages compete with each other. |
| Title is roughly 50–60 characters | 4 | Quick | Longer gets cut off in results; much shorter wastes space. |
| Has a meta description (a one or two sentence summary in the page's code) | 6 | Quick | Often shown under the title in results. Without one, a random snippet appears. |
| Meta description is roughly 120–160 characters | 4 | Quick | Fits in the results without being cut off. |
| Has a canonical link (the page's one "official" address) pointing to itself | 7 | Decide | Stops the same page at slightly different addresses counting as duplicates. |
| Not accidentally set to `noindex` (a tag that says "don't list me") | 10 | Your call | One stray tag removes the page from search entirely. Check it's intentional. |
| Site has a `robots.txt` file (instructions for search engine robots) | 5 | Quick | Without it, crawl rules are unclear. A simple "allow everything" file is fine. |
| `robots.txt` does not say `Disallow: /` for everyone | 8 | Your call | That line blocks the whole site from search. Serious if accidental. |
| Site has a `sitemap.xml` (a list of all its pages) | 6 | Quick | Helps search engines find every page, especially deep ones. |
| Sitemap is valid and mentioned in `robots.txt` | 4 | Decide | Broken or unmentioned sitemaps get ignored. |
| Has the mobile viewport setting (`<meta name="viewport" ...>`) | 6 | Quick | Needed to display properly on phones, which search engines rank by. |
| Address starts with `https://` | 7 | Your call | Secure pages rank better and show the padlock. Usually a hosting setting. |
| Exactly one main heading (`<h1>`) | 5 | Decide | It tells search engines the page's main topic. |
| Headings don't skip levels (no jumping from h1 to h3) | 4 | Decide | Clean outline helps search engines and screen-reader users. |
| At least 90% of images have alt text (a short description of the image) | 5 | Decide | Helps image search and people using screen readers. |
| Page states its language (`<html lang="en">` or similar) | 4 | Quick | Tells search engines which language audience it's for. |
| No broken links to the site's own pages | 6 | Your call | Broken links waste search engines' time and frustrate visitors. |
| Page is reachable and allowed to be listed | 6 | Your call | If it can't be listed, nothing else matters. |

**Plain-HTML examples** (for sites where the person edits HTML directly; website builders put these in their settings instead):

```html
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Sourdough for Beginners — A Simple 3-Day Method</title>
  <meta name="description" content="A step-by-step sourdough method for complete beginners, with timings, photos, and fixes for the five most common mistakes.">
  <link rel="canonical" href="https://example.com/sourdough">
</head>
```

A simple permissive `robots.txt` (a plain text file at the site's root):

```
User-agent: *
Allow: /
Sitemap: https://example.com/sitemap.xml
```

Don't block AI tools' robots by default; that works against GEO. Only block private areas.

---

## B. Content (45 points)

Is it clear what the page is about, and is there enough to it? Mostly judgment.

| Check | Points | Fix | Why |
|---|---|---|---|
| Title and main heading agree on what the page is about | 8 | Your call | Mixed signals confuse search engines about which searches it answers. |
| Subheadings cover the subtopics a visitor would expect | 6 | Your call | Good subheadings match what people search for. |
| Enough substance (not just a few lines) | 8 | Your call | Very thin pages rarely show up in search. |
| Easy to read (short sentences, plain words, not a wall of text) | 5 | Your call | Hard-to-read pages lose visitors. |
| Links to other relevant pages on the same site | 7 | Decide | Links between your pages help search engines and visitors find more. |
| Not stuffed with repeated keywords | 6 | Your call | Repeating the same phrase unnaturally looks like spam. |
| Shows it's up to date (date or "updated" note, where timing matters) | 5 | Your call | Out-of-date pages sink for time-sensitive topics. |

---

## C. Machine-readable extras (77 points)

Labels and summaries that help AI tools and search engines understand and trust the page. All must honestly describe the visible page.

| Check | Points | Fix | Why |
|---|---|---|---|
| Site has an `llms.txt` file with real content | 8 | Quick | An emerging convention: a short plain-text guide to the site for AI tools. |
| `llms.txt` honestly matches the visible site | 5 | Your call | If it says things the site doesn't, that's cloaking. |
| `llms-full.txt` (optional fuller text version) | 3 | Decide | Gives AI tools the complete text to quote accurately. Nice to have. |
| Structured data describing the organisation or site | 7 | Decide | Tells machines who is behind the site. |
| Structured data describing articles/posts (headline, author, date) | 7 | Decide | These are the details AI tools quote and credit. |
| FAQ structured data where the page has real questions and answers | 5 | Decide | Question-and-answer content is often shown in AI answers. |
| Breadcrumb structured data (where the page sits in the site) | 4 | Decide | Shows the site's structure. |
| Author identified and linked to the article | 5 | Decide | Clear authorship makes content more trustworthy to cite. |
| Structured data is valid (no errors) | 6 | Quick | Broken structured data is silently ignored. |
| Social sharing tags (Open Graph: `og:title`, `og:description`, `og:image`, `og:type`) | 6 | Quick | Controls how the link looks when shared, and helps crawlers. |
| X/Twitter card tags | 4 | Quick | Controls how the link looks when shared on X. |
| Meaningful page sections (`<main>`, `<article>`, `<nav>`, `<time>`) | 6 | Decide | Helps machines tell the main content from menus and footers. |
| Visible published and updated dates | 5 | Decide | AI tools prefer clearly dated, recent sources. |
| Visible signs of expertise and trustworthiness (who wrote it, why they know) | 6 | Your call | Affects whether AI tools are willing to cite it. |

**What "structured data" means:** a small block of code, invisible on the page, that labels things in a standard way (the common standard is called schema.org, written in a format called JSON-LD). Example, only using facts that are visible on the page:

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "Sourdough for Beginners",
  "author": { "@type": "Person", "name": "[the author name shown on the page]" },
  "datePublished": "2026-03-01",
  "dateModified": "2026-05-10"
}
</script>
```

Never put anything in structured data that isn't true and visible on the page.

**A good `llms.txt`** (a plain text file at the site root, e.g. `example.com/llms.txt`):

```
# Example Bakery School
> Online sourdough and bread courses for complete beginners.

## Key pages
- [Sourdough for Beginners](https://example.com/sourdough): 3-day method with timings and fixes.
- [Courses](https://example.com/courses): what each course covers and what it costs.
- [About](https://example.com/about): who runs the school and how to get in touch.
```

Grade an existing `llms.txt` on: exists; has real entries (not a stub, not the whole site pasted in); descriptions match the pages; current (no dead pages or old prices); full working addresses; not stuffed with keywords; nothing that contradicts the visible site.

---

## D. Quotability (35 points)

When an AI tool reads the page, can it lift a clear, accurate sentence that makes sense on its own? Judge the visible writing. All **Your call**: suggestions only, never rewrite without asking, because this is the person's voice.

| Check | Points | Good | Weak |
|---|---|---|---|
| Key terms clearly defined | 6 | "A sourdough starter is a mix of flour and water that captures wild yeast to make bread rise." | "That's where the starter comes in, and it changes everything." |
| Paragraphs make sense on their own | 6 | "Feed the starter twice a day. After about five days it will double in size within six hours." | "Do this until it does that, which is the whole point." |
| Concrete facts (numbers, dates, names) | 6 | "Our 2025 class of 40 students baked their first loaf in an average of 3 days." | "Students get amazing results." |
| Answers come first | 6 | Heading "How long does it take?" then "About three days from start to loaf." | Same heading, then three paragraphs of history first. |
| Real questions with self-contained answers | 5 | "Can I use regular flour? Yes, plain white flour works fine." | No questions, or one-word answers. |
| Sentences worth quoting on their own | 6 | "A starter that doubles within six hours is ready to bake with." | "As we've seen, this matters for the reasons above." |

The most important four are: making sense on their own, concrete facts, answers first, and quotable sentences.

Every suggestion must use this format and quote the real page:

> **As written:** "[exact sentence from the page]"
> **Why it's hard to quote:** [which check, one line]
> **Could become:** "[a concrete improved version]"

If there's no real weak sentence to quote, there's no suggestion. A clearly written page gets a high score and no suggestions.
