# AI Engineering

My path from **backend Java engineer** to **forward-deployed AI engineer**: building production AI systems on real organisation data. RAG, safe agents, evals, and deployment on AWS. Applied engineering, not research.

**📍 [Read the roadmap →](ROADMAP.md)**

## Where I am

| Phase | Window | Status |
|---|---|---|
| 00 · Foundations & mental model | 12–25 Oct | 🟡 In progress |
| 01 · RAG over real data, measured from day one | 26 Oct–15 Nov | ⚪ |
| 02 · Safe agents and workflows | 16 Nov–6 Dec | ⚪ |
| 03 · Evals and observability | 7–20 Dec | ⚪ |
| 04 · Deploy to AWS | 4–24 Jan | ⚪ |
| 05 · Production hardening and FDE craft | 25 Jan–7 Feb | ⚪ |
| 06 · Capstone and positioning | 8–28 Feb | ⚪ |

Dates are target windows. A phase is done when its exit criteria are met.

## The flagship project

**[Org Assistant](project/)**: a question-answering and action assistant over the [GitLab Handbook](https://handbook.gitlab.com/), a real company's internal docs. It's built in layers: cited answers, then access control and document sync, then safe actions, then evals in CI, then AWS, then hardening.

## Repo layout

```
ROADMAP.md     the plan: phases, milestones, resources, exit criteria
journal.md     five lines a week: learned, built, stuck, next, hours
learning/      one file per phase: notes, open questions, quiz answer
project/       the flagship system, grown layer by layer
scratch/       throwaway exercises and course labs
archive/       earlier roadmaps (Feb 2026), kept for history
```

## Principles

- **One system, grown in layers.** Depth over breadth.
- **Evals from day one.** Every change is measured against the golden set.
- **Safe by default.** Read-only tools, approval before writes, limits on steps and cost.
- **Ship it.** Deployed with Terraform and CI, or it doesn't count.
