# Resources

Reference material for the workshop. Nothing here is exercise-specific — it's the
stuff participants keep open in another tab, or take home.

- **`glossary/`** — 30 terms (token, context window, harness, skill, context rot,
  data classification…). `glossary-md/` is the source; `glossary-html/` is the
  browsable version (open `glossary-html/index.html`).
- **`handouts/`** — print-ready one-pagers, Learning Lab house style (Inter, white,
  `#c8102e`). Each exists as `.html` (self-contained) and `.pdf`; some also ship the
  `.md` source.

All of it has been de-dated: no "Day 1 / Day 2 / Day 3" framing, no "Summer of
Claude" branding. Kickers are now just the category ("The Frame", "Cheat Card");
footers read **Faculty Workshop · Bok Center · Learning Lab**. Everything is written
to stand alone in a single session, so the same set works across all four workshops.

**MCP is named but not taught.** The how-tos are cut — the concept card, the setup
recipe, the plumbing. What survives is the acknowledgement that the category exists
and that connecting Claude to a live service is a real grant of access. It's more
reach than we want faculty to attempt on two hours of AI training.

## Handouts, and what each is for

| Handout | Use it for |
|---|---|
| `index.html` | Chat / Cowork / Code — the three interfaces, side by side. Orientation. |
| `its-all-text.html` | The conceptual through-line: skills, CLAUDE.md, memory, tools are all just text. |
| `recipe-card.html` | The `inputs/` → `operations/` → `outputs/` heuristic — the shape of `_workshop-exercise/` and every use case. |
| `markdown-cheatsheet.md` | Markdown from zero, plus a one-screen symbol reference. |
| `terminal-refresher.html` | `cd`, `ls`, paths — for anyone touching the CLI. |
| `claude-code-commands-and-concepts.*` | Slash commands + concepts (skills, CLAUDE.md, subagents, plan mode). The best single Claude Code reference in the series. |
| `security-concerns.*` | Prompt injection, excessive agency, data exposure — risks and habits. |
| `what-you-can-make.*` | Gallery of project genres, ordered familiar → unfamiliar. Good closer. |
| `setup-checklists/` | Pre-work: Mac/Windows Claude Code checklists, desktop app, web UI. |

There is **no roadmap/agenda handout** — a "workshop runthrough" doc goes here once
it's written.

## What was changed on the way in

- **Kickers and footers** — day prefixes stripped, "Summer of Claude" dropped.
  PDFs regenerated from the edited HTML via the `handout-house-style` skill's
  `html2pdf.sh`. Page counts unchanged (all single-sheet except
  `what-you-can-make`, which is two-sided).
- **`claude-code-commands-and-concepts`** — MCP concept card removed.
- **`what-you-can-make`** — the "Bots & Connected Tools (MCP, Slack)" row keeps its
  examples but is tagged "not covered today"; its unpacked recipe (`.mcp.json`,
  server setup, best-fit plumbing) is replaced by a short note on what a
  live-service connection actually grants.
- **`index.html`** — the MCP security bullet rewritten as a generic
  connected-services warning, so the safety point survives without teaching MCP.
- **`setup-checklists/code-ide/claude-code-setup.md`** — rewritten out of its
  "Day 2 of the workshop" narrative; the repo tour now describes *this* repo
  (`_workshop-exercise/`, `resources/`, `further-use-cases/`) rather than the
  June repo's `projects/` layout. Clone URLs in the Mac/Windows guides and
  checklists repointed to `claude-workshop-exercise`.
- **Glossary** — two entries (`data-classification`, `claude-cowork`) had "Day 1"
  framing in their *Why it matters* sections; rewritten.

## Deliberately left behind

From the June repos, not ported — available in `~/Development/claude-code-2026*` if wanted:

- **Day-N key-takeaways docs** — transcript-specific to those sessions, not portable.
- **`git-conceptually`** — good, but a one-day workshop rarely gets past `git clone`.
- **`claude-skills` (field guide), `ui-api-mcp`, `mcp-for-faculty`** — Day-4 depth,
  and the last two are MCP.
- **`claude-code-commands.html`** — superseded by `claude-code-commands-and-concepts`.

## Known rough edge

The setup guides embed screenshots as `files.slack.com` links with `pub_secret`
tokens. They render today but aren't durable — worth re-hosting before the images
matter.

Source: `claude-code-20260611/resources/` (most complete of the series), with
`security-concerns` from `claude-code-20260604/`.
