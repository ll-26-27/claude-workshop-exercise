# Resources

Reference material. Nothing here is tied to the exercise — it's what you keep open
in another tab, or take home.

## glossary/

30 terms: token, context window, harness, skill, CLAUDE.md, context rot, data
classification, and the rest.

- [`glossary-md/`](glossary/glossary-md/) — the source, one file per term
- [`glossary-html/index.html`](glossary/glossary-html/index.html) — browsable version

## handouts/

Print-ready one-pagers. Each exists as a self-contained `.html` and a `.pdf`; some
also ship the `.md` source.

| Handout | What it covers |
|---|---|
| [`index.html`](handouts/index.html) | Chat / Cowork / Code — the three interfaces side by side |
| [`its-all-text.html`](handouts/its-all-text.html) | Skills, CLAUDE.md, memory, tools — all of it is text |
| [`recipe-card.html`](handouts/recipe-card.html) | The `inputs/` → `operations/` → `outputs/` heuristic |
| [`markdown-cheatsheet.md`](handouts/markdown-cheatsheet.md) | Markdown from zero, plus a one-screen symbol reference |
| [`terminal-refresher.html`](handouts/terminal-refresher.html) | `cd`, `ls`, paths |
| [`claude-code-commands-and-concepts.html`](handouts/claude-code-commands-and-concepts.html) | Slash commands, and the concepts behind them |
| [`security-concerns.html`](handouts/security-concerns.html) | Prompt injection, excessive agency, data exposure |
| [`what-you-can-make.html`](handouts/what-you-can-make.html) | A gallery of project genres, familiar to unfamiliar |

## handouts/setup-checklists/

Installing Claude Code, by route.

- [`code-ide/`](handouts/setup-checklists/code-ide/) — terminal and VS Code. Printable
  checklists for [Mac](handouts/setup-checklists/code-ide/checklists/claude-code-mac-checklist.html)
  and [Windows](handouts/setup-checklists/code-ide/checklists/claude-code-windows-checklist.html),
  plus a longer guide explaining each step.
- [`desktop-app/`](handouts/setup-checklists/desktop-app/) — the desktop app
- [`webui/`](handouts/setup-checklists/webui/) — claude.ai in a browser

## Rebuilding a handout

Edit the `.html`, then regenerate the PDF:

```bash
~/.claude/skills/handout-house-style/scripts/html2pdf.sh handouts/<name>.html
```
