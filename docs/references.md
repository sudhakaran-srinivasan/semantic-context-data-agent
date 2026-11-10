# References

Grouped by what each source contributes. "Read" means a team member read the source itself; "Notes only" means we have only a short summary so far, so do not cite specifics from it until it is read.

## Industry articles

| Source | What it contributes | Status |
|---|---|---|
| Google Cloud, "Expanded semantic model support in Knowledge Catalog" (Oct 29, 2026) | Agents fail for lack of business definitions, not query-writing skill; conflicting definitions shown with their source. The "nearly 4X" figure is Google's own internal benchmark. | Read |
| Anthropic, "How Anthropic enables self-service data analytics with Claude" | Accuracy as a context and verification problem; semantic layer first | Notes only |
| OpenAI, "Inside OpenAI's in-house data agent" and ByteByteGo summary | Layered context, a small set of curated tools, evaluation with question and reference-answer pairs | Notes only |
| Uber, QueryGPT | Small single-purpose steps, domain workspaces, multi-dimension evaluation set | Notes only |
| Pinterest, "Unified Context-Intent Embeddings for Text-to-SQL" | Retrieval by intent; governance signals such as freshness and documentation quality | Notes only |
| Ontologies, Knowledge Graphs, and a Semantic Layer (Dwarampudi) | Define concepts and valid relationships first; the model is the last step | Notes only |
| `agentic-warehouse-analyst` (open source) | Intake gate that can answer, clarify, abstain, or refuse; critic step | Notes only |
| How LangChain Built an Agent-First Data Stack | | Title only |
| Introducing Hex 4.0 | | Title only |
| NVIDIA/auto-ontology | | Title only |
| Ontology-driven observability: knowledge graph at Netflix scale | | Title only |
| Engineering Multi-Agent AI for a 100 GB Data Warehouse (Medium) | | Title only |

## Research papers

| Paper | Finding (from the abstract) |
|---|---|
| [Semantic Layers for Reliable LLM-Powered Data Analytics](https://arxiv.org/pdf/2604.25149) (Rumiantsau, Fokeev) | 99 questions on the Contoso retail dataset, three models, with vs. without a ~4 KB hand-written semantic-layer document: first-attempt pass rates rose 17 to 23 points (to 67.7-68.7% from 45.5-50.5%). Closest precedent to our experiment. |
| [UniDataAgent: An Ontology-Grounded Agent for Enterprise Question-to-Report Automation](https://arxiv.org/pdf/2609.27257) | On 40 real business questions: 95.0% strict accuracy vs. 72.5% for document RAG |
| [EvoOntology: A Self-Evolving Ontology Layer for Data Agents](https://arxiv.org/html/2609.15779v1) | Beat plain ReAct agents and agents with a static semantic layer on three benchmarks |
| [AgentOnto: Ontology-Guided LLM Agents for Enterprise Data Analytics](https://arxiv.org/abs/2610.23317v1) | Stores database, document, and example-task knowledge in an ontology; folds in user-confirmed corrections |
| [Increasing the LLM Accuracy for Question Answering: Ontologies to the Rescue!](https://arxiv.org/pdf/2405.11706) | Ontology checks plus up to three rewrites: ~43% to ~73% correct; ~8% "I don't know" instead of a wrong answer |
| [A Benchmark to Understand the Role of Knowledge Graphs on LLM Accuracy for QA on Enterprise SQL Databases](https://arxiv.org/pdf/2311.07509) | GPT-4: ~16.7% correct with plain SQL vs. ~54.2% with a knowledge graph |
| [Ontology-Constrained Neural Reasoning in Enterprise Agentic Systems](https://arxiv.org/html/2604.00555v5) | 1,800 runs: grounded agents scored significantly higher than ungrounded ones |

Found but not yet read: [Bootstrapping Semantic Layer from Execution for Text-to-SQL](https://arxiv.org/pdf/2606.05634); [Natural Language Access to Domain-Specific Metadata](https://arxiv.org/pdf/2607.18029); [AWS Prescriptive Guidance: Semantic Layer for Agentic AI](https://docs.aws.amazon.com/prescriptive-guidance/latest/semantic-layer-agentic-ai-ontology-reasoning-virtual-knowledge-graph/semantic-layer-agentic-ai-ontology-reasoning-virtual-knowledge-graph.html).

## A note on terminology

Our YAML file is a **semantic layer**. A full **ontology** also models concepts and the relationships between them. We use "ontology-style definitions" where relevant and do not claim a full ontology.

Vendor-reported figures (for example, Google's) are the companies' own claims. We report our own measured results separately.
