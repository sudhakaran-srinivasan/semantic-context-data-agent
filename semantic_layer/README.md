# Semantic layer

Certified business definitions the assistant must use. Start from `metrics.example.yaml`, copy it to `metrics.yaml`, and make it match the sample database.

Each metric records: a name, plain-English description, the expression, required filters, source table, and synonyms. Each table records a trust status (certified, staging) and a freshness note. When two metrics could answer the same question, keep both and label each with its source so the assistant can ask which one is meant.
