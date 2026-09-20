# 🛡️ Adaptive Corrective RAG (CRAG) Engine

An enterprise-grade, self-correcting Retrieval-Augmented Generation system that doesn't just blind-retrieve—it **evaluates, refines, and dynamically falls back** to web search when local context is insufficient.

## 🚀 Key Engineering Features
- **Stateful Orchestration:** Built with **LangGraph** to manage conditional logic (`CORRECT`, `INCORRECT`, `AMBIGUOUS` routing paths).
- **Automated Document Grading:** Uses Pydantic and Groq structured outputs (`with_structured_output`) to score chunk relevance mathematically.
- **Sentence-Level Knowledge Refinement:** Strips noisy context down to individual sentences, filtering out irrelevant fluff before generation.
- **Intelligent Web Fallback:** Automatically triggers query rewriting (`TavilySearch`) when internal vector search confidence drops below threshold limits.
