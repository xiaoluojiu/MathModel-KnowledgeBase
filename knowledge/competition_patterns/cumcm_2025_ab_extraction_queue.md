# 2025 CUMCM A/B Paper Extraction Queue

## Priority 1 — official displayed papers

| Case | Evidence | Extraction target | Status |
|---|---|---|---|
| 2025A-A196 | Official China University Student Online display | equations, subproblems, model names, optimization, validation | queued |
| 2025B-B060 | Official China University Student Online display | same fields | queued |
| 2025B-B157 | Official China University Student Online display | same fields | queued |

## Extraction protocol

For each paper page image:

1. Preserve page order and source URL.
2. OCR only as an intermediate aid; visually verify mathematical notation.
3. Split content by subproblem.
4. Extract explicit model names separately from inferred mathematical structures.
5. Record model role: core / auxiliary / preprocessing / estimation / optimization / validation.
6. Extract objective and constraints.
7. Extract parameter-fitting method and solver separately.
8. Extract validation and error metrics.
9. Extract sensitivity/robustness statements.
10. Record limitations explicitly stated by the paper.
11. Link every extracted model to its Model Card.
12. Mark unsupported inference as `pattern_inferred`, never `historical_usage`.

## Quality gate

A paper-derived model edge may be promoted to the knowledge graph only when at least one of these is available:

- visible equation/model section in the official displayed paper;
- searchable full text from an authoritative source;
- author/university repository containing the same paper;
- official competition commentary explicitly naming the method.

Search snippets alone do not satisfy the gate.

## 2025 official context

The official 2025 award announcement identifies A as “烟幕干扰弹的投放策略” and B as “碳化硅外延层厚度的确定”. The official paper-display service provides one displayed A paper (A196) and two displayed B papers (B060, B157) in the currently indexed 2025 pages.

## Planned graph edges

`case -> subproblem`

`subproblem -> data_pattern`

`subproblem -> mathematical_structure`

`subproblem -> historical_model`

`historical_model -> model_role`

`historical_model -> solver`

`historical_model -> validation`

`case -> transferable_problem_pattern`

`historical_model -> alternative_model` only when the paper/source provides evidence.
