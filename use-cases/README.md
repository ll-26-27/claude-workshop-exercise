# Use cases

Portable use-case templates. Every one follows the same schema as this repo's root:

```
<use-case>/
  inputs/        what the faculty member brings
  operations/    the prompts, skills, and scripts that do the work
  outputs/       what comes out
  summary.md     situation → move → why it matters
  CLAUDE.md      project instructions
```

## Candidate pool

Source: `~/Development/20260903-aiLAB/demos/` — 23 demos, all already conforming to
the schema above. Shortlist below; **final five not yet picked.**

### Strongest candidates for a one-day workshop

| Demo | Move it teaches | Why it travels |
|---|---|---|
| `05-class-summarizer` | transcript → Top 10 Key Takeaways → printable handout | Smallest complete loop in the set (15 files). Every faculty member already has recordings. |
| `03-class-processor` | raw course materials → teaching artifacts, one house style | The general case of the above; vision + audio + text in one pipeline. |
| `12-research-helper` | folder of PDFs → self-contained HTML summaries | 19 files, one careful prompt. The clearest "one operation, whole corpus" demo. |
| `13-smart-text-search` | 538 songs → every writer named, with the line | Close reading at corpus scale; the "refuse to grep" discipline is the lesson. |
| `07-exam-makeup-generator` | original exam → interview → candidates → make-up exam | Best skill-authoring example; real CS20 trace. |
| `02-handout-formatting` | messy Word/PDF → clean print-ready handouts + answer key | Pairs directly with `resources/handouts/`. |
| `09-paper-to-teaching-materials` | one paper → a session's worth of material | Concrete, single-source, easy to swap in your own paper. |

### Probably too heavy for one day
`04-course-preparation` (184 files), `11-recentering-academics` (147),
`14-smart-text-search-joyce` (104), `01-admin-email-drafter` (122),
`08-interview-coding`, `15-texts-and-translation`, `10-physics-interactives`.

### Needs a deployed app or API key
`16-oral-exam-practice-bot`, `17-simple-art-history-lecture` (MCP),
`18`–`20` (Next.js sites), `21-text-analysis-and-datavis`, `22-image-API-widget`.
