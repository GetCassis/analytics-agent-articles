# Analytics agents built by data teams

A curated list of articles from data teams building analytics agents.

[Recommended first reads](#recommended-first-reads) · [Internal builds](#internal-builds) · [Browse by problem](#browse-by-problem) · [Related reading](#related-reading) · [Contribute](CONTRIBUTING.md)

## Recommended first reads

1. **Anthropic — How a team makes self-service analytics work.** [Skills, metric definitions, documentation, and evaluations](https://claude.com/blog/how-anthropic-enables-self-service-data-analytics-with-claude) (Jun 2026), including how the team keeps them current as data models change.
2. **OpenAI — Inside an in-house data agent.** [The architecture behind context preparation, retrieval, permissions, and evaluations](https://openai.com/index/inside-our-in-house-data-agent/) (Jan 2026).
3. **Ramp — Building one around an existing dbt project.** [SQL and Jinja examples for context tables and domain documentation](https://jaysobel.substack.com/p/building-an-analyst-agents-with-dbt) (Oct 2025).

## Internal builds

Read an article directly from the right column, or click a company for its full reading notes. Dates are publication dates; stacks reflect what the authors used at the time.

| Team | Stack | What to read |
| --- | --- | --- |
| [Alan](reading-notes.md#alan) | Nao, Claude Code, Dust | [Adoption across the data team and beyond](https://medium.com/alan/re-inventing-our-craft-how-alans-data-team-is-shaping-its-future-with-ai-e8d73d095ece) (Apr 2026) |
| [AngelList](reading-notes.md#angellist) | dbt, Snowflake, Devin | [Generating context from metadata and code](https://www.angellist.com/blog/the-semantic-layer-nobody-maintains) (Aug 2026) |
| [Anthropic](reading-notes.md#anthropic) | Claude Code, MCP | [Skills, documentation, and evaluations](https://claude.com/blog/how-anthropic-enables-self-service-data-analytics-with-claude) (Jun 2026) |
| [BlaBlaCar](reading-notes.md#blablacar) | dbt, BigQuery, Markdown | [Rebuilding a warehouse and its documentation for analytics agents](https://medium.com/blablacar/building-an-ai-ready-data-universe-at-blablacar-cb15fbc42020) (Sep 2026) |
| [Faire](reading-notes.md#faire) | Cursor, Snowflake, Mode | [Moving analytics into an IDE](https://craft.faire.com/we-moved-analytics-into-an-ide-and-havent-looked-back-f6e0c249cc42) (Nov 2025) |
| [GitHub](reading-notes.md#github) | Copilot, Kusto, Trino | [Shared context ownership and PR evaluations](https://github.blog/ai-and-ml/github-copilot/how-we-built-an-internal-data-analytics-agent/) (Jun 2026) |
| [Gorgias · 5 posts](reading-notes.md#gorgias) | dbt, BigQuery, LangSmith, BM25 | [Cortex platform](https://medium.com/gorgias-engineering/how-we-built-a-company-wide-internal-ai-platform-b57947cad08b) (Jul 2026) · [Context](https://medium.com/gorgias-engineering/building-a-context-layer-from-the-ground-up-d6f72713915a) (Mar 2026) · [Debugging](https://medium.com/gorgias-engineering/creating-a-culture-of-agent-debugging-97ba4a50e956) (May 2026) · [Evals](https://medium.com/gorgias-engineering/cortex-labs-benchmarking-an-internal-ai-agent-beyond-vibes-ec9404ce7f8b) (Jul 2026) · [Skill retrieval](https://medium.com/gorgias-engineering/how-do-you-handle-skill-retrieval-at-scale-7a6c524bd77e) (Aug 2026) |
| [LinkedIn](reading-notes.md#linkedin) | LangGraph, LangChain, DataHub | [SQL Bot: retrieval, repair, and user experience](https://www.linkedin.com/blog/engineering/ai/practical-text-to-sql-for-data-analytics) (Dec 2024) |
| [Meta](reading-notes.md#meta) | SQL, Python | [Personal context, iterative analysis, and reusable domain knowledge](https://medium.com/@AnalyticsAtMeta/inside-metas-home-grown-ai-analytics-agent-4ea6779acfb3) (Mar 2026) |
| [OpenAI](reading-notes.md#openai) | GPT-5.2, Codex, MCP | [Context enrichment and runtime retrieval](https://openai.com/index/inside-our-in-house-data-agent/) (Jan 2026) |
| [Ramp · 3 posts](reading-notes.md#ramp) | dbt, Snowflake, Looker, Slack | [Research overview](https://engineering.ramp.com/post/meet-ramp-research) (Sep 2025) · [dbt implementation](https://jaysobel.substack.com/p/building-an-analyst-agents-with-dbt) (Oct 2025) · [What changed next](https://www.iandmacomber.com/blog/post-ai-data-stack) (Aug 2026) |
| [Replit](reading-notes.md#replit) | Git | [Sharing reviewed corrections between agents](https://replit.com/blog/ai-adoption) (Aug 2026) |
| [Sourcegraph](reading-notes.md#sourcegraph) | Gemini, BigQuery, Cloud Functions | [DataBot’s tools and feedback loop](https://sourcegraph.com/blog/building-databot-our-always-on-data-assistant) (Feb 2026) |
| [Uber](reading-notes.md#uber) | GPT-4 Turbo | [QueryGPT: domain, table, and column selection](https://www.uber.com/gb/en/blog/query-gpt/) (Sep 2024) |
| [Vercel](reading-notes.md#vercel) | Claude, AI SDK, Sandbox, Cube | [Simplifying the agent around filesystem access](https://vercel.com/blog/we-removed-80-percent-of-our-agents-tools) (Dec 2025) |

## Browse by problem

- **Giving the agent context:** [Ramp](reading-notes.md#ramp), [Gorgias](reading-notes.md#gorgias), [AngelList](reading-notes.md#angellist), [BlaBlaCar](reading-notes.md#blablacar), [Meta](reading-notes.md#meta), [OpenAI](reading-notes.md#openai).
- **Testing answers and model changes:** [Gorgias](reading-notes.md#gorgias), [Anthropic](reading-notes.md#anthropic), [Ramp](reading-notes.md#ramp), [LinkedIn](reading-notes.md#linkedin), [Meta](reading-notes.md#meta), [Uber](reading-notes.md#uber).
- **Fixing mistakes and keeping context current:** [GitHub](reading-notes.md#github), [Gorgias](reading-notes.md#gorgias), [Meta](reading-notes.md#meta), [Replit](reading-notes.md#replit).
- **Reducing cost and latency:** [Gorgias](reading-notes.md#gorgias), [Vercel](reading-notes.md#vercel).
- **Getting people to use it:** [Alan](reading-notes.md#alan), [Faire](reading-notes.md#faire), [Ramp](reading-notes.md#ramp), [LinkedIn](reading-notes.md#linkedin), [Meta](reading-notes.md#meta).

## Related reading

Product engineering, technical studies, and benchmarks that complement the internal builds.

- [Cube: Building an Agentic Analytics Harness](https://cube.dev/blog/building-an-agentic-analytics-harness) · `Vendor implementation`. Errors, result limits, and permission-aware tools. [Stack and notes](reading-notes.md#cube).
- [Omni: Benchmarking Omni’s agentic analytics harness](https://omni.co/blog/benchmarking-omnis-agentic-analytics-harness) · `Vendor implementation`. Testing quality, latency, and cost on a vendor’s analytics workload. [Stack and notes](reading-notes.md#omni).
- [Cassis: A blank beats a guess](https://blog.getcassis.com/a-blank-beats-a-guess/) · `Vendor implementation`. Building the first context from existing data assets, with an open-source bootstrap kit. [Stack and notes](reading-notes.md#cassis).
- [Cassis: Context engineering for analytics agents](https://blog.getcassis.com/context-engineering-for-analytics-agents/) · `Vendor implementation`. How we structure tables, metrics, and business rules so an agent can find what it needs. [Stack and notes](reading-notes.md#cassis).

- [Benchouse: The Analytics Agent Benchmark](https://benchouse.ai/benchmark) · `Benchmark`. Compare accuracy, completeness, restraint, and cost per question across analytics agents. [Notes](reading-notes.md#benchouse).

## Suggest an article

Know a team that has written up its internal build? Open an issue or pull request with the link and a sentence about what makes it useful. See the [contribution guide](CONTRIBUTING.md) for the format. Corrections and broken-link reports are welcome too.
