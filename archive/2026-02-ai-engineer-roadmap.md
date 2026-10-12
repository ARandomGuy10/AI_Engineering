# 🧠 AI Engineer Roadmap (18 Months) — From Backend Java to Applied AI

**Goal:** Transition from backend Java engineer to Applied AI Engineer — someone who builds production AI applications using LLMs, RAG, agents, and evals (not someone who trains models from scratch).  
**Target Roles:** Applied AI Engineer, AI Platform Engineer, LLM Application Engineer  
**Focus:** Python fluency, LLM APIs, prompt engineering, RAG, agents, evals, and production AI systems.  
**Timeline:** Feb 2026 → Aug 2027 (adjust quarterly based on progress)  
**Learning Style:** YouTube during cardio, courses for structure, projects for hands-on skills

---

## Phase 0: Baseline & Python Bridge (Weeks 1–4)

**Objective:** Bridge from Java to Python and set up your AI development environment.

### ✅ Already Done
- [ ] Backend engineering experience (Java, Spring, REST APIs, SQL, design patterns)
- [ ] Git, Docker, Cloud basics (AWS/GCP)
- [ ] Basic JS/TS/React exposure (from LoveBytes project in 10x roadmap)

### 🐍 Python Fluency Sprint (Critical — New from Gap Analysis)
> Coming from Java, Python is a *very* different world. Invest time here — everything in this roadmap depends on it.

- [ ] **Core Python Patterns for Java Devs**:
  - List comprehensions, generators, decorators, context managers
  - `*args` / `**kwargs`, duck typing, dunder methods
  - 📺 Watch: [Arjan Codes](https://www.youtube.com/@ArjanCodes) — Python best practices, perfect for Java devs
- [ ] **Essential Libraries**:
  - `pydantic` — data validation (think Java DTOs but better)
  - `httpx` / `requests` — HTTP clients
  - `asyncio` — async programming (different from Java's CompletableFuture)
  - Type hints — feels like home for a Java dev, use them everywhere
- [ ] **Environment Setup**:
  - Python 3.11+, `pyenv` for version management
  - `uv` or `poetry` for dependency management (Python's equivalent of Maven/Gradle)
  - VS Code + Python + Pylance extensions
- [ ] 🔬 **Mini-Project**: Rewrite a small Java REST endpoint in Python (FastAPI) — build muscle memory for Python idioms

### 📺 Recommended for Cardio
- [Arjan Codes](https://www.youtube.com/@ArjanCodes) — Python patterns
- [Tech With Tim](https://www.youtube.com/@TechWithTim) — Python basics if needed

---

## Phase 1: ML/DL Fundamentals + LLM APIs (Months 2–5)

**Objective:** Build just enough ML foundation to be dangerous, and start working with LLM APIs immediately.

### 📐 Math Foundations (Just Enough)
- [ ] **Linear Algebra**: Vectors, matrices, dot products, matrix multiplication
  - 📺 Watch: [3Blue1Brown — Essence of Linear Algebra](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab) (full playlist, ~3 hours)
- [ ] **Statistics**: Mean, variance, distributions, Bayes' theorem
- [ ] **Gradient Descent**: Intuition for how models learn (loss functions, backprop at a high level)
  - 📺 Watch: [3Blue1Brown — Neural Networks](https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi)

### 🤖 Intro to Deep Learning
- [ ] **Course** (pick one):
  - [fast.ai — Practical Deep Learning](https://course.fast.ai/) — top-down, practical, Python-first (recommended)
  - Stanford CS231n (more theoretical, good if you want depth)
- [ ] 🔬 **Project**: PyTorch MNIST classifier — build, train, evaluate. Understand the training loop.
- [ ] 🔬 **Project**: Simple sequence model (LSTM or small transformer) — understand sequence processing

### 🧠 Transformers Intuition
- [ ] **Attention Mechanism**: Understand self-attention, multi-head attention, positional encoding
  - 📺 Watch: [3Blue1Brown — Attention in Transformers](https://www.youtube.com/watch?v=eMlx5fFNoYc)
  - 📺 Watch: [Andrej Karpathy — Let's build GPT from scratch](https://www.youtube.com/watch?v=kCc8FmEb1nY)
- [ ] 📖 Read: [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) — the best visual explanation
- [ ] 🔬 **Project**: Code a basic attention block from scratch in PyTorch — understand queries, keys, values

### 🔌 LLM API Development (New — Critical Gap)
> This is 80% of an Applied AI Engineer's daily work. Start early.

- [ ] **Claude API**:
  - Messages API, streaming responses, system prompts
  - Tool use / function calling
  - Structured output (JSON mode)
  - 📖 Read: [Anthropic API Docs](https://docs.anthropic.com/en/docs)
- [ ] **OpenAI API**:
  - Chat completions, function calling, structured outputs
  - Understand the differences from Claude API
- [ ] 🔬 **Project**: Build a CLI chatbot using Claude API
  - Conversation history management
  - System prompt configuration
  - Streaming output to terminal
- [ ] 🔬 **Project**: Build a tool-calling agent using Claude API
  - Define 3+ tools (e.g., web search, calculator, file reader)
  - Implement the tool-calling loop: model requests tool → you execute → return result

### ✍️ Prompt Engineering (New — Foundational Skill)
- [ ] 📖 Course: [Anthropic Prompt Engineering](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview) — read the full guide
- [ ] **Core Techniques**:
  - Zero-shot, few-shot, chain-of-thought
  - Role prompting, XML-structured prompts
  - Constitutional AI principles for safe outputs
- [ ] 🔬 **Project**: Build a prompt eval suite
  - Pick a classification task (e.g., sentiment analysis, intent classification)
  - Write 5 different prompt variants
  - Measure accuracy across 50+ test cases
  - Document which patterns work best and why

### 📺 Recommended for Cardio
- [Andrej Karpathy](https://www.youtube.com/@AndrejKarpathy) — LLM fundamentals
- [AI Jason](https://www.youtube.com/@AIJasonZ) — practical API tutorials, agent builds
- [3Blue1Brown](https://www.youtube.com/@3blue1brown) — math intuition

---

## Phase 2: Transformers Deep Dive + Fine-Tuning + Evals (Months 5–9)

**Objective:** Go deep on how transformers work internally, learn to fine-tune models for specific tasks, and build evaluation systems.

> **Recalibrated from gap analysis:** Less focus on pre-training from scratch and deep RLHF (that's for ML researchers). More focus on fine-tuning via APIs, evals, and applied understanding.

### 🔬 Transformer Internals (Understand, Not Build From Scratch)
- [ ] **nanoGPT**: Work through [Karpathy's nanoGPT repo](https://github.com/karpathy/nanoGPT)
  - Goal: Understand the code, modify it, run experiments — don't just read it
  - 📺 Watch: [Karpathy — Let's reproduce GPT-2](https://www.youtube.com/watch?v=l8pRSuU81PU)
- [ ] 📖 Read: [The Annotated Transformer](https://nlp.seas.harvard.edu/annotated-transformer/) — line-by-line walkthrough
- [ ] **Key Concepts to Understand**:
  - KV caching, Flash Attention, rotary positional embeddings
  - Tokenizer internals (BPE, SentencePiece)
  - Why context window limits exist

### 🎯 Fine-Tuning (Applied, Not Research)
- [ ] **API-Based Fine-Tuning**:
  - OpenAI fine-tuning API — prepare data, fine-tune, evaluate
  - When to fine-tune vs. when to use prompt engineering (most things don't need fine-tuning!)
- [ ] **Open Source Fine-Tuning**:
  - Hugging Face `transformers` + `peft` (LoRA/QLoRA)
  - Fine-tune a small model (Llama/Mistral) on a domain-specific dataset
  - 📺 Watch: [Hugging Face YouTube](https://www.youtube.com/@HuggingFace) — fine-tuning tutorials
- [ ] **RLHF Conceptual Understanding**:
  - Understand reward models, PPO, DPO at a high level
  - Know *when* RLHF matters and what it changes about model behavior
  - 📺 Watch: [Andrej Karpathy — State of GPT](https://www.youtube.com/watch?v=bZQun8Y4L2A) — covers RLHF pipeline
- [ ] 🔬 **Project**: Fine-tune a small open model on a custom dataset
  - Domain: Pick something you know (e.g., Java code review, recipe generation)
  - Compare fine-tuned vs base model on 20+ test cases
  - Document what worked and what didn't

### 📊 Evaluation & Observability (New — Critical Gap)
> Evals are the #1 skill that separates good Applied AI Engineers from mediocre ones.

- [ ] **Eval Frameworks**:
  - Build custom eval harnesses in Python (don't just use off-the-shelf metrics)
  - Metrics: Accuracy, precision, recall, F1 for classification tasks
  - Perplexity, BLEU, ROUGE for generation tasks (know when each applies)
- [ ] **LLM-as-Judge Pattern**:
  - Use a strong model (Claude/GPT-4) to evaluate outputs of weaker models
  - Build rubrics and scoring criteria
  - Understand the limitations (bias, consistency)
- [ ] **Observability Tools**:
  - [LangSmith](https://smith.langchain.com/) — tracing, debugging, evals
  - [Braintrust](https://www.braintrust.dev/) — eval platform
  - Weights & Biases — experiment tracking
- [ ] 🔬 **Project**: Build an end-to-end eval pipeline
  - Golden dataset of 100+ examples
  - Automated scoring (rule-based + LLM-as-judge)
  - Dashboard showing model performance over time

### 📺 Recommended for Cardio
- [Hamel Husain](https://www.youtube.com/@hamelhusain) — evals, production AI
- [Hugging Face](https://www.youtube.com/@HuggingFace) — fine-tuning, model hub
- [Yannic Kilcher](https://www.youtube.com/@YannicKilcher) — paper explanations

---

## Phase 3: RAG, Agents & Production AI (Months 9–14)

**Objective:** Build production-grade RAG systems and multi-step agents. Learn to ship AI features that users actually use.

### 📚 Advanced RAG
- [ ] **Chunking Strategies**:
  - Fixed-size, semantic, recursive, document-aware chunking
  - When to use each — there's no one-size-fits-all
- [ ] **Retrieval Architectures**:
  - Hybrid search: BM25 (keyword) + vector (semantic)
  - Reranking with cross-encoders
  - Query expansion and HyDE (Hypothetical Document Embeddings)
- [ ] **Vector Databases**:
  - Supabase `pgvector` (you already know Supabase!)
  - FAISS (in-memory, great for prototyping)
  - Pinecone or Weaviate (managed, production-ready)
- [ ] **RAG Evals**:
  - Precision / Recall on gold sets
  - Faithfulness (does the answer match the retrieved docs?)
  - Answer relevance (does it actually answer the question?)
- [ ] 🔬 **Project**: Production RAG System
  - Hybrid search (BM25 + pgvector) with reranking
  - Eval dashboard tracking retrieval quality over time
  - API endpoint for querying
  - 📺 Watch: [AI Jason — RAG tutorials](https://www.youtube.com/@AIJasonZ)

### 🤖 Agents at Scale
- [ ] **Agent Patterns** (learn the patterns, not just frameworks):
  - ReAct (Reasoning + Acting)
  - Tool calling with structured outputs
  - Router agents (classify intent → dispatch to specialist)
  - Multi-agent orchestration
- [ ] **Frameworks** (learn 2+, understand trade-offs):
  - LangGraph — stateful multi-step agents
  - Claude native tool use — no framework needed
  - Build one agent with **raw API calls only** — understand what frameworks abstract
- [ ] **Safety & Guardrails**:
  - Input validation, output filtering
  - Content moderation, prompt injection defense
  - JSON schema validation for tool calls
  - 📖 Read: [Anthropic safety best practices](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/mitigate-misuse)
- [ ] 🔬 **Project**: Multi-Agent Workflow
  - 3+ specialized agents collaborating on a task
  - Tool calling with external APIs
  - Error handling, retries, fallback strategies

### 🚀 Deployment & Production Patterns (New — Critical Gap)
> How do you actually ship AI features to production? This is what separates project builders from production engineers.

- [ ] **Streaming**: Server-Sent Events (SSE) for streaming LLM responses to frontend
- [ ] **Cost Management**: Token tracking, prompt caching, model selection based on task complexity
- [ ] **Rate Limiting & Caching**: Cache frequent queries, implement exponential backoff
- [ ] **Error Handling**: Retries with backoff, fallback models, timeout management
- [ ] **A/B Testing**: Test different prompts/models in production
- [ ] **Monitoring**: Track latency, cost, quality metrics in production
- [ ] **Infrastructure**:
  - Prompt caching (Anthropic's prompt caching, Redis for custom)
  - Tracing (LangSmith, OpenTelemetry)
  - Queue-based processing for long-running AI tasks

### 📺 Recommended for Cardio
- [AI Jason](https://www.youtube.com/@AIJasonZ) — RAG and agent tutorials
- [Matt Williams](https://www.youtube.com/@technovangelist) — Local LLMs with Ollama
- [Sam Witteveen](https://www.youtube.com/@samwitteveenai) — Agent deep dives

---

## Phase 4: Portfolio, Polish & Interview Prep (Months 14–18)

**Objective:** Build a portfolio that proves you can ship AI in production. Prepare for interviews.

### 💼 Portfolio Projects (Complete 3+)

#### Project 1: Production RAG System
- Hybrid search + reranking + eval dashboard
- Real data source (technical docs, codebase, knowledge base)
- Deployed with monitoring and cost tracking
- Write-up: Architecture decisions, eval results, lessons learned

#### Project 2: Multi-Agent Workflow
- Multi-tool agent swarm solving a real problem
- Built with both framework (LangGraph) AND raw API approaches
- Safety guardrails, error handling, retry logic
- Write-up: Agent design patterns, failure modes, production considerations

#### Project 3: Fine-Tuned Model + Eval Pipeline
- Fine-tune an open model on domain-specific data (LoRA/QLoRA)
- Compare against base model and API-based models
- Comprehensive eval suite with automated + human evaluation
- Write-up: When to fine-tune vs prompt engineer

### 🏢 Anthropic-Specific Prep
- [ ] Complete [Anthropic Academy](https://anthropic.skilljar.com/) — all courses
- [ ] Build 2+ integrations using Claude API (tool use, structured output, streaming)
- [ ] 📖 Read: Constitutional AI paper, Claude model card, Anthropic safety research
- [ ] Understand: Anthropic's approach to AI safety, RSP (Responsible Scaling Policy)

### 🎯 Interview Prep
- [ ] **Systems Design**:
  - Design a RAG system at scale
  - Design a multi-agent workflow
  - Design an LLM-powered feature for a product
- [ ] **ML Coding**:
  - Implement attention from scratch
  - Build a simple eval pipeline
  - Code a retrieval system
- [ ] **Python Coding**:
  - LeetCode-style but in Python (coming from Java, practice Python idioms)
  - `asyncio`, data structures, string manipulation
- [ ] **Behavioral / Safety**:
  - AI safety scenarios and ethical considerations
  - Production failure stories and lessons learned

### 📺 Recommended for Cardio
- [AI Explained](https://www.youtube.com/@aiexplained-official) — stay current on the field
- [Anthropic](https://www.youtube.com/@anthropic-ai) — company culture, research talks

---

## 📚 Resources — Master List

### 📺 YouTube Channels
| Channel | Best For | Phase |
|---------|----------|-------|
| [3Blue1Brown](https://www.youtube.com/@3blue1brown) | Math, neural nets, attention | Phase 1 |
| [Andrej Karpathy](https://www.youtube.com/@AndrejKarpathy) | LLM fundamentals, GPT internals | Phase 1–2 |
| [Arjan Codes](https://www.youtube.com/@ArjanCodes) | Python for Java devs | Phase 0 |
| [AI Jason](https://www.youtube.com/@AIJasonZ) | Practical RAG, agents, API tutorials | Phase 1–3 |
| [Hamel Husain](https://www.youtube.com/@hamelhusain) | Evals, production AI | Phase 2–3 |
| [Hugging Face](https://www.youtube.com/@HuggingFace) | Fine-tuning, model hub | Phase 2 |
| [AI Explained](https://www.youtube.com/@aiexplained-official) | Staying current | All phases |
| [Anthropic](https://www.youtube.com/@anthropic-ai) | Claude, safety, company | Phase 4 |

### 📖 Courses
- [fast.ai — Practical Deep Learning](https://course.fast.ai/)
- [Anthropic Academy](https://anthropic.skilljar.com/)
- [LangChain Academy](https://academy.langchain.com/)
- [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course)

### 📄 Key Reads
- [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/)
- [Anthropic Prompt Engineering Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)
- [Attention Is All You Need (paper)](https://arxiv.org/abs/1706.03762)
- [Constitutional AI (paper)](https://arxiv.org/abs/2212.08073)

### 🔗 Repos & Tools
- [nanoGPT](https://github.com/karpathy/nanoGPT) — Build GPT from scratch
- [InterviewReady AI Resources](https://github.com/InterviewReady/ai-engineering-resources)
- [LangSmith](https://smith.langchain.com/) — Tracing & evals
- [Anthropic Careers](https://www.anthropic.com/careers) — Job listings

---

## 📈 Progress Tracking

| Phase | Timeline | Focus | Key Deliverable |
|-------|----------|-------|----------------|
| Phase 0 | Month 1 | Python + Setup | FastAPI mini-project + dev environment |
| Phase 1 | Months 2–5 | ML Fundamentals + APIs | CLI chatbot + tool-calling agent + prompt eval suite |
| Phase 2 | Months 5–9 | Transformers + Fine-tuning + Evals | Fine-tuned model + eval pipeline |
| Phase 3 | Months 9–14 | RAG + Agents + Production | Production RAG system + multi-agent workflow |
| Phase 4 | Months 14–18 | Portfolio + Interviews | 3+ portfolio projects + interview readiness |
