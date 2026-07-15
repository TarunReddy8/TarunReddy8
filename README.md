# Hi, I'm Tarun Kumar Reddy Nallagari 👋

**AI/ML Engineer** — I build production LLM, RAG, and MLOps systems in regulated industries (banking & healthcare), where "it works in the demo" isn't good enough.

- 🏦 Currently: AI/ML Engineer at **Ally Financial** — RAG knowledge assistant for 2,000+ customer-care agents on Azure OpenAI, with the guardrails, evals, and monitoring that got it past a bank's model risk office
- 🎓 MS in Data Science, University at Buffalo · previously data engineering at **Optum** (2+ TB/day claims pipelines on Spark/Databricks)
- 🔧 I care about the unglamorous parts that make LLM systems shippable: **evaluation, grounding, cost control, and audit trails**

## Featured projects

### [evalsmith](https://github.com/TarunReddy8/evalsmith) — CI for LLM quality
[![CI](https://github.com/TarunReddy8/evalsmith/actions/workflows/ci.yml/badge.svg)](https://github.com/TarunReddy8/evalsmith/actions/workflows/ci.yml)

Evaluation framework for LLM/RAG apps: faithfulness, relevance, and safety scoring (LLM-as-judge or offline heuristics), with **regression gates** — commit a baseline, and any prompt or model change that drops quality fails the build, with a per-case HTML report showing exactly which answers regressed.

### [ClaimSight](https://github.com/TarunReddy8/claimsight) — multi-agent claims processing
[![CI](https://github.com/TarunReddy8/claimsight/actions/workflows/ci.yml/badge.svg)](https://github.com/TarunReddy8/claimsight/actions/workflows/ci.yml)

Turns a folder of raw claim documents into an audit-ready decision packet: LLM extraction with **verified citations** (hallucinated quotes get caught), a deterministic 9-rule policy engine, and a hash-chained tamper-evident audit trail. LLMs only where they add value — decisions stay reproducible code.

### [APSentry](https://github.com/TarunReddy8/apsentry) — AP invoice screening with backtested detectors
[![CI](https://github.com/TarunReddy8/apsentry/actions/workflows/ci.yml/badge.svg)](https://github.com/TarunReddy8/apsentry/actions/workflows/ci.yml)

Screens accounts-payable invoices with a **3-way match** (invoice vs PO vs goods receipt) plus statistical fraud detectors: duplicates (exact & fuzzy), price outliers via vendor-history z-scores, bank-detail changes, and threshold gaming. Detector **precision/recall are measured on a labeled synthetic population and gated at 90% in CI** — detector quality as a regression-tested property.

> These projects work together: ClaimSight's CI uses evalsmith to gate its LLM-written narratives for faithfulness. Build → evaluate → ship.

🚧 Next up: **TokenGate** — a self-hosted LLM gateway with semantic caching, complexity-based model routing, and per-team cost budgets.

## Tech I work with

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?logo=langchain&logoColor=white)
![Azure OpenAI](https://img.shields.io/badge/Azure_OpenAI-0078D4?logo=microsoftazure&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?logo=amazonwebservices&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![Spark](https://img.shields.io/badge/Apache_Spark-E25A1C?logo=apachespark&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?logo=databricks&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?logo=apachekafka&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?logo=apacheairflow&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?logo=snowflake&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?logo=mlflow&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?logo=terraform&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?logo=grafana&logoColor=white)

## Reach me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/tarun-kumar-reddy-nallagari-27b408218/)
[![Email](https://img.shields.io/badge/Email-EA4335?logo=gmail&logoColor=white)](mailto:ntarunreddywork@gmail.com)

📍 Buffalo, NY · open to AI/ML engineering roles
