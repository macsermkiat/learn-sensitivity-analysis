# Sensitivity Analysis for Causal Inference — a short course

A short, interactive course on reading, computing, and critiquing the sensitivity
analyses that appear in clinical real-world-data (RWD) and causal-ML studies — so you
can tell when "robust to unmeasured confounding" is earned, overstated, or missing.

## ▶ Read it as a website

**https://macsermkiat.github.io/learn-sensitivity-analysis/**

> GitHub renders the `.html` files in this repo as *source code*, not as pages. Use the
> link above (GitHub Pages) to actually run the interactive lessons — calculators, a
> contour-plot canvas, and instant-feedback quizzes. It works on mobile.

## Lessons

| # | Lesson | Skill |
|---|--------|-------|
| L01 | [What a Sensitivity Analysis Actually Asks](https://macsermkiat.github.io/learn-sensitivity-analysis/lessons/0001-what-sensitivity-analysis-asks.html) | Read, compute & critique an E-value |
| L02 | [Two Postures: Worst-Case Bounds vs Parametric](https://macsermkiat.github.io/learn-sensitivity-analysis/lessons/0002-two-postures-bounds-vs-parametric.html) | Place any method on the spectrum |
| L03 | [Rosenbaum Γ-Bounds for Matched Designs](https://macsermkiat.github.io/learn-sensitivity-analysis/lessons/0003-rosenbaum-gamma-bounds.html) | Interpret a Γ robustness statement |
| L04 | [The Robustness Value & Contour Plots](https://macsermkiat.github.io/learn-sensitivity-analysis/lessons/0004-robustness-value-and-contour-plots.html) | Read an RV + contour plot (bridges to causal ML) |
| L05 | [Negative Controls: the Design-Based Detector](https://macsermkiat.github.io/learn-sensitivity-analysis/lessons/0005-negative-controls.html) | Judge & interpret negative controls |

Reference: [Glossary](https://macsermkiat.github.io/learn-sensitivity-analysis/reference/glossary.html) — every term defined once, reused verbatim across lessons.

## The five families at a glance

- **Worst-case bounds** — the honest range of effects with *no* assumptions. (L02)
- **E-value** — how strong (risk-ratio scale) must confounding be to overturn it? (L01)
- **Robustness value** — same question on the partial-R² scale; extends to causal ML. (L04)
- **Rosenbaum Γ** — same question for matched designs, on the treatment-odds scale. (L03)
- **Negative controls** — is there a detectable *footprint* of confounding at all? (L05)

Calibration methods (E-value, RV, Γ) quantify *how much*; negative controls *detect*; bounds
state *what's knowable with no assumptions*.

## What you'll be able to do

- Interpret a reported E-value or robustness value and judge whether a result is genuinely
  robust to unmeasured confounding.
- Name the main families of sensitivity analysis and say when each applies.
- Spot the common misuses (treating an E-value as a probability, ignoring the CI-limit
  E-value, reading Γ as the full confounder strength, calling a clean negative control "proof").
- Read an OVB contour / Austen plot and a robustness value from `sensemakr` / `dml.sensemakr`.

## Sources

Lessons cite their sources inline. Core references: VanderWeele & Ding (E-value);
Manski and Richardson et al. (worst-case bounds); Rosenbaum (Γ); Cinelli & Hazlett and
Chernozhukov et al. (robustness value / OVB for causal ML); Lipsitch et al. (negative controls).

## Local use

Everything is self-contained static HTML (inline CSS + JS, no build step):

```bash
open index.html        # macOS — opens the hub in your browser
```
