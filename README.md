# Awesome-Automated-Data-Quality-Enrichment

# Awesome-Automated-Data-Quality-Enrichment
**Top Automated Data Quality Enrichment (Opensource) 🌟 Star if you like it! 🌟**

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on B2B Data Enrichment, Data Quality Validation, Identity Resolution & Automated Cleansing*
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Automated Data Quality & Enrichment**. These tools enable revenue teams to enrich lead records with firmographic and contact data, validate and cleanse datasets, resolve identities across sources, and automate data quality workflows—from fully managed enrichment platforms with proprietary databases and AI agents to self-hosted engines that scrape public data, run deterministic quality checks, and give teams complete control over their enrichment pipelines and data governance.

**Examples** include ZoomInfo, Clearbit, Apollo.io, Clay, People Data Labs, Lusha, LeadIQ, Openprise, Cognism, and HubSpot AI Data Agent (the category leaders in commercial space).

**Open-source emphasis**: This section is expanded with every relevant project for self-hosted enrichment, data quality, and open data infrastructure. **Critical note**: The open-source landscape splits into two distinct categories—**B2B enrichment engines** (FORGE, b2b-lead-intelligence) that scrape and verify business data from public sources, and **data quality frameworks** (DataGuard AI, DataCleaner, Truthound) that validate, profile, and cleanse datasets. No open-source project matches ZoomInfo's verified contact database or Clearbit's real-time enrichment API at scale.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[ZoomInfo](https://www.zoominfo.com/)**
  **B2B contact and company intelligence platform** with the largest verified contact database. **Pricing**: Quote-only; annual contracts. **Free tier**: Limited trial. **Best for**: sales and marketing teams needing broad B2B prospecting and enrichment with verified emails and direct dials.

- **[Clearbit](https://clearbit.com/)** (HubSpot)
  **Data enrichment and intelligence API** for company and person data with real-time enrichment. **Pricing**: Usage-based API pricing; quote for enterprise. **Free tier**: Limited free tier. **Best for**: product and growth teams wanting real-time enrichment via API for lead routing and personalization.

- **[Apollo.io](https://www.apollo.io/)**
  **B2B sales intelligence and outbound platform** with 240M+ contacts and enrichment capabilities. **Pricing**: Free tier; paid from $49/user/month (annual). **Free tier**: Yes, limited credits. **Best for**: teams wanting a combined database and enrichment workflow with autonomous sequences.

- **[Clay](https://www.clay.com/)**
  **Data enrichment and workflow automation** platform with waterfall enrichment across multiple providers and AI-powered personalization. **Pricing**: Free tier; paid plans by credits. **Free tier**: Yes, limited credits. **Best for**: growth teams wanting to chain multiple enrichment providers and automate personalized outreach.

- **[People Data Labs](https://www.peopledatalabs.com/)**
  **Person and company data enrichment API** with a large global dataset. **Pricing**: Credit-based API pricing. **Free tier**: Trial credits. **Best for**: developers wanting flexible API access to people and company data for enrichment pipelines.

- **[Lusha](https://www.lusha.com/)**
  **B2B contact enrichment** with browser extension and CRM integrations. **Pricing**: Free tier; paid plans per user. **Free tier**: Yes, limited credits. **Best for**: individual sales reps and small teams wanting quick contact lookups.

- **[LeadIQ](https://leadiq.com/)**
  **Sales prospecting and enrichment** with contact capture and CRM sync. **Pricing**: Free tier; paid plans per user. **Free tier**: Yes, limited. **Best for**: SDR teams wanting to capture and enrich leads during prospecting.

- **[Openprise](https://www.openprisetech.com/)**
  **Data orchestration and enrichment** platform with automated data quality workflows for RevOps. **Pricing**: Quote-only. **Free tier**: None. **Best for**: RevOps teams wanting automated data cleansing, enrichment, and routing across the revenue stack.

- **[Cognism](https://www.cognism.com/)**
  **B2B sales intelligence** with GDPR-compliant contact data and enrichment. **Pricing**: Quote-only. **Free tier**: None. **Best for**: European teams needing compliant B2B contact data with enrichment.

- **[HubSpot AI Data Agent](https://www.hubspot.com/)**
  **AI-powered data enrichment** within HubSpot Smart CRM. **Pricing**: Included with HubSpot paid tiers. **Free tier**: Limited. **Best for**: HubSpot users wanting native AI enrichment without third-party tools.

## Open-Source GitHub Projects

- **[FORGE (dataforge)](https://github.com/Nuclear-Marmalade/dataforge)**
  **Free open-source business data enrichment engine** (license per repo) — **the most complete open-source alternative to Apollo, ZoomInfo, and Clearbit** found in this research . **Features**: **Email extraction** via 6 layers (mailto links, regex, Cloudflare decode, JSON-LD, obfuscation decode, contact page crawl); **SMTP verification** without sending mail; **tech stack detection** (30+ technologies: WordPress, Shopify, React, Next.js, Stripe, Intercom, etc.); **government data importers** (FCC ULS ~3M telecom records, NPI Registry ~7M healthcare providers, SAM.gov ~900K federal contractors); **local AI enrichment** via Ollama (business summaries, industry classification, health scores, pain points) with no API costs; quality checks with COALESCE writes (never clobber existing data) and rollback support . **Architecture**: Two parallel tracks—web scraping (~16K records/hr with 4 workers) and AI enrichment (~7-20K/day depending on hardware)—both using COALESCE writes and checkpointing after every batch . **Tech stack**: Python, PostgreSQL, Ollama (local AI). **Deploy**: Self-hosted (`pip install forge-enrichment`; CLI or dashboard). **Trade-off**: **Scraping-based, not a verified database**—coverage depends on what's publicly available on websites and government records. No proprietary contact database. Email verification is SMTP-based (RCPT TO), not a verified deliverability guarantee. **Best for**: teams wanting free, self-hosted B2B enrichment without per-record API costs—especially for local businesses, healthcare providers, and federal contractors available in government datasets.

- **[DataGuard AI](https://pypi.org/project/dataguard-ai/)**
  **AI-assisted data quality scanning and validation framework** (license per PyPI) — **the most comprehensive open-source data quality tool** found in this research, with deterministic checks and optional AI explanations . **Features**: **YAML rule engine** (not_null, unique, accepted_values, between, regex, max_null_pct, row_count_between); **schema drift detection** (snapshot baseline, compare against new data); **data contracts** generation; **dbt test generation**; **Great Expectations config export**; **PII detection**; HTML/JSON reports with quality/governance scores and suggested remediation; **database scanning** (DuckDB, PostgreSQL); **GitHub Actions** integration . **Detection philosophy**: "AI assists; deterministic and statistical checks detect and verify"—the default scanning path does not require an LLM, keeping findings reproducible and avoiding sending raw production data to external models . **Tech stack**: Python. **Deploy**: CLI (`dataguard scan data.csv`; `dataguard drift data_v2.csv --baseline baseline.json`). **Trade-off**: **Quality validation, not enrichment**—it profiles and checks data you already have; it does not add missing fields from external sources. Database scans load tables into memory (warehouse-scale pushdown is roadmap). **Best for**: data teams wanting deterministic, reproducible data quality checks with optional AI-assisted explanations—especially teams already using dbt or Great Expectations.

- **[DataCleaner](https://github.com/datacleaner/DataCleaner)**
  **Premier open source Data Quality solution** (LGPL) — **the most established open-source data quality toolkit**, maintained but not actively developed . **Features**: Profile, correct, and enrich data; ad-hoc analysis and recurring cleansing; "swiss-army knife" for matching and Master Data Management solutions. Module structure includes API, engine core, and desktop Swing UI . **Tech stack**: Java. **Deploy**: Desktop application or engine library. **Trade-off**: **Maintained but not actively developed**—new features are driven by pull requests only . Java desktop UI may feel dated. Not a modern API-first tool. **Best for**: organizations with existing Java infrastructure wanting a proven, stable data quality toolkit for profiling and cleansing—accepting slower feature velocity.

- **[Truthound](https://pypi.org/project/truthound/)**
  **Polars-based data validation framework and workflow orchestration** (license per PyPI) — **the fastest open-source data quality framework**, claiming 2.66x speedup and 44% memory reduction vs. Great Expectations in historical benchmarks . **Features**: **Zero-configuration** (`th.check(data)` creates a workspace automatically); deterministic auto-validation suite (schema, nullability, types, ranges, key heuristics—selects only needed checks, not "run everything"); single `ValidationRunResult` model shared by checkpoints, reporters, and plugins; **workflow integration** via Truthound Orchestration (Airflow, Dagster, Prefect, dbt, Mage, Kestra); optional AI review layer (prompt-based validation suggestions, human-reviewed) . **Tech stack**: Python (Polars). **Deploy**: CLI and library (`pip install truthound`). **Trade-off**: **Validation framework, not enrichment**—it checks data quality against contracts and heuristics; it does not add external data. AI is optional and human-reviewed, not autonomous. **Best for**: data engineers wanting fast, deterministic validation that integrates with modern workflow orchestrators—especially teams already using Polars or frustrated with Great Expectations' performance.

- **[Tracardi](https://github.com/tracardi/tracardi)**
  **API-first composable open-source Customer Data Platform** (MIT with Common Clause) — **the most complete open-source CDP for customer data unification and enrichment workflows** . **Features**: **Collect, ingest, aggregate, and store customer data** from multiple sources in real time; **model customer data** with rules that transform page data into user profiles; **unify profiles** by merging customer data and eliminating duplicates; **personalize** with real-time frontend apps and marketing segmentation; **integrate internal systems** as a centralized orchestration hub; **social engagement** via Tracardi bridges; **scale e-commerce** as a headless, API-first platform . **Tech stack**: Python, Docker. **Deploy**: Self-hosted (`docker-compose up`; installation GUI at port 8787). **Trade-off**: **CDP infrastructure, not a B2B enrichment engine**—it unifies and enriches customer data you collect, but does not scrape external business data or verify emails like FORGE. **Best for**: teams wanting to build a self-hosted CDP with profile unification and real-time personalization—using their own first-party data, not purchasing B2B databases.

- **[b2b-lead-intelligence](https://pypi.org/project/b2b-lead-intelligence/)**
  **B2B Company & Decision-Maker Lead Intelligence SDK** (license per PyPI) — **a lightweight Python SDK positioned as an open-source Apollo/Proxycurl alternative** . **Features**: `enrich_company()` for firmographics and tech stack; `find_executives()` for decision-makers by department with email confidence scores; `get_hiring_signals()` for growth stage and hiring intent score . **Tech stack**: Python (`pip install b2b-lead-intelligence`). **Deploy**: SDK/CLI. **Trade-off**: **Minimal package (5.7 kB)**—extremely limited scope and validation. No indication of data sources or refresh cadence. Likely a thin wrapper or demo, not a production enrichment engine. **Best for**: developers wanting to explore a simple B2B enrichment SDK API pattern—**not for production use without verifying data quality and coverage**.

- **[Span](https://pypi.org/project/span-data/)**
  **Customer data resolution and unification library** (license per PyPI, active development) — **the most focused open-source identity resolution tool** . **Features**: **ID Graph** built on Splink and DuckDB—links records referring to the same entity across datasets and produces a unified ID graph keyed on `profile_id`; **Customer 360 compiler**—merges demographics from multiple sources with configurable waterfall precedence, computes rolling-window metrics (6/12/lifetime), builds consent fact tables, generates customer segments; **manual override workflows** for merge/split/assign; exports to DataFrames, CSV, Parquet, DuckDB, Snowflake . **Tech stack**: Python (Splink, DuckDB). **Deploy**: CLI (`span-data run span_config.yaml`) or library. **Trade-off**: **Identity resolution, not enrichment**—it resolves who is who across your data; it does not add missing firmographic or contact fields from external sources. **Best for**: data teams needing probabilistic identity resolution and Customer 360 unification across multiple first-party data sources—without a commercial CDP.

### Additional Strong Open-Source Options

- **HoloClean** — Machine learning system for data enrichment (Python, ~516 stars). **Note**: Academic ML project for data repair; last pushed over a year ago . **Best for**: researchers exploring ML-based data cleaning, not production enrichment.
- **miniMDM** — Minimal Master Data Management application (Python, PostgreSQL). Lifecycle states, config-based validation, audit log, webhook receiver, RBAC . **Note**: MDM governance, not enrichment—manages master records but does not add external data. **Best for**: teams needing lightweight MDM for customer master data governance.
- **DataForge** *(see FORGE above)* — The most practical open-source B2B enrichment engine for teams wanting free, self-hosted enrichment from public sources.

**Frameworks for building custom systems**: Combine **FORGE** for B2B data enrichment from public sources with **DataGuard AI** or **Truthound** for quality validation, **Span** for identity resolution across datasets, and **Tracardi** for CDP-level profile unification—creating an open-source data quality and enrichment stack. **None of these match ZoomInfo's verified contact database or Clearbit's real-time enrichment API**; those require commercial platforms or significant data acquisition and verification infrastructure.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Data quality and enrichment platforms handling personal and business data must comply with data protection regulations (GDPR, CCPA, etc.) and respect website terms of service when scraping. Email verification via SMTP (RCPT TO) may trigger spam filters if misused.
- **The "B2B enrichment engine" vs. "data quality framework" vs. "identity resolution" vs. "CDP" distinction is critical.** **FORGE** and **b2b-lead-intelligence** are **B2B enrichment engines**—they add missing business data from external sources . **DataGuard AI, Truthound, and DataCleaner** are **data quality frameworks**—they validate and cleanse data you already have . **Span** is **identity resolution**—it links records across your datasets . **Tracardi** is a **CDP**—it unifies customer profiles from first-party data . **No open-source project provides a turnkey ZoomInfo or Clearbit replacement.**
- **FORGE is the most practical open-source B2B enrichment option**—it scrapes public sources, imports government records, and verifies emails without API costs . **The trade-off**: coverage depends on public data, not a proprietary verified database. It will not match ZoomInfo's email accuracy or direct dial coverage. **For local businesses, healthcare providers, and federal contractors, government datasets provide strong coverage; for enterprise B2B contacts, coverage will be thinner.**
- **DataGuard AI is the most comprehensive open-source data quality tool** with deterministic checks, schema drift detection, and dbt/Great Expectations integration . **Truthound** is the performance-focused alternative for Polars users. **DataCleaner** is the established but aging option—maintained, not actively developed .
- **Span is the most focused open-source identity resolution tool**, using Splink for probabilistic matching and DuckDB for processing . **The trade-off**: it resolves identities within your data; it does not enrich with external data.
- **b2b-lead-intelligence is a tiny package (5.7 kB)**—treat it as an API pattern reference, not a production enrichment engine. No evidence of a real data pipeline or refresh cadence.
- **Pricing opacity varies.** ZoomInfo, Clearbit (enterprise), Clay (enterprise), People Data Labs (volume), Openprise, and Cognism require sales contact. Apollo, Lusha, and LeadIQ publish tiered pricing with free tiers. HubSpot includes AI Data Agent in paid tiers. **Validate with direct vendor conversations against your actual enrichment volume and data quality requirements.**
- Self-hosted open-source solutions require proper infrastructure (PostgreSQL for FORGE, Docker for Tracardi), scraping compliance review, and ongoing maintenance. **Scraping websites without authorization may violate terms of service**—ensure your enrichment pipelines comply with applicable laws and site policies before running at scale.

---

**Made for developers, RevOps teams, and organizations building transparent data quality and enrichment solutions.**
Let's make Automated Data Quality & Enrichment more open, data-driven, and enrichment-efficient.
