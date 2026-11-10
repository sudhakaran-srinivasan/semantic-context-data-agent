# Semantic Context Layer

**A semantic context layer for trustworthy data answers, with a demo assistant that answers, clarifies, or declines.**

Most AI data assistants can write a query. Far fewer know what your business *means* by "revenue", which tables are certified, or when to say "I can't answer that reliably." This project grounds an LLM in a small, governed semantic layer (certified metric definitions, filters, join paths, synonyms, and data-trust flags) and measures what that grounding changes.

> Status: early design. Nothing below is a result yet. Numbers will be added only after we run the evaluation.

## The idea in one paragraph

A user asks a business question in plain English. Before any query is written, the assistant looks up the question in the semantic layer. It then does one of three things: **answers** (showing the query, the metric definition used, and the source), **asks a clarifying question** (for example, when two definitions of "revenue" conflict), or **declines** (when the data is not certified or fresh enough to trust). We compare the same questions with and without the semantic layer on a small sample database that contains deliberate traps.

## Why this matters

Recent industry and research work points the same way: agent accuracy depends heavily on context and verification, not only on query generation. See [docs/references.md](docs/references.md) for the articles and papers behind this design.

## How it works

```
question
   |
   v
[1] ground      look up metrics, filters, joins, trust flags in the semantic layer
   |
   v
[2] generate    LLM drafts the query using only grounded context
   |
   v
[3] validate    read-only database, statement guard, trust checks
   |
   v
[4] respond     answer + sources  |  clarifying question  |  decline
```

## Repository structure

| Path | Purpose |
|---|---|
| `semantic_layer/` | Certified metric definitions, filters, trust flags (YAML) |
| `data/` | Script that builds a small synthetic sample database (DuckDB) |
| `prompts/` | Versioned prompts with a changelog of what changed and why |
| `src/` | Pipeline code: ground, generate, validate, respond |
| `evaluation/` | Test cases, scoring, results (with vs. without the semantic layer) |
| `tests/` | Unit tests for the validators and guards |
| `docs/` | Requirements checklist, references, workflow, AI-use log, starter issues |

## Setup (will be finalized as code lands)

1. Python 3.11 or newer.
2. `python -m venv .venv && source .venv/bin/activate`
3. `pip install -r requirements.txt`
4. Copy `.env.example` to `.env` and add your own provider values. Credentials are never committed.
5. Build the sample database: see `data/README.md`.

## Model and services

To be documented here once chosen: provider, model name(s), and why each was chosen for its role.

## Known limitations

To be filled in from the evaluation. Early expectations: a hand-written semantic layer must be maintained, results on a small synthetic dataset may not generalize, and silent failures (confident wrong answers) are the main risk to measure.

## Data and privacy

The sample database is fully synthetic. No real customer, employer, or personal data is used anywhere in this repository.

## Project documentation

- [Requirements checklist](docs/requirements-checklist.md)
- [References](docs/references.md)
- [Team workflow](docs/team-and-workflow.md)
- [AI-use log](docs/ai-use-log.md)
- [Starter issues](docs/issues.md)
