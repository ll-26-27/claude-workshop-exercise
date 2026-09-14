# Where these transcripts come from

**Source:** the Bok Center Learning Lab's *Claude for Faculty* workshop series,
Harvard, **8–10 June 2026**. Three consecutive afternoon sessions, recorded in the
room and auto-transcribed, then diarized by speaker.

| File | Session | Date | Covered |
|---|---|---|---|
| `day_1_transcript.md` | Session 1 | 8 June 2026 | ~13:24–14:53 |
| `day_2_transcript.md` | Session 2 | 9 June 2026 | ~14:03–15:26 |
| `day_3_transcript.md` | Session 3 | 10 June 2026 | full session |

These are **real recordings of real sessions that already happened**, not synthetic
samples. That is the point of the demo: this is what a recording of your own class
looks like once it comes back from transcription — speaker labels, timestamps,
false starts, crosstalk, and all.

## Why the dates are on purpose

The transcripts are dated because the sessions were. That's fine, and it's worth
saying out loud when you run the demo: *"this is a recording of a workshop we ran
in June; yours will look the same."* Faculty read a dated transcript as evidence
the pipeline was run on something real.

What should **not** carry a date is the material in `resources/handouts/` — those
are reference sheets participants take home, and a handout that visibly announces
it was made three months ago reads as stale. Those have been de-dated. Inputs and
outputs of a worked demo are the opposite case: provenance is the feature.

## Named people

The transcripts contain the names of Learning Lab staff and participating faculty,
spoken aloud in the room (instructors, plus faculty asking questions). They were
recorded with the room's knowledge as part of the workshop. If you repoint this
demo at a recording of your own teaching, **check your institution's policy on
recording students before putting a transcript in a repository** — student speech
in a classroom is not the same category as staff speech in a faculty workshop.

## Swapping in your own

Drop any transcript in this folder and run
[`../operations/key-takeaways-prompt.md`](../operations/key-takeaways-prompt.md)
against it. The prompt is written to be source-agnostic: it asks for the title
shape, an italic provenance opening, ten numbered takeaways, and a secondary-points
section, regardless of what the session was about.
