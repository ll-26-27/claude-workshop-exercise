# The workshop exercise

The thing the room actually does. Photos of each table's hand-drawn AI-comfort
spectrum go in; a coded CSV and an interactive chart come out.

```
_workshop-exercise/
  inputs/      12 photos, one per table (.HEIC straight off a phone)
  operations/  01-photos-to-csv.md · 02-csv-to-visualization.md · extract.py
  outputs/     ai_comfort_spectrum.csv · ai_comfort_spectrum.html
```

This is the `inputs/` → `operations/` → `outputs/` shape in its simplest form, and
it is the same shape every project in [`../further-use-cases/`](../further-use-cases/) follows. The
[recipe-card handout](../resources/handouts/recipe-card.html) is about this layout.

## Running it

Paths inside `operations/` are written relative to **this folder**, so work from
here rather than from the repo root:

```bash
cd _workshop-exercise
python operations/extract.py prep  inputs/ work/
python operations/extract.py score work/ outputs/ai_comfort_spectrum.csv
```

`work/` is scratch space for the converted JPEGs and is gitignored.

Or skip the script entirely and hand Claude
[`operations/01-photos-to-csv.md`](operations/01-photos-to-csv.md) — the prompt does
the same job, and the "optional fast path" note in it explains which steps the
script covers deterministically.

## Why the leading underscore

It sorts to the top, above `resources/` and `further-use-cases/`, so the first thing
anyone sees when they open the repo is the thing they are here to do.
