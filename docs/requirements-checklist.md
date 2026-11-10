# Requirements checklist

Maps each course requirement to the file or section that proves it. Tick a box only when the evidence exists in the repo.

| # | Requirement | Evidence to produce | Where | Done |
|---|---|---|---|---|
| 1 | Applied LLM use case | One paragraph naming the audience (business users who need trusted data answers) and the problem | README, project document | [ ] |
| 2 | LLM integration | Model/provider named, with why it fits each role (e.g., generator vs. checker); credentials documented as env vars only | README "Model and services" | [ ] |
| 3 | Prompt customization | Prompt files with version history (v1, v2, v3) and a note on what failed and what changed | `prompts/` | [ ] |
| 4 | Context, evaluation, or safety feature | Context: semantic layer. Evaluation: with vs. without layer (ideally two models). Safety: read-only DB, decline rules, source display | `semantic_layer/`, `evaluation/`, `src/` | [ ] |
| 5 | Testing and evaluation | Test-case table with expected behavior (answer / clarify / decline), results, run-to-run consistency, limitations, risks, audience fit | `evaluation/` | [ ] |
| 6 | Documentation, AI use, ethical reflection | Project document, prompt and testing appendix, AI-use log, ethics reflection (privacy, bias, hallucination, misuse, transparency, accessibility, IP, human oversight) | `docs/` | [ ] |

## Submission package (Module 7)

- [ ] GitHub repository (shared with instructor or public), cleaned
- [ ] Project documentation (title, users, problem, model, prompts, safety/evaluation, design, tests, results, limitations, ethics, AI use, future work)
- [ ] Prompt and testing appendix
- [ ] AI use and ethical reflection
- [ ] Recorded presentation and demo (10-15 min: intro of 5 min or less, demo of at least 5 min)

## Module 4 check-in (due date: confirm in Canvas)

- [ ] Application goal, intended users, model/API selected, prompt strategy, AI tools used, progress to date

## Habits that make the evidence easy

- Save every prompt version and a one-line reason for the change, as you go.
- Screenshot or save evaluation runs as you go, not at the end.
- Log AI-tool use in `docs/ai-use-log.md` the same day, including what you rejected or changed.
