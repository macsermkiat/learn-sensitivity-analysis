# Notes

## Learner profile
- Domain context: clinical real-world data (RWD). Examples should be clinical where possible
  (drug–outcome associations, transfusion/observational cohorts) — lands harder than abstract.
- Goal is **fluency** (read/critique/reason), not building estimators from scratch.

## PITCH CORRECTION (2026-06-10) — IMPORTANT
- User reported they "can't understand the lessons well" and asked to make them EASIER with
  MORE explanation. The original L01–L05 were built for a "statistically sophisticated, skip
  remedial stats" reader — that pitch was TOO HIGH in practice.
- New house style (now applied to ALL of L01–L05):
  - Lead with a concrete clinical STORY, not the abstract assumption.
  - Unpack EVERY jargon term in plain words the first time it appears (blue `.plain` boxes:
    "In plain words ...").
  - Walk formulas through step by step (`.steps` block), plugging in real numbers.
  - Add a "Quick decoder" definition box at the end recapping every term.
  - Add a one-line hint under each quiz question.
  - Use analogies (e.g. E-value = "how heavy a truck before the bridge falls").
  - Do NOT assume causal-inference fluency; build it. Still no remedial *basic* stats lecture,
    but DO define confounding, ignorability, risk ratio, etc. when first used.

## Teaching preferences (global, from user CLAUDE.md)
- No emojis in any output.
- Prefers concise, concrete material.

## Workspace conventions
- Lessons are self-contained HTML in `lessons/` (inline CSS+JS, no shared assets) — bulletproof
  on GitHub Pages and offline. Open via `open <file>` on macOS.
- Glossary is the spine: every term defined once in `reference/glossary.html`, reused verbatim.
- The workspace is now also a deployable static site (see below). `index.html` is the hub.

## Site / GitHub Pages (added 2026-06-09)
- User wants to push this folder to GitHub and read it as a mobile website via GitHub Pages.
- `index.html` (root) = mobile-first hub: lesson cards + "five families at a glance" map + glossary link.
- Every lesson + the glossary carry a `.lnav` strip (Home / Glossary / prev / next).
- `.nojekyll` present so Pages serves HTML as-is; `.gitignore` ignores `.DS_Store`.
- Push model: user pushes themselves. Suggested = make this folder its own repo
  (`git init` inside it), push, enable Pages from root of the default branch. Do NOT fold it
  into the parent `Project_Chatbot_research` repo's staged changes.

## Curriculum status — full arc L01–L05 now BUILT (2026-06-09)
- L01 E-value · L02 two postures (bounds vs parametric) · L03 Rosenbaum Γ · L04 robustness
  value + contour plot (interactive canvas; bridges to DML/sensemakr) · L05 negative controls.
- This batch was built ahead in one pass at user request ("build everything") — a deliberate
  deviation from the usual one-lesson-per-session pacing, so they can self-study on mobile.
- IMPORTANT: built ≠ learned. `learning-records/` is intentionally still empty — no evidence
  of understanding yet. Write the first record only when the user demonstrates a skill
  (answers a scenario, critiques a real paper), not just because a lesson exists.

## Teaching emphases baked into the lessons (reuse in live tutoring)
- L03's core trap: Γ is the treatment-leg only; don't read it as full confounder strength.
- L04 is THE mission skill (read RV + contour, benchmark vs measured covariates, transfers to ML).
- L05's fluency test: negative controls DETECT a footprint; they don't QUANTIFY bias.

## Review pass (2026-06-10)
- Fixed L03 circular sentence in the smoking example ("smokers more likely to be smokers").
- L01: added OR/HR → RR conversion aside (rare outcome ≈ RR; common outcome √OR) + decoder entry —
  papers mostly report OR/HR, and unconverted common-outcome ORs inflate E-values.
- NEW `reference/checklist.html` — one-page critique checklist (all five families + red flags),
  linked from index and L05; the take-to-a-real-paper capstone.
- Glossary: added ATE, U-comparability, NCO/NCE flavours under Negative control.

## Candidate next moves (post-arc)
- Live critique of a real paper's sensitivity section (the wisdom step — see RESOURCES communities).
- Depth on request: amplification (Γ→(Λ,Δ)); proximal causal inference / control-outcome
  calibration (correcting, not just detecting, with negative controls).
