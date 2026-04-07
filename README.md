# AI Product PRD + Evaluation Framework

This repository is a product management work sample focused on one of the most important gaps in modern AI product development: teams often try to launch AI features using generic product documents that do not account for model behavior, evaluation methodology, safety controls, fallback logic, or operational rollback criteria.

The repository is designed as a practical framework for AI product managers, technical program managers, and cross functional leaders who need a repeatable way to define, evaluate, and launch AI powered experiences with higher quality and lower avoidable risk. Rather than treating AI as a simple feature extension, this project treats AI as a product capability that requires explicit choices around model selection, offline evaluation, online experimentation, safety review, observability, and business impact measurement.

## Why this repository exists

Traditional PRDs are often sufficient for deterministic software workflows where behavior is predictable and outputs are tightly constrained. AI products are different. They introduce probabilistic behavior, variable latency, quality inconsistency, hallucination risk, prompt sensitivity, privacy considerations, and new failure modes that can damage user trust if they are not planned for up front.

This repository addresses that gap by providing a reusable AI specific PRD template, a fully worked example for AI powered e commerce search, an evaluation framework that covers both offline and online quality assessment, and a pre launch safety checklist that forces a team to define risk controls before rollout.

## What is included

- A reusable 14 section AI product PRD template
- A fully worked example PRD for AI powered e commerce search
- An evaluation framework covering offline metrics, online A B testing, and post launch monitoring
- A practical AI safety checklist for launch readiness
- A metrics glossary for common AI quality and operational terms
- An IMPACT document connecting product quality to business outcomes

## Why the worked example focuses on e commerce search

E commerce search is a strong example because it has clear user intent, measurable business outcomes, visible failure modes, and well understood pain points. It is also a realistic domain for demonstrating how AI product management differs from traditional search product management. A keyword based search system can fail on synonyms, natural language queries, vague intent, and conversational refinement, while an AI enhanced system introduces both meaningful upside and new operational risk.

## Key insight

The most important insight in this repository is that an AI product should not be approved for launch based only on a promising demo or anecdotal feedback. It should be approved only after the team has defined how quality will be measured offline, how success will be measured online, what failure modes are unacceptable, what fallback behavior protects the user, and what exact thresholds should trigger rollback.

## Recommended reading order

1. `templates/ai-prd-template.md`
2. `examples/ecommerce-ai-search-prd.md`
3. `evaluation/eval-framework.md`
4. `safety/ai-safety-checklist.md`
5. `IMPACT.md`

## Who this repository is for

This repository is built for product managers, aspiring AI PMs, technical program managers, product operations leaders, and interviewers evaluating whether a candidate can think clearly about AI feature definition, launch discipline, and business impact.

## Portfolio intent

This is a professional portfolio artifact. It is intended to demonstrate structured product thinking, AI specific evaluation judgment, launch readiness discipline, and the ability to connect technical tradeoffs to business outcomes.
