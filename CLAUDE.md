# CLAUDE.md — agent-native-lab

Brief for a fresh Claude session opening this repo. Focused on the conventions
that are not obvious from the file alone.

A single-page, **blog-style proposal** arguing that the Vision &amp; Learning Lab
should become *agent-native* — handing routine lab chores to AI agents you talk
to in plain English, with Atlas (the lab inventory agent) as the working proof.
It is shared as a link and meant to be read in a browser.

## What this repo is

- One self-contained file: **`index.html`** — inline CSS, prose only, no build
  step, no dependencies, no JS.
- Served at **https://yubohuangai.github.io/agent-native-lab/** via GitHub Pages
  (source: `main`, root `/`). A push redeploys in ~30–40s.

## Conventions (the load-bearing ones)

### It's a blog essay, not a landing page
Prose-forward, first-person, narrative voice. Spine: lede → (1) friction today →
(2) Atlas as the implemented starting point → (3) a blueprint for the future →
(4) maintenance &amp; growing together, ending on the pull-quote. **Pure text** —
no demo CTAs, no diagrams, no tables. The user removed all of those on purpose;
don't reintroduce them without asking.

### Visual style — match it
Clean "Keynote-white": ~720px reading column, system font, `--accent:#b45309`
(amber), bordered `h2` headings, a left-border `blockquote` for the pull-quote.
Adapted from the `led-sync-panel` reference. Emphasis is **sparse and purposeful**
— bold for the one key takeaway per section, italic for example phrases, key
terms, and the single aphorism. Resist over-emphasizing.

### Deliberate choices — don't "fix" them
- `<meta name="robots" content="noindex,nofollow">` is intentional (hand-shared, not for search).
- The **first** "Atlas" mention links to its Slack workspace invite (`lab-inventory-dev`); other mentions stay plain.
- No individual names in the byline — the audience is the lab broadly.

### Deploy &amp; verify
Edit `index.html` → commit → `git push`; Pages redeploys. Pages/CDN caches, so
**always verify the live URL serves the new version** before claiming done —
poll `curl -s <url> | grep` for a string unique to the change. Commits are
authored as the user (`yubohuangai`); end messages with the Co-Authored-By trailer.

## Related
- [lab-inventory-bot](https://github.com/yubohuangai/lab-inventory-bot) — Atlas's source.
- The Slack announcement for this page is drafted in `visionandlearning` → `#-random`.
  **Draft only — never post to Slack directly.**
