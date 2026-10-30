# Awesome Automated Data Quality & Enrichment [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Curated directory of SaaS platforms, enterprise solutions, and open-source GitHub projects focused on B2B data enrichment, automated data quality validation, identity resolution, data profiling, and intelligent cleansing.

[![GitHub stars](https://img.shields.io/github/stars/ishandutta2007/Awesome-Automated-Data-Quality-Enrichment?style=social)](https://github.com/ishandutta2007/Awesome-Automated-Data-Quality-Enrichment/stargazers)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/ishandutta2007/Awesome-Automated-Data-Quality-Enrichment/pulls)

Modern revenue operations (RevOps), data engineering, and machine learning teams require reliable, continuous data pipelines. This repository tracks the leading commercial SaaS products and open-source GitHub libraries across **B2B contact and firmographic enrichment**, **waterfall API lookups**, **schema validation**, **entity matching / identity resolution**, and **AI-powered data cleansing**.

---

## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS & Hosted Enrichment Platforms](#saas--hosted-enrichment-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [Categorization Breakdown](#categorization-breakdown)
- [How to Choose Your Stack](#how-to-choose-your-stack)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

---

## Sector Overview & Market Dynamics

The global **B2B Data Enrichment** market is estimated at **$2.8B–$3.1B** growing at ~10.1% CAGR, while the complementary **Data Quality & Governance Tools** market is valued at **$2.8B–$3.9B** and expanding at **15%–19% CAGR** toward $15B+ by 2032 due to enterprise generative AI and automated pipeline requirements. 

The sector exhibits a **polarized market structure**:
- **Data Quality & Master Data Management (MDM):** Moderately concentrated and steadily consolidating, dominated by entrenched enterprise infrastructure providers (such as Salesforce/Informatica, IBM, and SAP) alongside standard open-source validation protocols.
- **B2B Sales Intelligence & Contact Enrichment:** Highly fragmented at the provider level, featuring hundreds of specialized data brokers for firmographics, technographics, intent data, and local compliance. While giants like ZoomInfo, Apollo.io, and HubSpot anchor market share, no single database achieves complete coverage; hence, the market is rapidly pivoting toward **meta-orchestration and waterfall enrichment** platforms (e.g., Clay) that programmatically query across multiple providers.

---

## SaaS & Hosted Enrichment Platforms

The table below benchmarks commercial SaaS data quality and enrichment platforms. It is ranked by company scale (market valuation / enterprise market cap in descending order), with exact starting tier pricing and specific free-tier or trial limitations.

| Platform | Company Scale (Valuation / Revenue) | Primary Focus | Starting Paid Price | Free Tier / Free Trial Limits | Key Capabilities |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **[HubSpot](https://www.hubspot.com/)** | **~$28.0B** Market Cap (~$2.5B+ ARR) | CRM Platform & Breeze Intelligence | **$20/mo/seat** (Starter Customer Platform; ~$7/mo promo) | **Free forever plan** includes core CRM & Breeze Assistant. *Data Agent & Breeze Intelligence require paid tiers* (includes 500 shared credits/mo on Starter). | Native AI data agent, CRM deduplication, automated firmographic backfill, buyer intent signals. |
| **[Clay](https://www.clay.com/)** | **~$7.1B** Valuation (~$100M–$200M ARR) | Waterfall Enrichment & AI Data Orchestration | **$185/mo** (Launch plan; $167/mo billed annually) | **Free forever plan**: 100 data credits/mo, 500 action automations/mo, 200 rows max per table, unlimited team seats. | Cascading waterfall lookups across 150+ data vendors, autonomous AI web scrapers, dynamic outbound enrichment. |
| **[Apollo.io](https://www.apollo.io/)** | **~$1.6B** Valuation (~$250M ARR) | B2B Sales Intelligence & Outbound CRM | **$49/user/mo** billed annually ($59/mo monthly; Basic tier) | **Free forever plan**: 50 credits/month (email reveals), 10 export credits/month, 250 sequence emails/day, basic search filters. | 275M+ buyer contact database, built-in email sequencer, automated phone number verification, CRM bi-directional sync. |
| **[ZoomInfo](https://www.zoominfo.com/)** (NASDAQ: GTM) | **~$1.2B** Market Cap (~$1.2B ARR) | Enterprise B2B Contact & Intent Intelligence | **~$12,500/year** (Professional tier, annual contract) | **7-day free trial** available via sales consultation (limited search views, no bulk exports). No permanent self-serve free tier. | Enterprise verified contact coverage, org chart tracking, real-time website visitor resolution, intent signals. |
| **[Lusha](https://www.lusha.com/)** | **~$500M+** Valuation (~$50M+ ARR) | B2B Contact Intelligence & Phone Reveal | **$37.45/user/mo** billed annually ($49/mo monthly; Starter tier) | **Free forever plan**: 40 credits/mo (1 user seat), up to 100 CSV rows enrichment per batch. *Credits do not roll over.* | Chrome prospecting extension, direct-dial phone lookups, GDPR-compliant contact lists, CRM automated sync. |
| **[Clearbit](https://clearbit.com/)** *(HubSpot)* | **$150M** Acquisition Price (~$31M ARR) | Real-time Enrichment API & Identity Resolution | **$20/mo/seat** (Integrated as HubSpot Breeze Intelligence) | **No standalone free tier** (legacy free APIs retired). Included with HubSpot paid tiers (Starter gets 500 credits/mo). | Real-time IP-to-company reverse lookup, form shortening APIs, automated demographic enrichment for RevOps. |
| **[Cognism](https://www.cognism.com/)** | **~$100M+** Funding (~$40M ARR) | EMEA Compliance & Sales Intelligence | **~$15,000/year** (Grow plan base platform fee + per seat) | **No self-serve free tier/trial**. Provides **25–50 verified sample lead records** upon completed sales demo. | Phone-verified mobile data (Diamond Data), Do-Not-Call (DNC) list checking across EMEA & US, GDPR-first compliance. |
| **[Openprise](https://www.openprisetech.com/)** | **~$50M+** Funding (~$25M ARR) | Enterprise RevOps Orchestration & Data Hygiene | **~$35,000/year** (Platform enterprise license) | **No free tier or public self-serve trial**; private sandbox environment provided during enterprise evaluations. | Full RevOps pipeline automation, multi-vendor data normalization, lead-to-account matching, deduplication. |
| **[People Data Labs](https://www.peopledatalabs.com/)** | **~$40M+** Funding (~$20M ARR) | Developer Data Enrichment & Identity APIs | **$98/mo** billed annually (Pro Person Data, ~350 credits/mo) | **Free forever developer sandbox**: 100 API queries/month (contact data such as phone and email strictly masked/obfuscated). | 3B+ person profiles, raw JSON APIs, SQL/Elasticsearch database feeds, tech stack and company entity resolution. |
| **[LeadIQ](https://leadiq.com/)** | **~$35M+** Funding (~$15M ARR) | In-Workflow Prospecting & Contact Cleansing | **$15/user/mo** billed annually ($20/mo monthly; Pro tier) | **Free forever plan**: 50 universal credits/mo for 1 user, Chrome extension capture, basic email enrichment. | LinkedIn prospecting capture, 1-click CRM export, email deliverability validation, automated account routing. |

---

## Open-Source GitHub Projects

The following open-source frameworks provide self-hosted tools for data validation, entity resolution, data profiling, automated cleansing, and public data enrichment. 

Sorted by **GitHub Star Count** (descending):

| Project | Stars | Category | Core Tech Stack | Description & Highlights |
| :--- | :---: | :--- | :--- | :--- |
| **[OpenRefine](https://github.com/OpenRefine/OpenRefine)** | [![OpenRefine Stars](https://img.shields.io/github/stars/OpenRefine/OpenRefine?style=social&color=white)](https://github.com/OpenRefine/OpenRefine/stargazers) | Data Cleansing & Transformation | Java, Web UI | The industry standard open-source desktop tool for exploring, cleaning, and transforming messy tabular data with GREL expressions and reconciliation APIs. |
| **[Great Expectations](https://github.com/great-expectations/great_expectations)** | [![Great Expectations Stars](https://img.shields.io/github/stars/great-expectations/great_expectations?style=social&color=white)](https://github.com/great-expectations/great_expectations/stargazers) | Data Quality & Testing Framework | Python, SQL, Spark | Leading framework for automated data testing, continuous quality profiling, data documentation, and pipeline integration (dbt, Airflow, Snowflake). |
| **[Cleanlab](https://github.com/cleanlab/cleanlab)** | [![Cleanlab Stars](https://img.shields.io/github/stars/cleanlab/cleanlab?style=social&color=white)](https://github.com/cleanlab/cleanlab/stargazers) | AI/ML Data Quality & Label Cleaning | Python, PyTorch | Machine learning data-centric AI library to detect label errors, identify outliers, curate clean training sets, and audit tabular, text, and audio datasets. |
| **[Dedupe](https://github.com/dedupeio/dedupe)** | [![Dedupe Stars](https://img.shields.io/github/stars/dedupeio/dedupe?style=social&color=white)](https://github.com/dedupeio/dedupe/stargazers) | Record Linkage & Deduplication | Python, C++ | Machine-learning-based deduplication and entity resolution library that learns fuzzy matching rules interactively from user feedback. |
| **[Splink](https://github.com/moj-analytical-services/splink)** | [![Splink Stars](https://img.shields.io/github/stars/moj-analytical-services/splink?style=social&color=white)](https://github.com/moj-analytical-services/splink/stargazers) | Identity Resolution & Linkage | Python, DuckDB, Spark | Ultra-fast probabilistic record linkage at scale using the Fellegi-Sunter methodology; native push-down support for DuckDB, AWS Athena, and Spark. |
| **[Soda Core](https://github.com/sodadata/soda-core)** | [![Soda Core Stars](https://img.shields.io/github/stars/sodadata/soda-core?style=social&color=white)](https://github.com/sodadata/soda-core/stargazers) | Metric-Based Quality Validation | Python, SodaCL | Modern CLI and Python library that uses declarative YAML checks (SodaCL) to monitor schema drift, freshness, missing values, and query results. |
| **[DataProfiler](https://github.com/capitalone/DataProfiler)** | [![DataProfiler Stars](https://img.shields.io/github/stars/capitalone/DataProfiler?style=social&color=white)](https://github.com/capitalone/DataProfiler/stargazers) | Data Profiling & Sensitive PII Detection | Python, TensorFlow | Capital One's library designed to scan schemas, profile column statistics, and classify sensitive PII information across unstructured and tabular data. |
| **[Frictionless](https://github.com/frictionlessdata/frictionless-py)** | [![Frictionless Stars](https://img.shields.io/github/stars/frictionlessdata/frictionless-py?style=social&color=white)](https://github.com/frictionlessdata/frictionless-py/stargazers) | Data Contracts & Tabular Validation | Python | Data validation and packaging toolkit built on the open Frictionless Specs; checks structural schemas and generates portable data contracts. |
| **[Tracardi](https://github.com/tracardi/tracardi)** | [![Tracardi Stars](https://img.shields.io/github/stars/tracardi/tracardi?style=social&color=white)](https://github.com/tracardi/tracardi/stargazers) | Open-Source CDP & Profile Unification | Python, Docker | Composable Customer Data Platform engine for real-time customer event tracking, identity merging, data enrichment rules, and marketing automation. |
| **[DataCleaner](https://github.com/datacleaner/DataCleaner)** | [![DataCleaner Stars](https://img.shields.io/github/stars/datacleaner/DataCleaner?style=social&color=white)](https://github.com/datacleaner/DataCleaner/stargazers) | Profiling & Master Data Management | Java, Swing UI | Established data profiling and cleansing application designed for entity matching, fuzzy standardization, and corporate master data management (MDM). |
| **[FORGE (dataforge)](https://github.com/Nuclear-Marmalade/dataforge)** | [![Dataforge Stars](https://img.shields.io/github/stars/Nuclear-Marmalade/dataforge?style=social&color=white)](https://github.com/Nuclear-Marmalade/dataforge/stargazers) | Public B2B Enrichment Engine | Python, PostgreSQL | Complete self-hosted B2B enrichment pipeline with 6-layer email extraction, non-sending SMTP verification, tech stack discovery, and local AI (Ollama). |
| **[Truthound](https://github.com/seadonggyun4/Truthound)** | [![Truthound Stars](https://img.shields.io/github/stars/seadonggyun4/Truthound?style=social&color=white)](https://github.com/seadonggyun4/Truthound/stargazers) | High-Performance Polars Validation | Python, Polars | High-speed data contract and quality validation framework claiming up to 2.6x speedups over Great Expectations via Polars; integrates with Airflow & Dagster. |
| **[b2b-lead-intelligence-api](https://github.com/meanusarcanus/b2b-lead-intelligence-api)** | [![b2b-lead-intelligence-api Stars](https://img.shields.io/github/stars/meanusarcanus/b2b-lead-intelligence-api?style=social&color=white)](https://github.com/meanusarcanus/b2b-lead-intelligence-api/stargazers) | Headless Lead Intelligence SDK | Python | Lightweight developer SDK and API wrapper pattern for firmographic lookups, decision-maker extraction, and hiring growth signals. |

---

## Categorization Breakdown

To choose the right tooling, distinguish between the four fundamental layers of data quality and enrichment:

1. **B2B Enrichment Engines & Waterfall Aggregators**
   - *Commercial:* **Clay**, **Apollo.io**, **ZoomInfo**, **Clearbit**, **People Data Labs**.
   - *Open Source:* **FORGE**, **b2b-lead-intelligence-api**.
   - *Function:* Look up external phone numbers, verified email addresses, revenue estimates, and technographics to append missing data onto leads.
2. **Deterministic Data Quality & Contract Testing**
   - *Open Source:* **Great Expectations**, **Soda Core**, **Truthound**, **Frictionless**.
   - *Function:* Enforce expectations, schema contracts, null value limits, and anomalies in ETL/ELT pipelines before writing to data warehouses.
3. **Identity Resolution, Deduplication & Entity Matching**
   - *Commercial:* **Openprise**, **ZoomInfo RingLead**.
   - *Open Source:* **Splink**, **Dedupe**, **OpenRefine**.
   - *Function:* Probabilistically link disparate records, merge duplicated contacts, and maintain a clean single source of truth (Customer 360).
4. **Data-Centric AI & Automated Cleansing**
   - *Open Source:* **Cleanlab**, **DataProfiler**, **Tracardi**.
   - *Function:* Find label errors in training data, flag corrupted rows, profile sensitive PII, and build automated CDP cleansing graphs.

---

## How to Choose Your Stack

```
                          ┌────────────────────────────┐
                          │   Need External B2B Data?   │
                          └─────────────┬──────────────┘
                                        │
                         ┌──────────────┴──────────────┐
                        YES                            NO
                         │                             │
          ┌──────────────┴─────────────┐         ┌─────┴───────────────────────┐
          │  Proprietary Data Needed?   │         │  What is the primary need?  │
          └───────┬─────────────┬──────┘         └─────┬───────────────┬───────┘
                 YES            NO                     │               │
                  │              │               [Validation]     [Identity]
         ┌────────┴───────┐  ┌───┴──────────┐          │               │
         │ Commercial API │  │ Open Source  │          ▼               ▼
         │ Clay, Apollo,  │  │ FORGE, Govt  │   Great Expect.    Splink, Dedupe
         │ ZoomInfo, Lusha│  │ Open Data    │   Soda Core        OpenRefine
         └────────────────┘  └──────────────┘   Truthound
```

- **For High-Volume Outbound Sales Teams:** Pair a commercial aggregator like **Clay** or **Apollo.io** with **Lusha** for direct dials.
- **For Modern Data Engineering (Analytics & Warehousing):** Standardize on **Great Expectations** or **Soda Core** for pipeline quality tests with **Splink** for identity resolution across data warehouse models.
- **For Low-Cost / Privacy-First Enrichment:** Deploy **FORGE** locally with PostgreSQL and Ollama, paired with **OpenRefine** or **Cleanlab** for data cleaning.

---

## How to Contribute

Contributions are welcome! Please feel free to submit a pull request:

1. **Fork this repository** to your GitHub account.
2. **Add or update entries** following the tabular or formatted layout:
   - For SaaS tools: include verified starting prices, exact free tier / trial conditions, and company scale metrics.
   - For Open-Source projects: provide the GitHub repository, star badge (`style=social&color=white`), license, and core use cases.
3. **Submit a Pull Request** with a descriptive summary of your updates.

---

## Disclaimer

- This list is community-curated for technical and business evaluation.
- Pricing, free tiers, and API terms change regularly. Always confirm exact licensing and quota limits directly with vendors before building commercial integrations.
- Scraping public websites, SMTP verification (RCPT TO), and automated lead ingestion must always comply with applicable data protection regulations (including GDPR, CCPA/CPRA, and CAN-SPAM) and third-party terms of service.
