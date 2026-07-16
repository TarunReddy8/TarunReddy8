# Hi, I'm Tarun Kumar Reddy Nallagari 👋

**AI/ML Engineer** · Buffalo, NY · building production LLM, RAG, and MLOps systems where *"it works in the demo"* isn't good enough.

🌐 **Portfolio:** [tarunreddy8.github.io](https://tarunreddy8.github.io/) — 💼 [LinkedIn](https://www.linkedin.com/in/tarun-kumar-reddy-nallagari-27b408218/) — ✉️ [ntarunreddywork@gmail.com](mailto:ntarunreddywork@gmail.com)

---

## My story: from moving data to building the AI on top of it

I started out in **Bengaluru, India**, as a **Data Engineer at Optum (UnitedHealth Group)** — the plumbing years, and I mean that as a compliment. I built PySpark pipelines that moved **2+ TB of medical and pharmacy claims every day** on Databricks, migrated 100+ legacy Hive workloads (60% faster, ~40% cheaper), stood up near-real-time Kafka ingestion, and enforced HIPAA-grade controls across Delta Lake and Snowflake. I learned what "production" actually costs: SLAs, data quality gates, the pager at 3 AM. Data engineering taught me that a system is only as good as its worst day.

Then generative AI changed what was possible on top of that data — so I moved, in two senses. I came to the **United States** for an **MS in Data Science at the University at Buffalo (SUNY)**, and I moved up the stack from *moving* data to *reasoning* over it.

Today I'm an **AI/ML Engineer at Ally Financial in New York** 🇺🇸, where I built a **RAG knowledge assistant for 2,000+ customer-care agents** on Azure OpenAI — with the guardrails, evaluation harness, and monitoring that got it past a **bank's model risk office**. It cut agent handle time 14%, LLM spend ~35%, and holds p95 under 800 ms at 50K requests a day.

The through-line from Optum to Ally is the same instinct: **the unglamorous parts are what make AI shippable** — evaluation, grounding, cost control, audit trails. My data-engineering years are why my AI systems have tests, gates, and monitoring instead of just a nice demo.

> **Bengaluru → Buffalo. Data Engineer → AI Engineer. Moving data → building the intelligence on top of it.**

---

## The work: four systems, one philosophy — *build → evaluate → ship*

I ship my thinking in the open. Each project solves a real business problem **and** proves a different discipline. They even reference each other.

### 🧪 [evalsmith](https://github.com/TarunReddy8/evalsmith) — CI for LLM quality
[![CI](https://github.com/TarunReddy8/evalsmith/actions/workflows/ci.yml/badge.svg)](https://github.com/TarunReddy8/evalsmith/actions/workflows/ci.yml)

My data-engineering reflex applied to LLMs: *if you can't measure it, you can't ship it.* An evaluation framework scoring faithfulness, relevance, and safety (LLM-as-judge or offline heuristics), with **regression gates** — commit a baseline, and any prompt or model change that drops quality **fails the build**, with a per-case HTML report showing exactly which answers regressed.

### 🏥 [ClaimSight](https://github.com/TarunReddy8/claimsight) — multi-agent claims processing
[![CI](https://github.com/TarunReddy8/claimsight/actions/workflows/ci.yml/badge.svg)](https://github.com/TarunReddy8/claimsight/actions/workflows/ci.yml)

Straight from my healthcare-claims roots, now with agents. Turns a folder of raw claim documents into an **audit-ready decision packet**: LLM extraction with *verified citations* (hallucinated quotes get caught), a deterministic 9-rule policy engine, and a hash-chained tamper-evident audit trail. LLMs only where they add value — the decision itself stays reproducible code. **Its narratives are gated by evalsmith in CI.**

### 💳 [APSentry](https://github.com/TarunReddy8/apsentry) — AP invoice screening with backtested detectors
[![CI](https://github.com/TarunReddy8/apsentry/actions/workflows/ci.yml/badge.svg)](https://github.com/TarunReddy8/apsentry/actions/workflows/ci.yml)

The fintech + statistics side. A **3-way match** (invoice vs PO vs goods receipt) plus fraud detectors: exact & fuzzy duplicates, price outliers via vendor-history z-scores, bank-detail changes, threshold gaming. Detector **precision/recall are measured on a labeled synthetic population and gated at 90% in CI** — detector quality treated as a regression-tested property, not a hope.

### 🎙️ [Voxa](https://github.com/TarunReddy8/voxa) — a fully local, low-latency voice AI agent
[![CI](https://github.com/TarunReddy8/voxa/actions/workflows/ci.yml/badge.svg)](https://github.com/TarunReddy8/voxa/actions/workflows/ci.yml)

The latency obsession, made personal. Talk to your computer with **zero cloud dependencies**: energy-based VAD, faster-whisper STT, streaming Ollama reasoning with native tool calls, and a **sentence-streamed Piper TTS pipeline that starts speaking while the model is still generating**. Per-turn latency breakdown built in, AST-safe tool execution, and an agent loop fully testable in CI without any hardware.

> 🚧 **Next:** *TokenGate* — a self-hosted LLM gateway with semantic caching, complexity-based model routing, and per-team cost budgets. Build → evaluate → **operate cheaply.**

---

## Tech I work with

**AI / ML**
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?logo=langchain&logoColor=white)
![Azure OpenAI](https://img.shields.io/badge/Azure_OpenAI-0078D4?logo=microsoftazure&logoColor=white)
![RAG](https://img.shields.io/badge/RAG-5eead4?logoColor=white)
![LLM Evaluation](https://img.shields.io/badge/LLM_Evaluation-818cf8?logoColor=white)

**MLOps / Cloud**
![AWS](https://img.shields.io/badge/AWS-232F3E?logo=amazonwebservices&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?logo=mlflow&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?logo=terraform&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?logo=grafana&logoColor=white)

**Data Engineering** *(where it started)*
![Spark](https://img.shields.io/badge/Apache_Spark-E25A1C?logo=apachespark&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?logo=databricks&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?logo=apachekafka&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?logo=apacheairflow&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?logo=snowflake&logoColor=white)

---

## GitHub stats

![Tarun's GitHub stats](https://github-readme-stats.vercel.app/api?username=TarunReddy8&show_icons=true&hide_border=true&theme=tokyonight&count_private=true)
![Top languages](https://github-readme-stats.vercel.app/api/top-langs/?username=TarunReddy8&layout=compact&hide_border=true&theme=tokyonight)

---

📍 **Buffalo, NY** · open to AI/ML engineering roles · let's build something that ships.
