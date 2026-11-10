# Starter issues (copy into GitHub Issues)

## Setup
- [ ] Create repo, add collaborators and the instructor (or make public)
- [ ] Add GitHub Projects board with columns: Backlog, In progress, Review, Done
- [ ] Confirm model/provider and budget; document in README

## Data (data/)
- [ ] Write seeded script that builds the sample DuckDB database
- [ ] Add deliberate traps: cancelled orders, a staging table, two conflicting definitions of the same metric
- [ ] Document the schema and each trap

## Semantic layer (semantic_layer/)
- [ ] Define certified metrics (name, description, expression, filters, source table, synonyms)
- [ ] Add trust flags per table (certified, staging, freshness)
- [ ] Add one deliberate metric conflict with sources shown

## Pipeline (src/, prompts/)
- [ ] Grounding step: match question to metrics/tables
- [ ] Generation prompt v1 with structured output (answer / clarify / decline)
- [ ] Validation: read-only connection, statement guard, trust checks
- [ ] Response formatting: show query, definition used, and source

## Evaluation (evaluation/)
- [ ] Write 20-30 test questions with expected behavior and expected answer
- [ ] Build harness: with vs. without semantic layer
- [ ] Run each case multiple times to measure consistency
- [ ] Compare two models if budget allows

## Safety (src/, tests/)
- [ ] Unit tests for the statement guard
- [ ] Prompt-injection test cases

## Docs and demo
- [ ] Project document, prompt and testing appendix, AI-use and ethics reflection
- [ ] Module 4 check-in
- [ ] Record presentation and demo
