# Claude Fable 5 — Overview & Use Cases

## Overview

- Claude Fable 5 is Anthropic's most capable widely released model, built for the most demanding reasoning and long-horizon agentic work.
- Launched June 9, 2026, alongside Claude Mythos 5 — the first models in the new **Mythos class**, a tier that sits above Claude Opus in capability.
- Claude Fable 5 and Claude Mythos 5 share the same underlying model. Fable 5 is generally available and includes additional safety measures for dual-use capabilities; Mythos 5 is offered without those measures to approved organizations only (Project Glasswing).
- API model ID: `claude-fable-5` (Mythos 5: `claude-mythos-5`).
- Specs: **1M token context window** (default and maximum), **up to 128K output tokens** per request.
- Pricing: **$10 per million input tokens / $50 per million output tokens** — less than half the price of Claude Mythos Preview.

## Model family positioning

| Model | Tier | Access |
|---|---|---|
| Claude Fable 5 | Mythos class (above Opus) | Generally available (API + subscriptions) |
| Claude Mythos 5 | Mythos class (same model, no dual-use classifiers) | Project Glasswing only |
| Claude Opus 4.8 | Opus tier — most capable Opus model | Generally available, $5/$25 per MTok |
| Claude Sonnet 4.6 | Best speed/intelligence balance | Generally available, $3/$15 per MTok |
| Claude Haiku 4.5 | Fastest, most cost-effective | Generally available, $1/$5 per MTok |

- Fable 5 is recommended when the task demands the highest available intelligence: hardest unsolved problems, multi-hour autonomous runs, frontier reasoning. Opus 4.8 remains the default for general work.

## Headline capabilities

- **Long-horizon agentic execution**: state-of-the-art at long, autonomous work. Single requests on hard tasks can run many minutes (a 15-minute single request is normal when a task involves gathering context, building, and self-verifying). Best results come from a full task specification up front and high effort settings.
- **Software engineering**: Stripe reported Fable 5 compressed months of work into days, completing a 50-million-line Ruby migration in one day. Strong first-shot implementations of well-specified systems, code review, debugging, and repository-history search.
- **Knowledge work**: top performance on finance benchmarks; end-to-end enterprise deliverables — financial analysis, spreadsheets, slides, documents.
- **Vision**: state-of-the-art performance on dense or degraded images — explicitly trained to use bash and crop tools on flipped/blurry/noisy inputs. Demonstrated playing Pokémon FireRed from screenshots alone.
- **Long-context + memory**: functions effectively across millions of tokens; performs notably better when given a memory surface (even a plain markdown file) to write learnings to. Supports the memory tool, compaction, and context editing.
- **Multi-agent orchestration**: parallel sub-agent delegation is dependable; reliably sustains ongoing communications with long-running sub-agents and peer agents.
- **Navigating ambiguity**: stronger at connecting tasks to intent; teams with the best early outcomes gave it their hardest unsolved problems first.
- **Life sciences (Mythos 5)**: accelerated drug design tasks approximately tenfold and generated novel scientific hypotheses (protein design, genomics, molecular biology).

## Customer signals (early access)

- **Stripe**: 50-million-line Ruby migration completed in one day — "months of work into days."
- **Cursor**: "opened up a class of long-horizon problems that were out of reach."
- **GitHub**: "exceeded previous benchmarks" on complex coding tasks.
- **Cognition**: highest-scoring model on FrontierBench.

## Use cases

1. **Autonomous coding agents** — overnight refactors, large migrations, complex multi-repo changes that complete without human correction.
2. **Deep research & analysis** — multi-source research, financial modeling, legal document review, long-document synthesis across the 1M context window.
3. **Enterprise deliverables** — end-to-end production of spreadsheets, slide decks, documents, and analyses.
4. **Agent orchestration** — coordinator agents managing fleets of parallel sub-agents on independent workstreams.
5. **Vision-heavy workflows** — document understanding on degraded scans, screenshot-driven computer use, chart/figure analysis.
6. **Code review & debugging** — higher recall and precision on real bugs; one-shot fixes; correctly identifying intermittent flakes.
7. **Scientific research (via Mythos 5 / Glasswing)** — drug design, genomics, hypothesis generation for approved researchers.

## Developer experience / API

- **Thinking is always on** — adaptive thinking is the only mode; control depth with the `effort` parameter (`low` → `xhigh` and `max`). Lower effort on Fable 5 often exceeds the `max` performance of previous models.
- **Raw chain of thought is never returned** — `display: "summarized"` returns readable summaries.
- **Refusals & fallback**: safety classifiers may decline requests in covered domains (HTTP 200 with `stop_reason: "refusal"`). Server-side `fallbacks` parameter, SDK middleware, or fallback credit retry the request on Claude Opus 4.8 — pre-output refusals are not billed.
- Supported at launch: effort, task budgets (beta), memory tool, code execution, programmatic tool calling, context editing, compaction, vision.
- Available on the Claude API, Claude Platform on AWS, Amazon Bedrock, Vertex AI, and Microsoft Foundry.
- Requires 30-day data retention (designated a Covered Model; not available under zero data retention).

## Safety

- Three primary safeguards on Fable 5:
  1. **AI classifiers** detect and block harmful requests in cybersecurity, biology/chemistry, and model-distillation domains; blocked queries can fall back to Claude Opus 4.8 instead of refusing outright.
  2. **Jailbreak resistance**: 1,000+ hours of external red-teaming produced no universal jailbreaks.
  3. **Data retention**: 30-day policy, data used only for safety purposes and deleted afterward.
- Mythos 5 removes cybersecurity safeguards for authorized defense professionals and biology safeguards for approved researchers through trusted access programs.

## Sources

- https://platform.claude.com/docs/en/about-claude/models/introducing-claude-fable-5.md
- https://www.anthropic.com/news/claude-fable-5-mythos-5
- https://www.anthropic.com/news/claude-fable-5 (announcement reference)
- Anthropic Claude API documentation (models overview, migration guide)
