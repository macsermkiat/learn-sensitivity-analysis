# Sensitivity Analysis (Causal / RWD) Resources

## Knowledge

- [VanderWeele & Ding (2017), "Sensitivity Analysis in Observational Research: Introducing the E-Value", Annals of Internal Medicine 167:268–274](https://www.acpjournals.org/doi/10.7326/M17-1485)
  THE canonical clinical-RWD reference. Use for: the E-value definition, why a sensitivity
  analysis should accompany every observational causal claim, computing E-values for the
  estimate and for the CI limit nearest the null.
- [Linden, Mathur & VanderWeele (2020), "Conducting sensitivity analysis for unmeasured confounding... using E-values: the evalue package", Stata Journal](https://journals.sagepub.com/doi/10.1177/1536867X20909696)
  Practical how-to + formulas across RR, OR, HR, risk-difference scales. Use for: getting the
  scale conversions right when reading a paper that reports something other than a risk ratio.
- [Cinelli & Hazlett (2020), "Making Sense of Sensitivity: Extending Omitted Variable Bias", JRSS-B](https://carloscinelli.com/files/Cinelli%20and%20Hazlett%20-%20OVB%20for%20IV.pdf)
  Partial-R² / robustness-value framework + sensemakr. Use for: contour plots, benchmarking
  unmeasured confounding against measured covariates, the robustness value.
- [Chernozhukov, Cinelli, Newey, Sharma & Syrgkanis (2026), "Long Story Short: Omitted Variable Bias in Causal Machine Learning", Rev. Econ. & Stat.](https://carloscinelli.com/files/Chernozhukov%20et%20al%20-%20OVB%20for%20ML.pdf)
  Extends OVB sensitivity to flexible/ML estimators (DML). Use for: the causal-ML side of the
  mission — robustness values for ATE/ACD from nonparametric models. Package: dml.sensemakr.
- [sensemakr / dml.sensemakr (Cinelli)](https://github.com/carloscinelli/dml.sensemakr)
  Reference implementation + vignettes. Use for: seeing what the contour plots and robustness
  values actually look like in output.
- [Manski (1990), "Nonparametric Bounds on Treatment Effects", American Economic Review P&P 80(2):319–323](https://ideas.repec.org/a/aea/aecrev/v80y1990i2p319-23.html)
  The origin of assumption-free worst-case bounds (partial identification). Use for: the
  non-parametric posture in L02 — what you can say with NO confounding assumptions, and why
  the bounds are honest but usually wide.
- [Richardson, Hudgens, Gilbert & Fine (2014), "Nonparametric Bounds and Sensitivity Analysis of Treatment Effects", Statistical Science 29(4)](https://pmc.ncbi.nlm.nih.gov/articles/PMC4317325/)
  Accessible bridge connecting Manski bounds to parametric sensitivity analysis. Use for: L02's
  spectrum from "no assumptions / wide" to "calibrated / narrow."
- [Rosenbaum, "Sensitivity Analysis in Observational Studies" (encyclopedia entry, Wharton PDF)](http://www-stat.wharton.upenn.edu/~rosenbap/BehStatSen.pdf)
  Primary, readable treatment of Γ-bounds for matched designs. Use for: the definition of Γ,
  the smoking/lung-cancer worked example, and how the worst-case p-value is computed per Γ.
- [Kang, "Rosenbaum's Sensitivity Analysis (For Matched Pairs)" — UW-Madison course notes](https://pages.cs.wisc.edu/~hyunseung/stat992_sp24/RosenbaumSens.html)
  The accessible secondary explainer the gap called for. Use for: intuition + the `rbounds`/
  `sensitivitymv` R workflow.
- [Lipsitch, Tchetgen Tchetgen & Cohen (2010), "Negative Controls: A Tool for Detecting Confounding and Bias in Observational Studies", Epidemiology 21(3):383–388](https://pmc.ncbi.nlm.nih.gov/articles/PMC3053408/)
  THE negative-control reference. Use for: negative-control outcomes/exposures, the
  U-comparability assumption, and clinical examples (L05).

## Wisdom (Communities)
- _Not yet selected._ Candidates to vet later: Cross Validated (stats.stackexchange.com) for
  interpretation questions; the methods sections of the Society for Epidemiologic Research.
  (User goal is fluency, not production work, so community is lower priority for now.)

## Gaps
- ~~Rosenbaum Γ-bounds plain-language explainer~~ — filled: Rosenbaum Wharton PDF + Kang UW notes.
- ~~Negative-control reference~~ — filled: Lipsitch, Tchetgen Tchetgen & Cohen (2010).
- Optional depth, not yet sourced in detail: Rosenbaum & Silber (2009) **amplification** of Γ
  into a (treatment-leg, outcome-leg) pair — the bridge from Γ to E-value-style two-leg thinking.
- Optional depth: proximal causal inference / control-outcome calibration (Tchetgen Tchetgen)
  for *correcting* (not just detecting) bias with negative controls.
