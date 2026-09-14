# Use cases

Portable worked examples. Every one follows the same schema as `_workshop-exercise/`:

```
<use-case>/
  inputs/        what the faculty member brings
  operations/    the prompts, skills, and scripts that do the work
  outputs/       what comes out
  summary.md     situation → move → why it matters
  CLAUDE.md      project instructions
```

Ported from `~/Development/20260903-aiLAB/demos/`, with the `NN-` number prefixes
dropped — the ordering there was a gallery sequence, not a teaching order.

## The five

| Use case | The move | Inputs are | Fit |
|---|---|---|---|
| `class-summarizer` | session recording → Top 10 key takeaways → printable HTML | 3 real diarized workshop transcripts (June 2026) | any |
| `research-helper` | folder of papers → self-contained HTML summaries | 3 real arXiv PDFs + 1 markdown | STEM (swappable) |
| `exam-makeup-generator` | original exam → interview → assembled make-up exam | a real CS20 final, `.tex` + `.pdf` | STEM |
| `handout-formatting` | messy Word/PDF → clean print-ready handouts + answer key | real diff-eq worksheets; a genuinely messy `.docx` | STEM |
| `physics-interactives` | teaching brief → manipulable simulation + lesson plan | a faculty teaching brief | bio/STEM |

**`physics-interactives` now ships three working simulations** in `outputs/sims/`: enzyme kinetics (Michaelis–Menten + inhibition), Hardy–Weinberg, and Lotka–Volterra predator–prey. Each is one self-contained HTML file that opens by double-click, with sliders, linked views, guided prompts, and a visible model-limitations panel. Before this the project shipped skills and templates but no actual sim. See [`physics-interactives/outputs/sims/README.md`](physics-interactives/outputs/sims/README.md) for how the models were checked — including a textbook claim the build caught and corrected.

Each covers a different operation type — summarize, batch-process, author a skill,
reformat, build an artifact — so no two repeat the same move.

## Notes on provenance

**`class-summarizer` inputs are dated on purpose.** They are recordings of real
sessions from 8–10 June 2026, with real participants named in them. See
[`class-summarizer/inputs/README.md`](class-summarizer/inputs/README.md) for the
full provenance note and the caution about recording students rather than staff.

The distinction that matters: a *worked demo* should show where its material came
from — that's the evidence it was run on something real. A *reference handout* in
`resources/handouts/` should not announce that it was made three months ago. The
handouts have been de-dated; these inputs deliberately have not.

**`research-helper` is the easiest swap.** Its three arXiv PDFs are about LLM
context behaviour. Drop in bioRxiv or PubMed PDFs instead and the prompt works
unchanged — nothing in `operations/` is specific to the current papers.

## Not ported

- **`13-smart-text-search`** — ported, then removed. The Dylan-lyrics corpus is a
  genuinely strong demo of close reading at scale, but it is a humanities example
  and the room it would have run in is mostly bio/STEM. Still available at
  `~/Development/20260903-aiLAB/demos/13-smart-text-search`, and in this repo's
  git history.
- **`04-course-preparation`** — excluded.
- **`00-handwritten-student-submissions`** — `inputs/student-work/` is gitignored;
  only a blank synthetic quiz ships, so it's a template rather than a worked run.
  `_workshop-exercise/` already demonstrates the photo→CSV move.
- **`21-text-analysis-and-datavis`** — its `outputs/` are prose *descriptions* of a
  webpage rather than the page itself; the real artifact lives on Vercel.
- The remaining heavy or deployment-dependent demos (`01`, `08`, `11`, `14`–`20`,
  `22`) stay in the aiLAB repo.
