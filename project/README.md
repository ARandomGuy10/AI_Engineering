# Org Assistant

A question-answering and action assistant over a real company's internal handbook, built the way a forward-deployed engineer would build it for a client.

**Data:** the [GitLab Handbook](https://handbook.gitlab.com/) ([source](https://gitlab.com/gitlab-com/content-sites/handbook), MIT licensed). Clone it into `data/` (git-ignored). Never commit it.

## Layers

| Layer | Phase | Capability | Status |
|---|---|---|---|
| L1 | 01 | Answers with citations; says "I don't have enough evidence" when it can't answer | ⚪ |
| L2 | 01 | Hybrid search, re-ranking, incremental sync of changed and deleted docs, role-based access | ⚪ |
| L3 | 02 | Safe actions: read-only tools, draft-only writes, approval, step and cost limits | ⚪ |
| L4 | 03 | Traces, golden set, checked LLM judge, regression gate in CI | ⚪ |
| L5 | 04 | On AWS via Terraform: ECS Fargate, RDS pgvector, API tests in CI | ⚪ |
| L6 | 05 | Guardrails, caching, fallbacks, rollout plan, runbook | ⚪ |

## Golden set

`evals/golden.jsonl` is written **before** the first line of RAG code. Each case has a question, the role asking, the expected answer, the source pages, and the expected behaviour (`answer`, `refuse_no_evidence`, or `refuse_no_access`).

## Results

Every retrieval or prompt change gets a row here.

| Date | Change | Answer quality | Refusals correct | Access respected | Notes |
|---|---|---|---|---|---|
| | Baseline (naive RAG) | | | | |
