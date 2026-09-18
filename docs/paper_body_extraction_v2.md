# Paper Body Extraction Protocol v2

## Purpose
Turn competition papers into evidence-backed knowledge rather than a list of model names.

## Evidence levels
- `E0`: title/index only
- `E1`: official problem/commentary
- `E2`: paper body visible and model statement located
- `E3`: equation/algorithm/parameter/validation evidence located
- `E4`: multiple independent papers or official commentary corroborate the same structural method

Only E2+ may set `historical_usage=true`. E3 is preferred for model-to-problem edges. E4 is preferred for reusable pattern claims.

## Extraction unit
For every paper, extract:
1. problem_id
2. paper_id
3. page range
4. subproblem
5. claim
6. evidence snippet or formula summary
7. model_family
8. model_role
9. assumptions
10. parameters
11. solver
12. objective
13. constraints
14. validation
15. sensitivity/robustness
16. limitations
17. transferable_pattern
18. evidence_level

## Model-role vocabulary
`mechanism_model`, `estimation`, `prediction`, `classification`, `clustering`, `evaluation`, `decision`, `optimization`, `simulation`, `solver`, `preprocessing`, `feature_extraction`, `validation`, `sensitivity_analysis`.

A paper may use one algorithm in several roles; do not collapse roles into the algorithm name.

## Algorithm vs model rule
Examples:
- ODE = mathematical/dynamical model.
- Newton/LM = numerical solver.
- FFT = signal feature extraction / initialization.
- GA/PSO/SA = optimization solver/metaheuristic.
- AHP/TOPSIS = decision/evaluation method.
- Random Forest/XGBoost = predictive model.

## Historical usage vs recommendation
`historical_usage` records what the paper actually used.
`candidate_model` records what the knowledge graph says may fit a structural pattern.
`recommended_model` must be generated only after current Problem + Data + Constraints matching; it must never be copied from historical usage.

## Negative knowledge
Extract explicit failure, instability, high computational cost, assumption violations, poor residual behavior, sensitivity, or model replacement. If absent, write `not_reported`, never infer a failure.

## OCR policy
When official paper pages are image-only:
1. capture page images;
2. OCR text;
3. manually/algorithmically verify equations and symbols;
4. retain page numbers;
5. mark uncertain OCR with `[OCR-UNCERTAIN]`;
6. never silently repair a formula.

## Copyright/data policy
Do not bulk-republish copyrighted paper images or full paper text in this repository. Store metadata, short evidence notes, structured facts, page references, source URLs, and derived tags. Store user-owned or openly licensed full text only when redistribution rights permit.

## Quality gate
A case is `deep_verified` only when:
- problem identity is verified;
- at least one paper body is inspected;
- every historical model edge has page-level evidence;
- solver/model roles are separated;
- at least one validation or limitation field is recorded or explicitly marked `not_reported`.
