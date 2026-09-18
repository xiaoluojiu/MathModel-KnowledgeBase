# Competition Case Knowledge Methodology

Competition papers are used as **case evidence**, not as templates to copy.

## What is extracted

For each problem/case, the knowledge base records:

1. Problem type and subproblem structure.
2. Data modality and observable patterns.
3. Modeling roles: prediction, evaluation, optimization, simulation, mechanism, etc.
4. Candidate model families and their role in the solution pipeline.
5. Evidence that makes a model plausible: assumptions, data structure, constraints, objective, validation requirements.
6. Reasonable alternatives and model-combination patterns.
7. Lessons that can improve AI model retrieval.

## What is not copied

The repository should not mirror complete copyrighted winning papers. It stores structured metadata, concise derived modeling knowledge, and links to the authoritative source pages. When a source permits redistribution, the license/permission should be recorded before storing the full document.

## Evidence levels

- `official_problem`: official contest problem/data page.
- `official_result`: official award/result page.
- `official_paper`: organizer-hosted winning paper or official paper archive.
- `secondary_analysis`: independently published analysis.
- `inferred_pattern`: knowledge-base inference; must not be presented as an official description of a team's method.

## AI retrieval rule

A competition case is evidence for a **problem-model relationship**, not proof that the same model is optimal for a new problem. The AI must re-check the new problem's data, assumptions, objective, constraints and validation requirements before transferring a pattern.
