# Learn Magic skills

Eight free skills for people who have just started making things with AI.

More about them, with examples: https://learnmagic.ai/skills

## What's a skill?

A skill is a saved set of instructions your AI follows for a particular kind of job.

Instead of explaining "please check this properly, and here's how" every single time, you install a skill once. After that, your AI knows the method and uses it when it fits, or when you ask for it by name.

Each skill here is just a folder with a plain text file called `SKILL.md` inside (sometimes with an extra reference file). You can open it and read exactly what it tells your AI to do. There are no programs to run and nothing hidden.

## The skills

| Skill | What it's for |
|---|---|
| **premortem** | Imagines your plan has already failed, works out why, and helps you fix those weak spots before you start. |
| **stress-test** | Challenges a plan before you commit to it: hidden assumptions, scope creep, edge cases, and whether it's realistic. |
| **intake** | Interviews you to turn a rough idea into a clear project brief: goal, people involved, limits, what success looks like, and scope. |
| **canopy** | Looks at a plan from several imagined futures (it failed, it barely succeeded, a reviewer judges each decision) to show what's fragile and what holds up. |
| **qc** | Checks something your AI just made: tries it where possible, re-reads it with fresh eyes, and ticks it off against what you asked for. |
| **listen** | Makes sure every point in a long message of feedback gets handled: numbers them, works through them in order, ends with a checklist. |
| **research-methodology** | Helps you find out whether a claim is actually true and how sure you can be, with honest confidence labels and sources. |
| **websiteseogeo** | Checks how findable your web page is on search engines (SEO) and in AI answer tools (GEO), with a score and a plain-words fix list. |

Every skill is written to work in a normal Claude chat. If a step works better with extra tools (like web access or files on your computer), the skill says so and gives you a way to do it without them.

## Try one first

Each of these prompts was used to test the skill in a fresh Claude Code install. Paste one in after installing, then swap in your own plan, page or claim.

| Skill | A first thing to say |
|---|---|
| **premortem** | `Use the premortem skill on this plan: I will run a free two-hour Saturday workshop at my local library teaching 12 retirees to use AI to write letters.` |
| **stress-test** | `Use the stress-test skill on this plan: build a one-page website for my dog-walking business this weekend with AI, put my prices and a booking form on it, and share the link on Monday.` |
| **intake** | `Use the intake skill. My idea: a simple page where parents in my kid's class can sign up to bring snacks for the school trip.` |
| **canopy** | `Use the canopy skill on this plan: my small bakery takes about 40 orders a week by phone. Next month I switch to an order form page that emails me each order.` |
| **qc** | `Use the qc skill to check this page I asked for ("a page with my name in big blue letters, centered"):` followed by the page's code. |
| **listen** | `Use the listen skill on this feedback:` followed by your list of changes, all in one message. |
| **research-methodology** | `Use the research-methodology skill. Claim to check: "Honey never spoils." How sure can we be, and what kind of source would settle it?` |
| **websiteseogeo** | `Use the websiteseogeo skill on this page:` followed by your page's code (or its address, if your AI can browse the web). |

## How to install

No terminal needed for the first two options. The easiest route is the ready-made ZIP for each skill, which already has the right folder layout. Download it from [learnmagic.ai/skills](https://learnmagic.ai/skills) (each skill has a download button), or use a direct link such as `https://learnmagic.ai/skills/qc.zip` (swap `qc` for any skill name in the table above).

### In Claude (claude.ai or the desktop app)

1. Download the skill's ZIP and keep it zipped. It already holds the skill's folder (for example `qc`) with `SKILL.md` inside.
2. In Claude, go to **Customize > Skills**, click **+**, then **Create skill**, then **Upload a skill**, and choose the ZIP.
3. On the Free, Pro or Max plan, code execution has to be switched on in **Settings > Capabilities** for skills to work.
4. Start a new chat and describe the job. Claude uses the skill when it fits, or you can ask for it by name ("use the qc skill").

Working from a copy of this repo instead? Make a ZIP of the skill's folder yourself. The ZIP must contain the folder (for example `qc/`), not just the files inside it.

Source: Claude's help page, [Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude). Menus change from time to time, so if these steps don't match what you see, check that page.

### In Claude Code

1. Download the ZIP and unzip it (or copy the skill's folder from this repo). You get a folder named after the skill, for example `qc`.
2. Move that folder into the `.claude/skills` folder in your home folder, so you end up with, for example:

   ```
   ~/.claude/skills/qc/SKILL.md
   ```

   `~` means your home folder. Make the `skills` folder if it isn't there yet.
3. In Claude Code, type `/qc` to use it, or just describe the job and Claude will pick it when it fits. If it doesn't show up, start a new session.

Source: [Extend Claude with skills](https://code.claude.com/docs/en/skills) in the Claude Code docs.

### With one command

If you're comfortable with a terminal, this installs them for you:

```
npx skills add learnmagic-ai/skills
```

## Safety

Each skill is checked by three independent reviewers before it's published. The skills don't install anything, don't change your settings, don't send your information anywhere, and only look at what you give them. When a skill could change your files, it shows you the changes first and waits for your OK.

As with anything you install, you're welcome to open the `SKILL.md` file and read it first. That's a good habit.

## Licence

MIT. Free to use, change, and share. See [LICENSE](LICENSE).
