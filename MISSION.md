# Mission: Sensitivity Analysis for Causal Inference (Clinical RWD & Causal ML)

## Why
To read, critique, and reason confidently about sensitivity analyses when they appear in
real-world-data (RWD) causal studies and causal-ML work — so that when a paper, model, or
collaborator claims an effect "survives unmeasured confounding," I can tell whether that
claim is sound, overstated, or missing.

## Success looks like
- Given any clinical RWD paper, I can interpret a reported E-value (or robustness value) and
  judge whether the result is genuinely robust to unmeasured confounding.
- I can name the main families of sensitivity analysis (worst-case bounds, Rosenbaum
  Γ-bounds, E-values, omitted-variable-bias / partial-R² methods, negative controls) and say
  when each applies.
- I can spot the common misuses: treating an E-value as a probability, ignoring the CI-limit
  E-value, conflating "no confounder found" with "no confounding possible."
- I can read an OVB contour / Austen plot and a robustness value from causal-ML output
  (sensemakr / dml.sensemakr) and explain what it implies.

## Constraints
- Goal is **fluency**, not implementation-from-scratch. Prioritise correct interpretation and
  critique over deriving estimators.
- Learner is statistically sophisticated (clinical research, builds ML, works with causal
  models) — skip remedial stats, go straight to the causal-inference framing.
- Short, self-contained lessons. One tangible win each.

## Out of scope (for now)
- Optimization / operations-research sensitivity (shadow prices, LP ranging).
- Financial what-if / tornado modelling.
- Full mathematical derivations of estimators.
