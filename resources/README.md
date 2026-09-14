# Workshop resources

This folder contains reference material for the workshop. The files can be read
independently of the group exercise and use cases.

## Glossary

The glossary defines 30 terms used in the workshop, including *token*, *context
window*, *agent*, *skill*, *prompt injection*, and *data classification*.

- [`glossary/glossary-md/`](glossary/glossary-md/) contains the Markdown source,
  with one file per term.
- [`glossary/glossary-html/index.html`](glossary/glossary-html/index.html) opens
  the browsable HTML version.

## Handouts

Most handouts are available as a standalone HTML file and a PDF. Some also have
Markdown source.

| Handout | Topic |
|---|---|
| [`index.html`](handouts/index.html) | Comparison of the Chat, Cowork, and Code interfaces |
| [`its-all-text.html`](handouts/its-all-text.html) | How prompts, project instructions, memory, skills, and tool definitions are stored as text |
| [`recipe-card.html`](handouts/recipe-card.html) | The `inputs/` → `operations/` → `outputs/` project structure |
| [`markdown-cheatsheet.md`](handouts/markdown-cheatsheet.md) | Basic Markdown syntax |
| [`terminal-refresher.html`](handouts/terminal-refresher.html) | Basic terminal commands and file paths |
| [`claude-code-commands-and-concepts.html`](handouts/claude-code-commands-and-concepts.html) | Claude Code commands and related concepts |
| [`security-concerns.html`](handouts/security-concerns.html) | Prompt injection, excessive permissions, and data exposure |
| [`what-you-can-make.html`](handouts/what-you-can-make.html) | Examples of projects that can be built with Claude Code |

## Setup guides

The [`handouts/setup-checklists/`](handouts/setup-checklists/) folder contains:

- `code-ide/`: terminal and VS Code setup for macOS and Windows
- `desktop-app/`: desktop application setup
- `webui/`: browser setup

The `code-ide/checklists/` folder contains shorter printable checklists.

## Rebuilding a handout PDF

Edit the handout's HTML source, then use the workshop's HTML-to-PDF script:

```bash
~/.claude/skills/handout-house-style/scripts/html2pdf.sh handouts/<name>.html
```

This command depends on a local skill outside this repository. If that skill is
not installed, the existing HTML and PDF files can still be used as provided.
