# Workshop exercise: photos to a chart

In this exercise, each table places task cards on a 1–10 scale showing how
comfortable the group is with using AI for each task. The repository contains
12 photos of those arrangements.

The exercise produces two files:

- `outputs/ai_comfort_spectrum.csv`: one row for each card that can be read and
  placed on the scale
- `outputs/ai_comfort_spectrum.html`: an interactive chart built from the CSV

Completed examples of both files are included.

## Folder contents

```text
inputs/      original HEIC photos, one per table
operations/  two task prompts and a supporting image-processing script
outputs/     completed CSV and HTML examples
```

Run commands from this folder because the prompts and scripts use paths that
are relative to it:

```bash
cd _workshop-exercise
```

## Option 1: use the prompt

Give Claude [`operations/01-photos-to-csv.md`](operations/01-photos-to-csv.md).
The prompt explains how to normalize filenames, detect cards, assign positions,
and write the CSV. Review the detected cards and any exclusions before accepting
the result.

After the CSV is complete, give Claude
[`operations/02-csv-to-visualization.md`](operations/02-csv-to-visualization.md)
to create the HTML chart.

## Option 2: use the supporting script

The script automates image conversion, card detection, and position scoring. It
does not read the text on the cards or decide whether every detected object is a
valid card. Those steps still require review.

```bash
python operations/extract.py prep inputs/ work/
python operations/extract.py detect work/
```

Open the contact sheets in `work/sheets/`, identify the numbered cards, and
record the labels in `work/labels.json` as instructed by the script. Then run:

```bash
python operations/extract.py score work/ outputs/ai_comfort_spectrum.csv
```

The temporary `work/` folder is excluded from Git.

## What to check

- Every included label matches one of the 18 tasks listed in the first prompt.
- A task does not appear twice for the same group.
- The leftmost and rightmost included cards receive scores of 1 and 10.
- Unclear photos, duplicate group numbers, and excluded cards are reported for
  human review.
