# Use cases

Five worked examples. Each is a complete project: copy the folder, swap your own
material into `inputs/`, and run the operations against it.

```
<use-case>/
  inputs/        what the faculty member brings
  operations/    the prompts, skills, and scripts that do the work
  outputs/       what comes out
  summary.md     what it is and how it was built
  CLAUDE.md      project instructions Claude reads automatically
```

## The five

| Use case | The move | Inputs are |
|---|---|---|
| [`class-summarizer`](class-summarizer/) | session recording → top ten key takeaways → printable HTML | 3 diarized workshop transcripts |
| [`research-helper`](research-helper/) | a folder of papers → a self-contained HTML summary of each | 3 arXiv PDFs and a markdown paper |
| [`exam-makeup-generator`](exam-makeup-generator/) | an exam → an interview about each question → an assembled make-up exam | a CS20 final, `.tex` and `.pdf` |
| [`handout-formatting`](handout-formatting/) | messy Word and PDF → clean print-ready handouts with an answer key | differential-equations worksheets; a `.docx` with five kinds of delimiter |
| [`physics-interactives`](physics-interactives/) | a teaching brief → a manipulable simulation and a lesson plan around it | a faculty teaching brief |

No two repeat the same move: summarize, batch-process, author a skill, reformat,
build an artifact.

## Where to start

- **Closest to what you already do:** `class-summarizer` or `research-helper`. One
  prompt, a folder of source material, a readable result.
- **If you want to see a skill:** `exam-makeup-generator` and `handout-formatting`
  both package their work as a reusable skill rather than a one-off prompt.
- **If you teach with diagrams:** `physics-interactives` ships three working
  simulations in [`physics-interactives/outputs/sims/`](physics-interactives/outputs/sims/)
  — enzyme kinetics, Hardy–Weinberg, and predator–prey. Each is a single HTML file
  that opens by double-click.

## A note on `class-summarizer`

Its transcripts are recordings of real workshop sessions with participants named in
them. See [`class-summarizer/inputs/README.md`](class-summarizer/inputs/README.md)
before you point it at a recording of your own teaching — student speech in a
classroom is not the same category as staff speech in a faculty workshop.
