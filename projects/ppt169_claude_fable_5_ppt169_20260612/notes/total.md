# 01_cover

This is Claude Fable 5, Anthropic's most capable widely released model, and over the next ten minutes we'll cover what it is, what it's exceptional at, and where to put it to work. Fable 5 launched in June twenty twenty-six as the first model in the new Mythos class, built specifically for the most demanding reasoning and long-horizon agentic work.

---

# 02_agenda

Here's the route we'll take. We start with what Fable 5 actually is and where it sits in the model family, then move through the specs, the headline capabilities, and what early customers are reporting. The back half is practical: the use cases worth pointing it at first, the developer experience changes you need to plan for, and the safety architecture that lets a frontier model ship as generally available.

---

# 03_what_is_fable_5

The single most important thing to understand is that Fable 5 is not a better Opus — it's a new class above Opus. Launched on June ninth, twenty twenty-six, Fable 5 and its sibling Claude Mythos 5 share the same underlying model: one frontier intelligence with two release postures. Fable 5 is the generally available release and carries additional safety measures for dual-use capabilities, while Mythos 5 ships without those measures to approved organizations through Project Glasswing. If you can call an API, you can use Fable 5 today.

---

# 04_model_family

So where does it sit? The pyramid tells the story: the Mythos class now tops the family, above Opus, Sonnet, and Haiku. Fable 5 is the generally available face of that class at ten dollars in and fifty dollars out per million tokens. The practical guidance is simple — Opus 4.8 remains the default for general work, and you reach for Fable 5 when the task genuinely demands the highest available intelligence: the hardest unsolved problems and the longest autonomous runs.

---

# 05_specs

The economics are predictable, which matters for a frontier model. You get a one-million-token context window as the default and the maximum, up to one hundred twenty-eight thousand output tokens per request, and flat pricing at ten and fifty dollars per million tokens — less than half the price of the Mythos Preview it replaces. It's live on five platforms from day one, and the one operational requirement to know about is thirty-day data retention: Fable 5 is not available under zero data retention.

---

# 06_capabilities

The gains land above what prior models could do at all, so don't evaluate it only on yesterday's workloads. Six areas stand out. It sustains multi-hour autonomous runs where a fifteen-minute single request is normal. It compresses months of software engineering into days. It leads finance benchmarks and produces complete enterprise deliverables. Its vision handles dense and degraded images — it played Pokémon FireRed from screenshots alone. It stays effective across millions of tokens, especially with a memory surface. And parallel sub-agent delegation, which used to be a gamble, is now dependable.

---

# 07_customer_signals

Early-access teams are reporting breakthroughs, not increments. Stripe completed a fifty-million-line Ruby migration in a single day — their words were months of work into days. Cursor said it opened up a class of long-horizon problems that were simply out of reach before. GitHub reported it exceeded their previous benchmarks on complex coding tasks, and Cognition measured it as the highest-scoring model ever on FrontierBench, their hardest internal evaluation.

---

# 08_use_cases

Those signals translate into six use cases, and they share one shape: long, ambiguous, high-stakes work that runs end to end. Autonomous coding agents for overnight refactors and large migrations. Deep research and analysis across the full million-token window. Enterprise deliverables produced as finished artifacts rather than drafts. Orchestration of parallel sub-agent fleets. Vision-heavy workflows like degraded scans and screenshot-driven computer use. And code review, where it finds real bugs with both higher recall and higher precision.

---

# 09_spotlight_engineering

Long-horizon coding is the breakout use case, and Stripe's number is the proof point: fifty million lines migrated in one day. Three practices made that possible, and they apply to any team. Specify the task fully in one well-written first turn. Run at high effort, because deeper planning up front usually lowers total cost. And let the model build and run its own verification harness as it works, instead of checking everything by hand afterward.

---

# 10_knowledge_work

The second spotlight is enterprise knowledge work, where the shift is that one agent now carries the analysis from raw source material to a shippable deliverable. Financial analysis with benchmark-leading accuracy, documents and decks produced as working files, research synthesis across entire data rooms, and legal review applied with the same judgment on file one and file ten thousand. The takeaway is the absence of hand-offs — analysis and production happen in one context.

---

# 11_developer_experience

For developers, integration is mostly a model-ID swap, with three behaviors to plan for. First, thinking is always on — adaptive is the only mode, and you control depth with the effort parameter rather than token budgets; low effort on Fable 5 often beats prior models at max. Second, safety classifiers can decline a request, so check the stop reason and configure a fallback to Opus 4.8 — refusals before output are never billed. Third, it runs everywhere Claude runs, with one requirement: thirty-day data retention.

---

# 12_safety

Fable 5 can be generally available because three safeguards travel with it. Classifiers detect and block harmful cybersecurity, biology, and model-distillation requests, and blocked queries fall back to Opus 4.8 rather than dead-ending. More than a thousand hours of external red-teaming produced no universal jailbreaks. And the thirty-day retention policy uses data for safety purposes only before deletion. Mythos 5 is the same model with those safeguards lifted, but only for vetted partners under trusted-access programs.

---

# 13_closing

The teams with the best results did one thing differently: they gave Fable 5 their hardest unsolved problems first. So start there. Give it the full specification up front, sweep the effort levels to find your cost-quality point, and let it delegate and verify its own work. The model ID is claude-fable-5, it's available today on every major platform, and the announcement at anthropic dot com has the full details. Thank you.
