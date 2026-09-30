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

## How to install

### In Claude (claude.ai or the desktop app)

1. Download the skill's folder and turn it into a ZIP file. The ZIP should contain the skill's folder itself (for example the `qc` folder, with `SKILL.md` inside it).
2. In Claude, go to **Customize > Skills**, click **+**, then **+ Create skill**, then **Upload a skill**, and upload the ZIP.
3. If you're on the Free, Pro or Max plan, code execution needs to be switched on in **Settings > Capabilities** for skills to work.

Source: Claude's help page, [Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude). Menus change from time to time, so if these steps don't match what you see, check that page.

### In Claude Code

Copy the skill's folder into your personal skills folder, so you end up with, for example:

```
~/.claude/skills/qc/SKILL.md
```

(`~` means your home folder.) The skill is then available in all your projects. You can use it by typing `/qc`, or Claude will use it when it fits.

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
