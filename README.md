# Claude workshop materials

This repository contains materials for a one-day workshop on using Claude Code
with files and folders. It includes one workshop use case, five further use
cases, and reference handouts from the Bok Center Learning Lab.

You do not need to understand every file. Start with the main use case during
the workshop, then choose a further use case that is close to your own work.

## Repository guide

| Folder | Contents | Start here |
|---|---|---|
| [`_workshop-use-cases/`](_workshop-use-cases/) | The shared workshop activity. It converts photos of table responses into a CSV file and an interactive chart. | [`README.md`](_workshop-use-cases/README.md) |
| [`further-use-cases/`](further-use-cases/) | Five additional examples involving transcripts, research papers, exams, handouts, and interactive simulations. | [`README.md`](further-use-cases/README.md) |
| [`resources/`](resources/) | A glossary, setup guides, and workshop handouts. | [`README.md`](resources/README.md) |

## Common folder structure

Most examples use three folders:

```text
inputs/       source files such as photos, transcripts, papers, or documents
operations/   prompts, skills, and scripts used to process the source files
outputs/      example results produced from the source files
```

The committed outputs show what a completed run looks like. You can inspect
them without running any code. If you run an example with your own material,
keep the original files in `inputs/` and write new files to `outputs/`.

## Setup

If Claude Code is not installed, use the guides in
[`resources/handouts/setup-checklists/`](resources/handouts/setup-checklists/).
The folder contains instructions for macOS, Windows, the desktop app, and the
web interface.

## Suggested path through the workshop

1. Review the [`inputs` / `operations` / `outputs` handout](resources/handouts/project-plan/project-plan.html).
2. Complete the [workshop use case](_workshop-use-cases/README.md).
3. Browse the [further use cases](further-use-cases/README.md).
4. Open one use case and read its `summary.md` before inspecting its files.
