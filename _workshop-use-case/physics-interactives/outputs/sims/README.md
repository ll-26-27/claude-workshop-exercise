# The simulations

Three PhET-style simulations, built with the `/phet-sim` skill in this project.
Each is a **single self-contained HTML file**: double-click it, it opens in Chrome,
it works. No server, no build step, no network access, no dependencies.

| File | Teaches | Misconception it attacks |
|---|---|---|
| [`enzyme-kinetics.html`](enzyme-kinetics.html) | Michaelis–Menten saturation; competitive vs. non-competitive inhibition | "Double the substrate, double the rate." Also: that K<sub>m</sub> is a rate, when it is a concentration. |
| [`hardy-weinberg.html`](hardy-weinberg.html) | What does and does not change allele frequency | "Dominant alleles spread." Also: that selection can purge a recessive allele quickly. |
| [`predator-prey.html`](predator-prey.html) | Lotka–Volterra cycles; reading a phase portrait | "Predator and prey peak together." Also: that something outside the system drives the cycle. |

Each file carries its design record in a header comment — learning goal, target
learner, core misconception, manipulables, what was deliberately left out,
reflection prompts, model limitations, classroom use.

## Shared structure

All three follow the same shape, so a faculty member who learns one can read the
others:

- **Controls** on the left — sliders with live numeric readouts and units, plus
  reset, and play/pause where there is a time axis.
- **Two or three linked views** — move one control and every view updates from the
  same state. This is the pedagogical core: the same fact, shown more than one way.
- **"What to notice"** — directs attention at the link between views.
- **"Try this"** — five guided experiments, phrased as predict-then-check.
- **"Model limitations"** — visible to the student, not hidden in instructor notes.
  Naming what the model gets wrong is part of the artifact.

## Accuracy

Each model was reimplemented independently and the numbers compared against what
the page reports:

- **Enzyme kinetics** — at [S] = 10 µM, K<sub>m</sub> = 15, V<sub>max</sub> = 60:
  occupancy 40%, v = 24.0 µmol/min. Lineweaver–Burk intercepts land at
  1/V<sub>max</sub> and −1/K<sub>m</sub>.
- **Hardy–Weinberg** — at p = 0.5 with no selection: genotype frequencies
  0.250 / 0.500 / 0.250, observed bars sitting exactly on the expectation outlines,
  and a flat trace.
- **Predator–prey** — integrated with RK4 rather than Euler, because Euler spirals
  outward and would make a closed orbit look divergent. After four full periods the
  orbit returns to within 0.1 of where it started. Equilibrium lands at γ/δ, α/β.

One result worth knowing before you teach with it: the predator peak trails the
prey peak by **a quarter of a cycle only near equilibrium**. That figure comes from
linearising the equations about the equilibrium point. On the large boom-and-bust
orbits the simulation shows by default, the measured lag is about 0.175 of a cycle.
The page reports the measured fraction live, and one of the "Try this" prompts
sends students to find the discrepancy themselves.

## Output contract

Verified on all three: no `fetch` or `XMLHttpRequest`, no `<script src=...>`, no
framework, no emoji, design record present, each file under 22 KB.
