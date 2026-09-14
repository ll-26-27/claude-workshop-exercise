# The simulations

Three worked PhET-style simulations, built with the `/phet-sim` skill in this
project. Each is a **single self-contained HTML file**: double-click it, it opens
in Chrome, it works. No server, no build step, no network access, no dependencies.

Before these existed the project shipped the skills, the templates, the rubrics and
four background essays — but not one actual simulation. These are what the skill
produces when you run it.

| File | Teaches | Core misconception it attacks |
|---|---|---|
| `enzyme-kinetics.html` | Michaelis–Menten saturation; competitive vs. non-competitive inhibition | "Double the substrate, double the rate." Also: that K<sub>m</sub> is a rate (it is a concentration). |
| `hardy-weinberg.html` | What does and does not change allele frequency | "Dominant alleles spread." Also: that selection can purge a recessive allele quickly. |
| `predator-prey.html` | Lotka–Volterra cycles; reading a phase portrait | "Predator and prey peak together." Also: that something outside the system drives the cycle. |

Each file carries its full design record in a header comment — learning goal,
target learner, core misconception, manipulables, what was deliberately left out,
reflection prompts, model limitations, classroom use.

## Shared structure

All three follow the same shape, so a faculty member who learns one can read the
others:

- **Controls** on the left — sliders with live numeric readouts and units, plus
  reset (and play/pause where there is a time axis).
- **Two or three linked views** — move one control and every view updates from the
  same state object. This is the pedagogical core: the same fact, shown more than
  one way.
- **"What to notice"** — directs attention at the link between views.
- **"Try this"** — five guided experiments, phrased as predict-then-check.
- **"Model limitations"** — visible to the student, not hidden in instructor notes.
  Naming what the model gets wrong is part of the artifact.

## How these were checked

Not just eyeballed. For each, the model was reimplemented independently and the
numbers compared against what the page reports:

- **Enzyme kinetics** — at [S] = 10 µM, K<sub>m</sub> = 15, V<sub>max</sub> = 60:
  occupancy 40%, v = 24.0 µmol/min. Lineweaver–Burk intercepts land at 1/V<sub>max</sub>
  and −1/K<sub>m</sub> as they should.
- **Hardy–Weinberg** — at p = 0.5 with no selection, genotype frequencies are
  0.250 / 0.500 / 0.250 and the observed bars sit exactly on the expectation
  outlines. The trace is flat, which is the entire lesson.
- **Predator–prey** — integrated with RK4 rather than Euler, because Euler spirals
  outward and would make a closed orbit look like a diverging one. Checked: after
  four full periods the orbit returns to (96.4139, 19.9856) → (96.4132, 20.0766).
  Equilibrium lands at γ/δ, α/β = 50, 20. The live page reports period 6.59 and
  lag 1.15, matching an independent calculation of 6.572 and 1.168.

### One correction worth knowing about

The predator–prey sim originally repeated the textbook line that the predator peak
trails the prey peak "by about a quarter of a cycle." Measured on the default
orbit, the lag is **0.175 of a cycle** — not a quarter.

The quarter-cycle figure comes from linearising the equations about the equilibrium
point, and it only holds for small oscillations near that point. On the large
boom-and-bust orbits the simulation shows by default, the lag is closer to a fifth
or a tenth. The page now says so, reports the measured fraction live, and one of
the "Try this" prompts sends students to find the discrepancy themselves.

That is a better lesson than the tidy number, and it is the kind of thing a worked
artifact catches that a slide does not.

## Output contract

Verified on all three: no `fetch` or `XMLHttpRequest`, no `<script src=...>`, no
framework, no emoji, design record present, each file under 22 KB.
