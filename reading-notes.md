# Reading notes

[Back to the directory](README.md)

Original titles, authors, dates, stack tags, and a short note on each article. For companies with several posts, start with the overview and work through the implementation details.

`Internal deployment` describes a team’s own use. `Vendor implementation` describes a product built for customers. Stack tags belong to the article, not the company’s entire stack.

## Alan

**[Re-inventing our craft: how Alan’s Data team is shaping its future with AI](https://medium.com/alan/re-inventing-our-craft-how-alans-data-team-is-shaping-its-future-with-ai-e8d73d095ece)** · Alan · April 2026 · `Internal deployment`

By Sebastien de Larquier ([@sdelarquier](https://github.com/sdelarquier)).

`Nao` · `Claude Code` · `Dust`

Alan’s data team describes using agents for analysis, development, and visualization, including what happened when colleagues outside the team started using them. Useful for the rollout questions: scoped write access, privacy, review fatigue, and how the team’s work changes. This is an adoption account rather than a full architecture walkthrough.

[Back to the directory](README.md)

## AngelList

**[The Semantic Layer Nobody Maintains](https://www.angellist.com/blog/the-semantic-layer-nobody-maintains)** · AngelList · August 2026 · `Internal deployment`

By Beau Rothrock.

`dbt` · `Snowflake` · `Devin` · `GitHub Actions` · `MCP`

AngelList generates its agent’s data catalog from dbt and Snowflake metadata and rebuilds it when changes merge. The post shows what can be pulled from metadata and application code, and where people still need to explain business definitions and check them with domain owners.

[Back to the directory](README.md)

## Anthropic

**[How Anthropic enables self-service data analytics with Claude](https://claude.com/blog/how-anthropic-enables-self-service-data-analytics-with-claude)** · Anthropic · June 2026 · `Internal deployment`

By Josh Cherry, Clement Peng, Johanne Jiao, Justin Leder, and Chen Chang.

`Claude Code` · `MCP` · `Git`

Anthropic uses Claude skills to guide analysis through agreed metric definitions, documentation, and raw data. When a data model changes, the team reviews the relevant skills and docs and reruns the affected tests. Includes templates you can adapt for your own skills.

[Back to the directory](README.md)

## BlaBlaCar

**[(Re)Building an AI-Ready data universe at BlaBlaCar](https://medium.com/blablacar/building-an-ai-ready-data-universe-at-blablacar-cb15fbc42020)** · BlaBlaCar · September 2026 · `Internal deployment`

By Maxime Rosina.

`dbt` · `BigQuery` · `Markdown` · `SQL`

BlaBlaCar rebuilt a competitive-intelligence warehouse so people and analytics agents could use the same documented business logic. The post includes dbt doc blocks, naming conventions, metric SQL, and a documenter-reviewer agent loop that checks generated documentation before it ships. It also shows how simpler models and consumption tables reduced maintenance and BigQuery spend; the focus is the data and context layer rather than the analytics-agent runtime.

[Back to the directory](README.md)

## Faire

**[We moved analytics into an IDE — and haven't looked back](https://craft.faire.com/we-moved-analytics-into-an-ide-and-havent-looked-back-f6e0c249cc42)** · Faire · November 2025 · `Internal deployment`

By Alexandra (Alexa) Cerf.

`Cursor` · `Snowflake` · `Mode` · `MCP`

Faire moved analytics work into Cursor and added reusable commands for querying, checking, and documenting results. The post also gets into what it took to get people using it: working through authentication issues, MCP errors, and Git problems, and changing everyday habits.

[Back to the directory](README.md)

## GitHub

**[How we built an internal data analytics agent](https://github.blog/ai-and-ml/github-copilot/how-we-built-an-internal-data-analytics-agent/)** · GitHub · June 2026 · `Internal deployment`

By Matteo Vasirani ([@mvasirani](https://github.com/mvasirani)) and Cynthia Joseph ([@CynthiaJoseph](https://github.com/CynthiaJoseph)).

`GitHub Copilot` · `Kusto` · `Trino` · `MCP`

GitHub’s Qubot answers data questions in Slack and developer tools. The interesting part is how teams maintain what it knows: product, data, and business teams own different layers of the context, and changes go through pull requests with evaluations before they ship.

[Back to the directory](README.md)

## Gorgias

**[How We Built a Company-Wide Internal AI Platform](https://medium.com/gorgias-engineering/how-we-built-a-company-wide-internal-ai-platform-b57947cad08b)** · Gorgias · July 2026 · `Internal deployment`

By Adam Treen.

`dbt` · `Markdown` · `Git` · `MCP` · `Slack`

Cortex grew from a Slack analytics agent into a shared workspace for skills, automations, apps, and company context. Gorgias explains how these pieces share one runtime and how changes made through the UI become Git changes people can review.

**[Building a context layer from the ground up](https://medium.com/gorgias-engineering/building-a-context-layer-from-the-ground-up-d6f72713915a)** · Gorgias · March 2026 · `Internal deployment`

By Yochan Khoi.

`dbt` · `BigQuery` · `Python` · `Airbyte`

Gorgias organizes context into table descriptions, business topics, and step-by-step instructions for more involved questions. The agent loads what it needs as it goes. Includes SQL and YAML examples showing how to document which table to use, how to query it, and what to check in the answer.

**[Creating a culture of Agent Debugging](https://medium.com/gorgias-engineering/creating-a-culture-of-agent-debugging-97ba4a50e956)** · Gorgias · May 2026 · `Internal deployment`

By Antoine Balliet ([@aballiet](https://github.com/aballiet)).

`LangGraph` · `LangSmith` · `Slack` · `BigQuery`

Gorgias makes agent traces easier to inspect and routes requests for help to the people who own the relevant context. The team debugs answers in Slack, and a weekly job turns problems reported by the agent into proposed code or context changes.

**[Cortex Labs: Benchmarking an Internal AI Agent Beyond Vibes](https://medium.com/gorgias-engineering/cortex-labs-benchmarking-an-internal-ai-agent-beyond-vibes-ec9404ce7f8b)** · Gorgias · July 2026 · `Internal deployment`

By Arthur Edmond ([@Shumatsurontek](https://github.com/Shumatsurontek)).

`LangSmith` · `Fireworks AI` · `Kimi K2.7 Code` · `Claude Sonnet` · `GitHub Actions`

Gorgias turns production conversations into evaluation tasks with human-reviewed rubrics, then compares quality, latency, and cost on its actual agent stack. The experiments separate the model doing retrieval from the model doing the analysis. The article also distinguishes its opt-in PR evaluations from a hard merge gate still being built.

**[How do you handle skill retrieval at scale ? From a small company catalog to more than 300 skills in a month.](https://medium.com/gorgias-engineering/how-do-you-handle-skill-retrieval-at-scale-7a6c524bd77e)** · Gorgias · August 2026 · `Internal deployment`

By Arthur Edmond ([@Shumatsurontek](https://github.com/Shumatsurontek)).

`BM25` · `Markdown`

Gorgias compared an LLM ranker, fine-tuned ColBERT, and BM25 for finding the right skill. BM25 was close enough on their tests to win on maintenance cost. Each skill now has three example requests that test whether its description makes it findable before it ships.

[Back to the directory](README.md)

## LinkedIn

**[Practical text-to-SQL for data analytics](https://www.linkedin.com/blog/engineering/ai/practical-text-to-sql-for-data-analytics)** · LinkedIn · December 2024 · `Internal deployment`

By Albert Chen, Manas Bundele, Gaurav Ahlawat, Patrick Stetz, Zhitao W., Qiang Fei, Don Jung, Audrey Chu, Bharadwaj Jayaraman, Ayushi Panth, Yatin Arora, Sourav Jain, Renjith Varma, Alex Ilin, Iuliia Melnychuk, Chelsea C., Joyan Sil, and Xiaofeng Wang.

`LangChain` · `LangGraph` · `DataHub` · `DARWIN`

LinkedIn’s SQL Bot uses dataset descriptions, query history, and a knowledge graph to choose tables and write queries. The team explains how it removes deprecated datasets, repairs SQL, and tests questions with more than one valid answer. Also worth reading for the decision to put the bot inside the existing query editor.

[Back to the directory](README.md)

## Meta

**[Inside Meta’s Home Grown AI Analytics Agent](https://medium.com/@AnalyticsAtMeta/inside-metas-home-grown-ai-analytics-agent-4ea6779acfb3)** · Meta · March 2026 · `Internal deployment`

Published by Analytics at Meta.

`SQL` · `Python`

Meta’s Analytics Agent starts from each person’s recent query history, then retrieves table descriptions, example queries, column documentation, code, semantic models, and other business context as it works. The article explains its iterative query loop and the Cookbooks, Recipes, and Ingredients system teams use to package domain instructions, reference experts, validation rules, semantic models, documentation, and learned corrections. It also covers rollout from a weekend prototype to company-wide use, with the SQL behind every answer visible for review.

[Back to the directory](README.md)

## OpenAI

**[Inside OpenAI's in-house data agent](https://openai.com/index/inside-our-in-house-data-agent/)** · OpenAI · January 2026 · `Internal deployment`

By Bonnie Xu ([@xubonnie](https://github.com/xubonnie)), Aravind Suresh, and Emma Tang.

`GPT-5.2` · `Codex` · `MCP` · `OpenAI Evals API`

OpenAI explains how its agent learns about the data before anyone asks a question, then looks up more context as it works. The team uses Codex to extract context from code, carries the user’s permissions through to data access, and tests answers against query results.

[Back to the directory](README.md)

## Ramp

**[Meet Ramp Research: Our Agentic Data Analyst](https://engineering.ramp.com/post/meet-ramp-research)** · Ramp · September 2025 · `Internal deployment`

By Faiz Hilaly, Cesar Duran, and Jay Sobel ([@jaysobel](https://github.com/jaysobel)).

`dbt` · `Snowflake` · `Looker` · `Slack` · `Python`

Ramp combines warehouse metadata with docs written by domain owners, then gives its Slack agent tools to explore the data. The team explains why reviewing every answer did not scale and how it moved to tests of both answers and intermediate steps, including tool calls and table choices.

**[Building an Analyst Agent with dbt](https://jaysobel.substack.com/p/building-an-analyst-agents-with-dbt)** · Jay Sobel / Ramp · October 2025 · `Internal deployment`

By Jay Sobel ([@jaysobel](https://github.com/jaysobel)).

`dbt` · `Snowflake` · `Claude`

Jay Sobel shows how to put table metadata, business definitions, and domain docs into dbt models that an agent can query. A practical starting point if your team already uses dbt and Snowflake, with SQL and Jinja examples for building the context tables.

**[The Shape and Feel of the Post-AI Data Stack](https://www.iandmacomber.com/blog/post-ai-data-stack)** · Ian Macomber / Ramp · August 2026 · `Internal deployment`

By Ian Macomber ([@ianmacomber](https://github.com/ianmacomber)).

`Snowflake` · `React`

Ian Macomber describes how Ramp builds dashboards for people and agents to read, and tests whether different interfaces and models produce consistent answers. The later sections cover inspecting traces and turning Gong calls into reusable structured data. A broader essay with concrete updates on how Ramp’s internal system works.

[Back to the directory](README.md)

## Replit

**[AI adoption starts with truth](https://replit.com/blog/ai-adoption)** · Replit · August 2026 · `Internal deployment`

By Jon Eide and Aadil Hussaini.

`Git`

Replit saves failed analyses, their fixes, and the reasons behind them in a shared Git repository. People review the changes so other agents can use what the team learned. A useful account of how to stop correcting the same mistake in separate conversations.

[Back to the directory](README.md)

## Sourcegraph

**[Building DataBot: Our always-on data assistant](https://sourcegraph.com/blog/building-databot-our-always-on-data-assistant)** · Sourcegraph · February 2026 · `Internal deployment`

By Aditya Kalia.

`Gemini 2.5 Flash` · `BigQuery` · `Google Cloud Functions` · `Slack` · `Sourcegraph Deep Search`

DataBot answers questions in Slack using a few tools to look up schemas, run SQL, and search the code that produces the data. Sourcegraph shows how the team checks the SQL behind answers and updates the instructions when something goes wrong.

[Back to the directory](README.md)

## Uber

**[QueryGPT – Natural Language to SQL Using Generative AI](https://www.uber.com/gb/en/blog/query-gpt/)** · Uber · September 2024 · `Internal deployment`

By Abhi Khune, Callie Busch, Jeffrey Johnson, and Pradeep Chakka.

`GPT-4 Turbo`

Uber walks through the move from a small RAG prototype to separate agents for identifying the business domain, selecting tables, and trimming large schemas. Users can correct the table selection before SQL is written. The evaluation section shows how to test those steps separately and track recurring errors.

[Back to the directory](README.md)

## Vercel

**[We removed 80% of our agent's tools](https://vercel.com/blog/we-removed-80-percent-of-our-agents-tools)** · Vercel · December 2025 · `Internal deployment`

By Andrew Qu ([@quuu](https://github.com/quuu)).

`Claude Opus 4.5` · `AI SDK` · `Vercel Sandbox` · `Cube`

Vercel replaced most of its SQL agent’s specialized tools with bash access to Cube files, keeping a tool for running SQL. The files already documented measures and joins, which made the simpler setup work. Includes code and a before/after comparison on five queries.

[Back to the directory](README.md)

## Cassis

**[A blank beats a guess: assembling context for analytics agents](https://blog.getcassis.com/a-blank-beats-a-guess/)** · Cassis · August 2026 · `Vendor implementation`

By Matthieu Blandineau ([@matbcassis](https://github.com/matbcassis)).

`dbt` · `SQL` · `YAML` · `Markdown` · `Claude`

How we assemble a first version of context from schemas, dbt, dashboards, query logs, and documentation. The GitLab walkthrough shows what scripts can recover, where an LLM can draft from evidence, and which gaps need a person’s answer. Includes the [open-source context bootstrap kit](https://github.com/GetCassis/ontology-bootstrap).

**[Context engineering for analytics agents: lessons from six months of building and rebuilding](https://blog.getcassis.com/context-engineering-for-analytics-agents/)** · Cassis · June 2026 · `Vendor implementation`

By Aloÿs Augustin and Matthieu Blandineau ([@matbcassis](https://github.com/matbcassis)).

`Cassis` · `Markdown` · `Git`

How we organize tables, metrics, and business rules so an agent can find the context it needs. We explain why we removed a layer that duplicated the schema, how we trace wrong answers back to missing or misplaced context, and where keeping one editable copy of each fact is still work in progress.

[Back to the directory](README.md)

## Cube

**[Building an Agentic Analytics Harness](https://cube.dev/blog/building-an-agentic-analytics-harness)** · Cube · September 2026 · `Vendor implementation`

By Artyom Keydunov ([@keydunov](https://github.com/keydunov)).

`Cube` · `Semantic SQL` · `MCP`

Cube walks through the tools behind its analytics agent, from querying data to building dashboards and changing models. Useful details include errors that tell the agent how to retry, results that say when rows have been cut off, and searches that respect the user’s permissions.

[Back to the directory](README.md)

## Omni

**[Benchmarking Omni's agentic analytics harness](https://omni.co/blog/benchmarking-omnis-agentic-analytics-harness)** · Omni · July 2026 · `Vendor implementation`

By Colin Zima.

`Omni` · `Claude`

Omni tests its agent on 100 analytics questions and tracks accuracy, response time, and cost as it changes the context and SQL validation. Useful for planning your own experiments: the results come from Omni’s chosen questions and tuned semantic models.

[Back to the directory](README.md)

## Benchouse

**[The Analytics Agent Benchmark](https://benchouse.ai/benchmark)** · Benchouse · Season 2026-S2 · `Benchmark` · Checked September 2026

Published by Benchouse.

A leaderboard comparing analytics agents on accuracy, completeness, restraint, and cost per question, with filters for descriptive, diagnostic, and prescriptive questions. Each entry identifies the model, where disclosed, and its context setup. Useful for comparing the configurations tested in a given season; follow the live page for current results.

[Back to the directory](README.md)
