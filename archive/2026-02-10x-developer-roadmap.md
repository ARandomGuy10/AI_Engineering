# 🚀 10x Developer Roadmap (3 Months) — Using Claude Code & AI Agents

**Goal:** Master Claude Code, MCP, sub-agents, and AI-first workflows to 10x your productivity as a backend engineer. Build LoveBytes (React/Supabase app) as a side project.  
**Focus:** Practical leverage. Use AI for every step — from thinking to shipping.  
**Stack:** React, TypeScript, Supabase, Claude Code CLI, Clerk Auth.  
**Start Date:** Feb 2026

---

## 📅 Month 1: LLM Fundamentals, Prompt Engineering & Claude Code Mastery

### 🧠 Week 1: Practical LLM Fundamentals + Prompt Engineering

**Objective:** Understand how LLMs work (tokens, context, attention) and learn the prompting patterns that make AI coding assistants 10x more useful.

#### LLM Fundamentals
- [ ] **Tokens & Cost**: LLMs read tokens (~750 words ≈ 1k tokens). Understand pricing per model.
  - 🔬 Lab: Use [Tiktokenizer](https://tiktokenizer.vercel.app/) to tokenize your Java stack traces and code snippets — notice how verbose code costs more.
- [ ] **Context Windows**: Think of it as "short-term memory" — stuffing too many files degrades output quality.
  - 📺 Watch: [Andrej Karpathy — Intro to LLMs](https://www.youtube.com/watch?v=zjkBMFhNj_g) (Chapters 1–3)
- [ ] **Transformers Intuition**: Understand the attention mechanism at a high level — why LLMs can "focus" on relevant code.
  - 📺 Watch: [3Blue1Brown — Attention in Transformers](https://www.youtube.com/watch?v=eMlx5fFNoYc)
- [ ] **Embeddings Teaser**: Semantic search via vector embeddings (Cosine Similarity). This will become important in your AI Engineer roadmap.

#### Prompt Engineering (Critical — The #1 Leverage Skill)
- [ ] **Structured Prompting Patterns**:
  - Few-shot prompting (provide examples of desired output)
  - Chain-of-thought (ask the model to reason step-by-step)
  - System prompts & role setting
  - XML-tagged instructions (Claude's preferred format)
- [ ] 📖 Read: [Anthropic Prompt Engineering Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview) — concise, practical, essential
- [ ] 🔬 Mini-Project: Create a `prompts/` directory in your repo with reusable prompt templates:
  - `code-review.md` — prompt for reviewing code quality
  - `test-generation.md` — prompt for generating unit tests
  - `refactor.md` — prompt for refactoring suggestions
  - `debug.md` — prompt for root cause analysis from error logs

---

### 🛠️ Week 2: Claude Code Core Workflow + Git Integration

**Objective:** Set up Claude Code, learn the core commands, and integrate AI into your daily Git workflow.

#### Claude Code Setup
- [ ] **Install**: `npm install -g @anthropic-ai/claude-code`
- [ ] **Context Management**:
  - `/add` — add specific files (don't dump everything, be surgical)
  - `/compact` — compress long conversations to stay within context limits
  - `/review` — review diffs before applying changes
- [ ] **`CLAUDE.md` Configuration**:
  - Create a `CLAUDE.md` in your project root with coding rules: language, style preferences, tech stack constraints
  - Test with: `claude /init`
  - 📺 Watch: [Anthropic YouTube](https://www.youtube.com/@anthropic-ai) — official Claude Code walkthroughs

#### Git Workflow with AI
- [ ] **Commit Messages**: Use Claude Code to generate meaningful commit messages from staged changes
- [ ] **PR Descriptions**: Generate PR descriptions that explain the "why" not just the "what"
- [ ] **Code Review**: Use `/review` to catch issues before pushing
- [ ] 🔬 Practice: Make 10 commits on a practice repo using AI-assisted commit messages — develop the muscle memory

---

### 🔌 Week 3: MCP, Skills & Sub-Agents

**Objective:** Extend Claude Code with external tools (MCP servers), create reusable skills, and configure sub-agents.

#### MCP (Model Context Protocol)
- [ ] 📖 Course: [Anthropic Academy — MCP Course](https://anthropic.skilljar.com/)
- [ ] **Setup MCP Servers**:
  - Filesystem MCP — safe read/write for project files
  - Postgres MCP — connect to Supabase for direct DB queries
- [ ] 🔬 Lab: Query your Supabase database through Claude Code using the Postgres MCP server

#### Sub-Agents & Skills
- [ ] **Sub-Agents**: Create specialized `/agents` personas:
  - "QA Bot" — focused on finding edge cases and writing tests
  - "Refactor Bot" — focused on code quality improvements
- [ ] **Skills**: Create reusable skill files for common workflows (deployment, migration, etc.)

---

### Week 4: Prompt Library & Debugging with AI

**Objective:** Build a personal prompt library and master the art of debugging with AI assistance.

#### Debugging with AI
- [ ] **The Debugging Workflow**: Learn to provide good context to Claude Code:
  1. Error message / stack trace
  2. Relevant code (not the entire codebase)
  3. What you've already tried
  4. Expected vs actual behavior
- [ ] 🔬 Practice: Intentionally break things in a project and practice the debugging loop:
  - CORS errors
  - Auth failures
  - Type mismatches
  - Race conditions
- [ ] **Pattern**: Use `claude "Here's the error: [paste]. Here's the relevant code: [paste]. I've tried [X]. What's the root cause?"` — structured debugging prompts

---

## 📅 Month 2: Build LoveBytes (AI-Assisted Full-Stack App Dev)

### 🏗️ Week 5: Planning & Scaffolding

**Objective:** Use Claude Code to plan and scaffold the entire LoveBytes app from scratch.

- [ ] `claude "Create PLAN.md for React/Supabase recipe app with the following features: ..."`
- [ ] **Scaffold**: Vite + React + TypeScript + Tailwind + Shadcn/ui + Clerk Auth
- [ ] **Database**: Design Supabase schema using Claude Code → generate migration files
- [ ] **Architecture**: Let Claude Code propose the folder structure, then review and adjust
- [ ] 📝 Key Learning: Practice the "AI proposes, you review" workflow — this is how 10x devs work

---

### 🧱 Week 6: CRUD, Logic & Testing with AI

**Objective:** Build core features and learn to generate tests alongside your code.

#### Feature Development
- [ ] **Prompts**: Generate Supabase migrations, `useRecipe` hook (TanStack Query), API layer
- [ ] **Pseudo-code → Code**: Write pseudo-code for planner logic, then let Claude implement it
- [ ] **Pattern**: Always ask Claude to explain its implementation choices — you learn faster this way

#### Testing with AI (New — from gap analysis)
- [ ] **Generate Tests**: For every feature, ask Claude Code to generate tests alongside the implementation
- [ ] **Types of Tests**:
  - Unit tests for utility functions and hooks
  - Integration tests for API calls
  - Component tests with React Testing Library
- [ ] **CI Pipeline**: Use Claude Code to scaffold a GitHub Actions workflow:
  - Run tests on every push
  - Lint checking
  - Type checking
- [ ] 🔬 Mini-Project: Achieve >80% test coverage on LoveBytes core logic, entirely AI-assisted

---

### 💅 Week 7: UI Polish & Performance

**Objective:** Use AI for design iteration, refactoring, and performance optimization.

- [ ] **Style**: Use Claude Code to iterate on card layouts, theme, animations
- [ ] **Refactor**: Ask Claude to identify code smells and refactor (extract components, simplify logic)
- [ ] **Bugfix**: Practice debugging CORS issues, Supabase RLS policies, performance bottlenecks
- [ ] **Accessibility**: Ask Claude to audit and fix a11y issues (aria labels, keyboard nav, contrast)

---

## 📅 Month 3: Automation, Optimization & Workflows

> **Note:** RAG and Agents have been moved to the AI Engineer roadmap where they'll get the deep treatment they deserve. This month focuses on becoming a workflow machine.

### ⚡ Week 8: Claude Code Automation Scripts

**Objective:** Build automation scripts that save you hours every week.

- [ ] **Documentation Generation**: Script that generates/updates README, API docs, and JSDoc from code
- [ ] **TODO Backlog**: Script that scans codebase for TODOs and generates a prioritized backlog
- [ ] **Changelog**: Auto-generate changelogs from git history
- [ ] **Migration Helper**: Script that generates DB migration files from schema changes
- [ ] 🔬 Mini-Project: Build a `scripts/` directory with 3+ reusable automation scripts

---

### 🎯 Week 9: Advanced Patterns & Token Optimization

**Objective:** Master advanced Claude Code patterns and optimize for speed + cost.

- [ ] **Advanced `CLAUDE.md`**: Evolve your CLAUDE.md with lessons learned — what works, what doesn't
- [ ] **Token Tracking**: Monitor and optimize token usage per session
- [ ] **Temperature Tuning**: Understand when to use high vs low temperature (creative vs precise tasks)
- [ ] **Custom Workflows**: Create end-to-end workflows:
  - "Feature workflow": spec → plan → implement → test → PR
  - "Bug workflow": reproduce → diagnose → fix → verify → commit
- [ ] **Parallel Agents**: Use sub-agents for parallel tasks (one writes code, another writes tests)

---

### 📊 Week 10: Measure, Document & Level Up

**Objective:** Quantify your productivity gains and create a personal knowledge base.

- [ ] **Measure**: Track before/after metrics on common tasks:
  - Time to implement a CRUD feature
  - Time to debug a production issue
  - Time to write tests for existing code
- [ ] **Document**: Write a personal "AI-Assisted Development Playbook" with your best prompts, workflows, and lessons
- [ ] **Share**: Blog post or README documenting your 10x journey — this becomes part of your portfolio

---

## 📚 Resources

### 📺 YouTube (Great for Cardio Sessions)
| Channel | What You'll Learn |
|---------|------------------|
| [Andrej Karpathy](https://www.youtube.com/@AndrejKarpathy) | LLM fundamentals, transformers intuition |
| [3Blue1Brown](https://www.youtube.com/@3blue1brown) | Math intuition, attention mechanism |
| [Anthropic](https://www.youtube.com/@anthropic-ai) | Claude Code demos, MCP walkthroughs |
| [AI Explained](https://www.youtube.com/@aiexplained-official) | Stay current on AI breakthroughs |
| [Fireship](https://www.youtube.com/@Fireship) | Fast-paced dev tool overviews |

### 📖 Courses
- [Anthropic Academy](https://anthropic.skilljar.com/) — MCP, Claude API, prompt engineering
- [Anthropic Prompt Engineering Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)

### 🔧 Tools
- [Tiktokenizer](https://tiktokenizer.vercel.app/) — Visualize tokenization
- [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code) — Official docs

---

## 📈 Progress Tracking

| Month | Focus | Key Deliverable |
|-------|-------|----------------|
| Month 1 | Fundamentals + Claude Code | Prompt library + CLAUDE.md mastery |
| Month 2 | Build LoveBytes | Working app with tests + CI/CD |
| Month 3 | Automation + Optimization | Personal AI playbook + measurable gains |
