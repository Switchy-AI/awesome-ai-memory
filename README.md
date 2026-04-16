# Awesome AI Memory [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of tools, papers, frameworks, and patterns for building memory into AI systems — agents, chatbots, copilots, and multi-model products.

Memory is the bottleneck for useful AI. Models forget, sessions reset, and every new product rebuilds state from scratch. This list tracks the people, code, and ideas actually moving the space forward.

Maintained by the team at [Switchy](https://switchy.build). PRs welcome — see [contributing](#contributing).

---

## Contents

- [Foundational papers](#foundational-papers)
- [Memory frameworks & libraries](#memory-frameworks--libraries)
- [Vector databases](#vector-databases)
- [Knowledge graphs for AI](#knowledge-graphs-for-ai)
- [Agent memory systems](#agent-memory-systems)
- [Long-context techniques](#long-context-techniques)
- [Evaluation & benchmarks](#evaluation--benchmarks)
- [Retrieval augmented generation](#retrieval-augmented-generation)
- [Commercial memory APIs](#commercial-memory-apis)
- [Blog posts & essays](#blog-posts--essays)
- [Talks & videos](#talks--videos)
- [Related awesome lists](#related-awesome-lists)
- [Contributing](#contributing)

---

## Foundational papers

Papers that shaped how practitioners think about memory in LLM systems.

- [MemGPT: Towards LLMs as Operating Systems](https://arxiv.org/abs/2310.08560) — Packer et al., 2023. OS-inspired memory hierarchy with paging between context and external storage.
- [Generative Agents: Interactive Simulacra of Human Behavior](https://arxiv.org/abs/2304.03442) — Park et al., 2023. Reflection, planning, and memory streams with recency/importance/relevance scoring.
- [Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks](https://arxiv.org/abs/2005.11401) — Lewis et al., 2020. The original RAG paper.
- [Lost in the Middle: How Language Models Use Long Contexts](https://arxiv.org/abs/2307.03172) — Liu et al., 2023. Why dumping everything into context fails.
- [Reflexion: Language Agents with Verbal Reinforcement Learning](https://arxiv.org/abs/2303.11366) — Shinn et al., 2023. Self-reflection as a memory mechanism.
- [Think-in-Memory: Recalling and Post-thinking Enable LLMs with Long-Term Memory](https://arxiv.org/abs/2311.08719) — Liu et al., 2023.

## Memory frameworks & libraries

Open-source libraries you can install today.

- [LangChain Memory](https://python.langchain.com/docs/modules/memory/) — classic buffer, summary, and vector-backed memory for LangChain chains and agents.
- [LlamaIndex Memory](https://docs.llamaindex.ai/) — chat memory buffers, vector memory, and composable memory modules.
- [Letta (formerly MemGPT)](https://github.com/letta-ai/letta) — stateful agents with hierarchical memory management.
- [Mem0](https://github.com/mem0ai/mem0) — self-improving memory layer for personalized AI.
- [Zep](https://github.com/getzep/zep) — long-term memory store with fact extraction and temporal knowledge graphs.
- [Cognee](https://github.com/topoteretes/cognee) — memory for AI agents with knowledge graphs + vector search.
- [Motorhead](https://github.com/getmetal/motorhead) — server for LLM chat history and context.

## Vector databases

The retrieval substrate under most memory systems.

- [pgvector](https://github.com/pgvector/pgvector) — Postgres extension. Start here if you already run Postgres.
- [Qdrant](https://github.com/qdrant/qdrant) — Rust-based, strong filtering, self-hostable.
- [Weaviate](https://github.com/weaviate/weaviate) — built-in hybrid search and modules for embeddings.
- [Milvus](https://github.com/milvus-io/milvus) — scalable, cloud-native.
- [Chroma](https://github.com/chroma-core/chroma) — developer-experience focused, easy local dev.
- [LanceDB](https://github.com/lancedb/lancedb) — serverless, embedded, columnar format.
- [Pinecone](https://www.pinecone.io/) — managed, widely used in production.

## Knowledge graphs for AI

Structured memory beyond chunks and vectors.

- [Graphiti](https://github.com/getzep/graphiti) — temporal knowledge graphs for agent memory.
- [LightRAG](https://github.com/HKUDS/LightRAG) — graph-augmented RAG that unifies retrieval with entity relations.
- [Neo4j + LLMs](https://neo4j.com/labs/genai-ecosystem/) — patterns for LLM-backed graph construction.
- [KùzuDB](https://github.com/kuzudb/kuzu) — embedded graph database.

## Agent memory systems

Production patterns for long-running agents.

- [AutoGPT memory backends](https://github.com/Significant-Gravitas/AutoGPT) — reference for how autonomous agents handle state.
- [CrewAI memory](https://docs.crewai.com/concepts/memory) — short-term, long-term, and entity memory for multi-agent crews.
- [Letta architecture docs](https://docs.letta.com/concepts/memgpt) — walkthrough of the hierarchical memory approach.

## Long-context techniques

When you want to lean on context instead of (or alongside) retrieval.

- [Anthropic — Contextual Retrieval](https://www.anthropic.com/news/contextual-retrieval) — prepending chunk-specific context before embedding.
- [Prompt caching (Anthropic, OpenAI, Google)](https://docs.anthropic.com/en/docs/build-with-claude/prompt-caching) — cheap repeated context.
- [RAPTOR: Recursive Abstractive Processing for Tree-Organized Retrieval](https://arxiv.org/abs/2401.18059) — hierarchical summary trees.

## Evaluation & benchmarks

You can't improve what you don't measure.

- [LoCoMo](https://github.com/snap-research/locomo) — long-term conversational memory benchmark.
- [LongMemEval](https://github.com/xiaowu0162/LongMemEval) — comprehensive benchmark of long-term memory.
- [MemoryBench](https://github.com/Switchy-AI/memory-bench) — open reproducible benchmark for agent memory systems (maintained by Switchy).
- [RULER](https://github.com/hsiehjackson/RULER) — long-context benchmark beyond needle-in-a-haystack.

## Retrieval augmented generation

RAG is adjacent to memory — usually both are needed.

- [RAG survey](https://arxiv.org/abs/2312.10997) — Gao et al., 2023.
- [ColBERT](https://github.com/stanford-futuredata/ColBERT) — late-interaction retrieval.
- [GraphRAG (Microsoft)](https://github.com/microsoft/graphrag) — graph-based RAG with entity summaries.

## Commercial memory APIs

Managed services for teams that don't want to rebuild this layer.

- [Switchy](https://switchy.build) — shared memory across 450+ models, four-layer architecture, drop-in API.
- [Mem0 Platform](https://mem0.ai) — managed memory with personalization focus.
- [Zep Cloud](https://www.getzep.com) — memory + knowledge graphs as a service.
- [Pinecone Assistants](https://www.pinecone.io/product/assistant/) — knowledge base + assistant abstraction.

## Blog posts & essays

Practitioner writing that shaped the field.

- [Lilian Weng — LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/) — the agent memory taxonomy almost everyone cites.
- [Andrej Karpathy — State of GPT](https://www.youtube.com/watch?v=bZQun8Y4L2A) — context engineering as a first-class skill.
- [Simon Willison — Prompt injection and LLM memory](https://simonwillison.net/tags/prompt-injection/) — security implications.
- [Chip Huyen — RAG and retrieval in production](https://huyenchip.com/2024/07/25/genai-platform.html).

## Talks & videos

- [MemGPT: Building LLMs as Operating Systems — Charles Packer](https://www.youtube.com/results?search_query=memgpt+charles+packer)
- [Harrison Chase on LangChain Memory](https://www.youtube.com/@LangChain)

## Related awesome lists

- [awesome-llm](https://github.com/Hannibal046/Awesome-LLM)
- [awesome-agents](https://github.com/kyrolabs/awesome-agents)
- [awesome-rag](https://github.com/frutik/Awesome-RAG)
- [awesome-langchain](https://github.com/kyrolabs/awesome-langchain)

---

## Contributing

PRs welcome. A few ground rules:

1. **One link per PR** unless entries are tightly related.
2. **No self-promotion without substance.** Commercial tools are fine if they solve a real problem — say what the tool does and why it belongs.
3. **Prefer primary sources.** Link the paper, repo, or doc — not a third-party summary.
4. **Keep the one-line description honest.** No marketing language. Describe what the thing does.
5. **Alphabetize within sections** when order doesn't otherwise matter.

See [contributing.md](contributing.md) for the full guide.

---

## License

[CC0](LICENSE) — public domain. Copy, fork, and remix freely.
