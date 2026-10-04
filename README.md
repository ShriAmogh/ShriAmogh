#  Hi, I'm Amogh Arora  

 B.Tech in Artificial Intelligence & Machine Learning @ GGSIPU (2022–2026)  
 AI/ML Engineer | Model Trainer | Python Developer | FastAPI Enthusiast


[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/amogh-arora-b68056259/) 
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=for-the-badge&logo=github)](https://github.com/ShriAmogh) 
[![Email](https://img.shields.io/badge/Email-amogharora99%40gmail.com-red?style=for-the-badge&logo=gmail)](mailto:amogharora99@gmail.com)

---

##  Technical Skills  

- **Languages:** Python, C/C++, SQL  
- **Backend Development:** FastAPI, Django, WebSockets, REST APIs, GraphQL
- **Databases:** SQLite, PostgreSQL, MongoDB  
- **Infra & Dev Tools:** Git, GitHub, VS Code, Docker, Apache Airflow
- **AI & Integrations:** PyTorch, TensorFlow, Keras, Scikit-learn, Pydantic, LangChain, LangGraph, NLP, RAG, MCP, RAGAS, APO, Agentic Frameworks, Transformers,                            LLM APIs
- **Web Scraping:** Puppeteer, Selenium, Headless Browsers, DOM Extraction, OAuth Handshake
- **Core Concepts:** Data Structures & Algorithms, Machine Learning, Deep Learning, DBMS, OS, OOPS  

---

## Live Project 

[**undertow-llm**](https://pypi.org/project/undertow-llm/) -- Published on PYPI

A Python library that wraps any LLM call with a single decorator and gives it semantic caching, rate limiting, retries, fallback chains, and a live observability dashboard, without changing your underlying function.

**'pip install undertow-llm'**

Usage

from undertow_llm import track

Features
- Semantic caching — embeds prompts as vectors and checks cosine similarity before hitting the API; identical or near-identical prompts return cached responses in ~15ms
- Rate limiting — token-bucket limiter per function; blocks and queues requests instead of throwing 429s
- Retries with exponential backoff — automatic retries on transient failures, with configurable jitter to prevent thundering herds
- Fallback chain — if the primary model fails after all retries, cascades through a list of backup functions automatically
- Canary routing — splits a percentage of traffic to an alternate function for safe A/B testing between models
- Policy hook — custom callable that can allow, block, or flag a request before it's sent
- Streaming support — works with generator and async generator responses; logs and caches on stream exhaustion
- Distributed tracing — every call gets a trace_id and span_id; nested @track calls inherit the parent trace
- Live dashboard — run undertow-llm serve to open a FastAPI + Chart.js dashboard showing cache hits, latency, cost, and request logs in real time
- Pluggable storage — SQLite with WAL mode for local dev; PostgreSQL + pgvector + Redis for production


Tech Stack
- Python — core library
- SentenceTransformers (all-MiniLM-L6-v2) — prompt embedding for semantic cache
- SQLite — default local storage with WAL mode
- PostgreSQL + pgvector — production vector storage
- Redis — distributed rate limiting and token bucket state
- FastAPI — observability dashboard backend
- Chart.js — real-time metrics charts in the dashboard
- contextvars — per-thread/task trace context propagation
- ThreadPoolExecutor — background metrics writes, non-blocking

---

##  Experience  

**AI Engineer Intern - Fractics (Feb 2026 - May 2026)**
- Engineered RAG & Ingestion Pipelines: Integrated **MCP servers** into an existing RAG system utilizing **bidirectional WebSocket streaming**, and built an end-to-end RSS ingestion pipeline to extract and enrich structured data on startup funding, acquisitions, and founders.
- Developed Advanced Prompting & Evaluation Systems: Implemented Chain-of-Thought RAG with real-time step-by-step UI streaming, created an **APO system** for prompt refinement using golden datasets, and evaluated the entire pipeline using **RAGAS** with custom domain metrics.
- Built Authenticated Scraping Architecture: Developed a headless Puppeteer scraping pipeline for DOM-level extraction that handles **OAuth login handshakes** to retrieve refresh tokens, enabling automated and authenticated access to gated data sources.

**Agentic AI Engineer Intern - AlgorithmX (Nov 2025 - Dec 2025)**
- Architected a scalable **FastAPI backend** with clean service-repository design, async ORM, and optimized DB interactions, and built a bidirectional WebSocket system enabling session pooling, real-time state sync, and multi-user event pipelines.
- Developed a JSON-to-graph compiler that converted JSON into structured DAG, enabling automated code generation.
- Engineered a multi-agent workflow using Microsoft Autogen, creating custom routing logic and orchestrated agent collaboration for automated code generation and validation.

**Software Developer Intern – Duco Consultancy (Jul 2025 – Aug 2025)**  
- Designed and implemented **MongoDB schema** for scalable data handling.  
- Built & deployed **Express.js backend services**, fully integrated with frontend.  
- Streamlined workflows by loading **large datasets into MongoDB** for scalability.

**Software Engineer Intern – Arya.ag (Jul 2024 – Oct 2024)**  
- Automated **multi-page web data extraction** with Selenium & CSV export.  
- Achieved **96% accuracy** with RandomForest on a multilingual dataset via custom preprocessing + Google Translate API.  
- Applied **image processing (contour-based masking + classification)** to identify crop types.

  

---

##  Projects  

🔹 [**Natural Language to SQL**](https://github.com/ShriAmogh/NL2SQL)  
- Fine-tuned Qwen2.5-1.5B via LoRA adapters on the Spider dataset using Kaggle GPUs, implementing completion-only
loss masking and Cosine scheduling to reduce training loss to 0.02.  
- Implemented 4-bit QLoRA quantization (NF4 precision), successfully reducing model GPU memory footprint by 73% and
optimizing query generation latency during local inference runs. 
- Developed a two-layer validation framework combining local SQLite execution row-matching with a Gemini LLM Judge
to audit query semantics, achieving a 90% execution accuracy (a 10% absolute increase over the base model’s 80%
baseline).

🔹 [**Agentic Retrieval-Augmented Generation System**](https://github.com/ShriAmogh/Memory-Augmented-RAG-with-Semantic-Caching) 
 - Architected a query-aware Hybrid RAG engine combining BM25 lexical retrieval, dense semantic search (Sentence-Transformers), and Cross-Encoder re-ranking (ms-marco-MiniLM-L-6-v2) in ChromaDB, integrating natural language intent and date extraction to eliminate temporal hallucinations.

- Engineered a multi-agent state machine using LangGraph featuring an iterative self-correcting validation loop for Pydantic schema enforcement, a ComparativeAgent for multi-paper synthesis, and an AuditAgent that computes automated hallucination scores (0–100%) for factual grounding.
  
- Developed an end-to-end full-stack AI platform using FastAPI and React (Vite), engineering asynchronous REST endpoints and an interactive UI for live PDF document ingestion, side-by-side literature review matrix rendering, and multi-turn grounded QA.

🔹 [**Industrial-Sensor-ELT-Pipeline**](https://github.com/ShriAmogh/Industrial-Sensor-ELT-Pipeline) 
 - Designed a production-grade ELT pipeline on 10,000 real industrial sensor records (AI4I 2020), implementing a Kimball star
schema with surrogate-key dimensions, staging-layer feature engineering (Kelvin-to-Celsius conversion, mechanical power
derivation, overstrain metrics), and idempotent upserts for full reprocessability.

- Orchestrated the 5-stage pipeline with an Apache Airflow DAG using XCom-based batch lineage, automated retries, and 8
data quality gates (null checks, range validation, referential integrity) with a circuit-breaker pattern that halts downstream
loads on critical failures.

- Built a live FastAPI observability dashboard serving real-time warehouse metrics, an interactive SQL sandbox with preloaded
queries and analytics views computing rolling Z-score anomaly detection across sensor telemetry.


🔹 [**RAGFlow-Django**](https://github.com/ShriAmogh/RAGFlow-Django) 
 - Engineered an end-to-end RAG pipeline with document ingestion, chunking, embedding, vector similarity search, and cross-encoder re-ranking, retrieving top-K high-relevance chunks and integrating an LLM to re-generate grounded, context-aware answers based on re-ranker scores for improved accuracy and reduced hallucinations.

- Designed a scalable Django backend with authentication-protected routes, session-based user isolation, PostgreSQL persistence, and modular app architecture, ensuring clean separation between auth, ingestion, and query workflows.

- Implemented asynchronous processing and scalability patterns using Celery for background indexing, job-based progress tracking, and non-blocking request handling, making the system resilient to heavy document loads and multi-user concurrency.




---

⭐️ From [ShriAmogh](https://github.com/ShriAmogh)  

