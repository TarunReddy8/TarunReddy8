# Hi, I'm Tarun Kumar Reddy Nallagari 👋

**AI/ML Engineer** · building production LLM, RAG, and MLOps systems where *"it works in the demo"* isn't good enough.

🌐 **Portfolio:** [tarunreddy8.github.io](https://tarunreddy8.github.io/) — 💼 [LinkedIn](https://www.linkedin.com/in/tarun-kumar-reddy-nallagari-27b408218/) — ✉️ [ntarunreddywork@gmail.com](mailto:ntarunreddywork@gmail.com)

---

## My story: from moving data to building the AI on top of it

I started out as a **Data Engineer at Optum (UnitedHealth Group)** — the plumbing years, and I mean that as a compliment. I built PySpark pipelines that moved **2+ TB of medical and pharmacy claims every day** on Databricks, migrated 100+ legacy Hive workloads (60% faster, ~40% cheaper), stood up near-real-time Kafka ingestion, and enforced HIPAA-grade controls across Delta Lake and Snowflake. I learned what "production" actually costs: SLAs, data quality gates, the pager at 3 AM. Data engineering taught me that a system is only as good as its worst day.

Then generative AI changed what was possible on top of that data — so I moved up the stack. I earned an **MS in Data Science** and went from *moving* data to *reasoning* over it.

Today I'm an **AI/ML Engineer at Ally Financial**, where I built a **RAG knowledge assistant for 2,000+ customer-care agents** on Azure OpenAI — with the guardrails, evaluation harness, and monitoring that got it past a **bank's model risk office**. It cut agent handle time 14%, LLM spend ~35%, and holds p95 under 800 ms at 50K requests a day.

The through-line from Optum to Ally is the same instinct: **the unglamorous parts are what make AI shippable** — evaluation, grounding, cost control, audit trails. My data-engineering years are why my AI systems have tests, gates, and monitoring instead of just a nice demo.

> **Data Engineer → AI Engineer. From moving data to building the intelligence on top of it.**

---

## The work: five systems, one philosophy — *build → evaluate → ship*

I ship my thinking in the open. Each project solves a real business problem **and** proves a different discipline — several run on **real public data** (SEC EDGAR, FDA openFDA, CORD receipts), all green in CI.

### 🧪 [evalsmith](https://github.com/TarunReddy8/evalsmith) — CI for LLM quality
[![CI](https://github.com/TarunReddy8/evalsmith/actions/workflows/ci.yml/badge.svg)](https://github.com/TarunReddy8/evalsmith/actions/workflows/ci.yml)

My data-engineering reflex applied to LLMs: *if you can't measure it, you can't ship it.* An evaluation framework scoring faithfulness, relevance, and safety (LLM-as-judge or offline heuristics), with **regression gates** — commit a baseline, and any prompt or model change that drops quality **fails the build**, with a per-case HTML report showing exactly which answers regressed.

### 📈 [edgar-iq](https://github.com/TarunReddy8/edgar-iq) — financial-filing intelligence on real SEC data
[![CI](https://github.com/TarunReddy8/edgar-iq/actions/workflows/ci.yml/badge.svg)](https://github.com/TarunReddy8/edgar-iq/actions/workflows/ci.yml)

The financial side, on **real data**. Give it a ticker; it pulls the company's **real XBRL financials straight from SEC EDGAR** (free, no key), builds annual metric series with year-over-year moves, and computes **deterministic red-flag signals** (revenue decline, net loss, thin liquidity, high leverage) grounded in the actual filed numbers. The LLM writes the risk narrative but **never invents numbers** — metrics and flags are computed first, with a deterministic offline fallback, and tests assert on Apple's and Intel's real reported figures.

### 🩺 [fda-signal](https://github.com/TarunReddy8/fda-signal) — drug safety-signal detection on real FDA data
[![CI](https://github.com/TarunReddy8/fda-signal/actions/workflows/ci.yml/badge.svg)](https://github.com/TarunReddy8/fda-signal/actions/workflows/ci.yml)

The healthcare + statistics side, on **real data**. Runs the same **disproportionality analysis (PRR / ROR / chi-square)** regulators use for pharmacovigilance, over **real FDA adverse-event reports (openFDA / FAERS)**. From raw report counts alone it rediscovers known risks — e.g. metformin → **lactic acidosis, PRR 80.9** — using standard MHRA signalling thresholds. Statistics are computed before any LLM call; it runs fully offline against committed real fixtures, honestly flags that signals mean disproportional *reporting* not causation, and is **not medical advice**.

### 📄 [DocAI](https://github.com/TarunReddy8/Doc-AI-Flow) — AI document intelligence platform
[![CI/CD](https://github.com/TarunReddy8/Doc-AI-Flow/actions/workflows/ci.yml/badge.svg)](https://github.com/TarunReddy8/Doc-AI-Flow/actions/workflows/ci.yml)

The full-stack MLOps piece. Turns scanned receipts and documents into **structured JSON**: OCR (DocTR → Tesseract fallback) → **versioned-prompt LLM extraction** (OpenAI / Anthropic / Gemini / Groq, or a no-key mock mode) → **ChromaDB** semantic search. Real MLOps — **MLflow** experiment tracking, **drift detection**, and **prompt A/B testing** — with Prometheus monitoring, a Streamlit dashboard, Docker Compose, and extraction accuracy measured on **real CORD receipts**, 28 tests in CI.

### 🎧 [TriageIQ](https://github.com/TarunReddy8/triageiq) — autonomous support-triage agent
[![CI](https://github.com/TarunReddy8/triageiq/actions/workflows/ci.yml/badge.svg)](https://github.com/TarunReddy8/triageiq/actions/workflows/ci.yml)

The agentic-AI piece. An agent that reads a support ticket, gathers context with **tool-calling** (KB search, order/customer lookup), and routes it to **auto-resolve / review / escalate**. The safety design is the point: side-effecting actions (refunds, account changes) are **proposed but never executed — they require human approval**; a bounded tool loop, **persistent case memory**, and **PII redaction** keep it production-shaped. A labeled-ticket **eval harness** scores category/disposition accuracy, escalation precision/recall, and safety — **gated in CI**.

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

Open to AI/ML engineering roles · let's build something that ships.
