# 💱 AI-Powered Currency Rate Monitor (RAG Orchestrator)

### Overview
A sophisticated financial automation engine built on **n8n** that monitors global currency fluctuations. This project utilizes **Retrieval-Augmented Generation (RAG)** to provide context-aware analysis of forex data, moving beyond simple price alerts to intelligent trend forecasting.

### 🧠 The Logic
1. **Ingestion:** Receives real-time currency data via Webhooks.
2. **Vectorization:** Processes and embeds data using **OpenAI (text-embedding-3-small)**.
3. **Contextual Retrieval:** Stores and queries historical trends in a **Weaviate Vector Database**.
4. **Agentic Reasoning:** A **LangChain Agent** synthesizes historical context with live rates to generate actionable insights.
5. **Reporting:** Automatically updates Google Sheets and triggers Slack alerts for high-volatility events.

### 🚀 Deployment
1. `docker-compose up -d`
2. Import `workflows/currency_rate_monitor.json` into n8n.
3. Configure your OpenAI and Weaviate credentials in the `.env` file.