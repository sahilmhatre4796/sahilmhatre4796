<p align="center">
  <img src="https://raw.githubusercontent.com/sahilmhatre4796/sahilmhatre4796/main/assets/banner.svg" alt="Sahil Mhatre — Backend &amp; Full-Stack Software Engineer | AI, Crypto &amp; Real-Time Systems" width="100%"/>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=16&pause=1200&color=2DD4BF&center=true&vCenter=true&width=620&height=40&lines=Backend+%26+API+Engineering;Scalable+Full-Stack+Applications;AI-Powered+Systems+%26+RAG;Crypto+%26+Real-Time+Data" alt="Typing SVG"/>
</p>

<p align="center">
  <a href="https://github.com/sahilmhatre4796"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub"></a>
  <a href="https://www.linkedin.com/in/sahilmhatre4796"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:sahilmhatre4796@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="https://aiflow-ai.vercel.app/"><img src="https://img.shields.io/badge/Live-aiflow--ai.vercel.app-1B1F23?style=flat-square&logo=vercel&logoColor=white" alt="Live site"></a>
</p>

<p align="center"><img src="https://raw.githubusercontent.com/sahilmhatre4796/sahilmhatre4796/main/assets/divider.svg" alt="" width="90%"/></p>

## `//` about

I build scalable backend services, full-stack applications and intelligent systems. My work spans **API development, database architecture, AI-powered applications, cryptocurrency platforms and workflow automation** — a backend-first mindset with the frontend range to ship end-to-end.

`currently building` [Agency Growth Automation Platform](https://github.com/sahilmhatre4796/agency-growth-automation-platform) — AI-powered lead discovery, qualification and outreach automation, in active development.

`strengths` backend architecture · API engineering · database design · real-time systems · RAG pipelines

`fluent in` React/Next.js · LLM integrations (OpenAI · Anthropic · Ollama · Groq) · event-driven architecture

`open to` backend · full-stack · AI engineering roles

<p align="center"><img src="https://raw.githubusercontent.com/sahilmhatre4796/sahilmhatre4796/main/assets/divider.svg" alt="" width="90%"/></p>

## `//` SELECTED PROJECTS | TOP 5

<img align="left" width="248" src="https://raw.githubusercontent.com/sahilmhatre4796/sahilmhatre4796/main/assets/card-01.svg" alt="01 — Agency Growth Automation Platform"/>

### 01 — [Agency Growth Automation Platform](https://github.com/sahilmhatre4796/agency-growth-automation-platform) <code>IN ACTIVE DEVELOPMENT</code>

AI-powered backend and automation platform for international B2B agency growth — prospect discovery, qualification, enrichment, CRM and personalized outreach.

**Implemented:** multi-tenant org-scoped CRM on Postgres RLS (tested) · bounded campaign orchestration (Serper, credit budgets, row-locked leases, pause/resume/cancel, per-page diagnostics, anti-directory filtering) · evidence-cited qualification with human-in-the-loop routing · opt-in, audit-bound enrichment. **Not live yet:** production deployment pending integration sign-off — live email sending is disabled by default; multi-sender Gmail architecture implemented, no provider connected. 650+ tests · GitHub Actions CI.

`next.js 16 · react 19 · typescript · supabase · vitest`

**[→ View repository](https://github.com/sahilmhatre4796/agency-growth-automation-platform)**

<br clear="left"/>
<p align="center"><img src="https://raw.githubusercontent.com/sahilmhatre4796/sahilmhatre4796/main/assets/divider.svg" alt="" width="60%"/></p>

<img align="right" width="248" src="https://raw.githubusercontent.com/sahilmhatre4796/sahilmhatre4796/main/assets/card-02.svg" alt="02 — Adaptive Crypto Trading System"/>

### 02 — [Adaptive Crypto Trading System](https://github.com/sahilmhatre4796/adaptive-crypto-trading-system) <code>PAPER / SHADOW ONLY</code>

Python framework for researching adaptive, multi-timeframe crypto strategies. **There is no code path anywhere in this codebase that places, modifies or cancels real orders.**

Public Binance USD-M ingestion → pattern detection → ATR-normalized market structure → multi-timeframe context (4h regime / 1h direction) → signal qualification with replay protection → risk approval (≤10% planned equity loss, `Decimal`) → simulated execution, append-only journals, deterministic replay, crash recovery, read-only dashboard. Live public-data **shadow evaluation** — 52 journaled decisions; strategy edge is **unvalidated** (M11 open). 522 tests, fully offline.

`python 3.13 · pandas · sqlite · binance usd-m`

**[→ View repository](https://github.com/sahilmhatre4796/adaptive-crypto-trading-system)**

<br clear="right"/>
<p align="center"><img src="https://raw.githubusercontent.com/sahilmhatre4796/sahilmhatre4796/main/assets/divider.svg" alt="" width="60%"/></p>

<img align="left" width="264" src="https://raw.githubusercontent.com/sahilmhatre4796/sahilmhatre4796/main/assets/card-03.svg" alt="03 — Crypto Pulse"/>

### 03 — [Crypto Pulse](https://github.com/sahilmhatre4796/cryptopulse-backend/tree/main/cryptopulse-backend/cryptopulse-backend) <code>MARKET INTELLIGENCE</code>

Cryptocurrency market intelligence platform — Express API, PostgreSQL, and a static dashboard with live prices, portfolio tracking and watchlists.

JWT access/refresh auth, bcrypt, helmet, CORS allowlist, rate limiting. Market data with caching and provider fallback: CoinGecko (primary) → CoinPaprika, plus DexScreener DEX pair discovery, Alternative.me Fear &amp; Greed, RSS news aggregation. Portfolio P&amp;L, watchlists, price-alert state machine, AES-256-GCM encrypted exchange-key CRUD. 32 integration tests against real PostgreSQL · frontend on Netlify. Honest scope: exchange integration is key storage only; bots are config/P&amp;L tracking, execution planned.

`node.js · express · postgresql · jwt · netlify`

**[→ View repository](https://github.com/sahilmhatre4796/cryptopulse-backend/tree/main/cryptopulse-backend/cryptopulse-backend)**

<br clear="left"/>
<p align="center"><img src="https://raw.githubusercontent.com/sahilmhatre4796/sahilmhatre4796/main/assets/divider.svg" alt="" width="60%"/></p>

<img align="right" width="248" src="https://raw.githubusercontent.com/sahilmhatre4796/sahilmhatre4796/main/assets/card-04.svg" alt="04 — AI Flow"/>

### 04 — [AI Flow](https://aiflow-ai.vercel.app/) <code>LIVE</code>

AI-powered SaaS for building no-code RAG chatbots — a self-hosted multi-tenant alternative to Intercom-style bot builders.

**Backend** ([ai-flow-backend](https://github.com/sahilmhatre4796/ai-flow-backend)): FastAPI + async PostgreSQL + pgvector · Celery + Redis ingestion · WebSocket chat over Redis pub/sub · 404-not-403 tenant isolation · RBAC (owner/admin/agent/viewer) · swappable providers (OpenAI/Anthropic/Ollama). Full RAG pipeline: PDF/DOCX/CSV/URL → sentence-boundary chunking → embeddings → cosine-distance retrieval → grounded replies with audit trail. **Frontend** ([ai-flow-frontend](https://github.com/sahilmhatre4796/ai-flow-frontend)): Vite + React dashboard — Bot Builder, Knowledge Base, Conversations, Leads, Analytics, Team, Billing — plus embeddable widget. Honest gaps: agent live-conversation WS not yet in dashboard (REST polling); doc-status polls every 3s.

`fastapi · pgvector · redis · celery · react · vite`

**[→ Visit live site](https://aiflow-ai.vercel.app/)** · **[→ Backend](https://github.com/sahilmhatre4796/ai-flow-backend)** · **[→ Frontend](https://github.com/sahilmhatre4796/ai-flow-frontend)**

<br clear="right"/>
<p align="center"><img src="https://raw.githubusercontent.com/sahilmhatre4796/sahilmhatre4796/main/assets/divider.svg" alt="" width="60%"/></p>

<img align="left" width="248" src="https://raw.githubusercontent.com/sahilmhatre4796/sahilmhatre4796/main/assets/card-05.svg" alt="05 — FlowForge"/>

### 05 — [FlowForge](https://github.com/sahilmhatre4796/flowforge) <code>EVENT-DRIVEN · KAFKA</code>

Webhook automation platform (Zapier/n8n/Make-style) — incoming HTTP events become DAG executions across a Kafka backbone.

`/hooks/{slug}` ingest with HMAC-SHA256 signatures · JWT auth (30-min access / 14-day refresh) · Fernet-encrypted API keys · Redis rate limiting · RBAC. Kafka bus: `webhook-events` · `workflow-executions` (retry) · `notifications` · `audit-logs` · `workflow-executions-dlq`, consumer groups scale horizontally. DAG executor: webhook/schedule/manual triggers → filter/if-else/delay/transform → HTTP, Slack, Discord, Telegram, SMTP, allow-listed SQL INSERT. Next.js 15 frontend · Docker Compose: PG 16 + Alembic, Kafka, nginx, Prometheus + Grafana. Honest scope: portfolio-scale build with production-style architecture — not load-proven.

`fastapi · kafka · postgresql · redis · next.js 15 · docker`

**[→ View repository](https://github.com/sahilmhatre4796/flowforge)**

<br clear="left"/>

<p align="center"><img src="https://raw.githubusercontent.com/sahilmhatre4796/sahilmhatre4796/main/assets/divider.svg" alt="" width="90%"/></p>

## `//` the stack

<p align="center">
  <img src="https://raw.githubusercontent.com/sahilmhatre4796/sahilmhatre4796/main/assets/skill-backend.svg" width="49%" alt="Backend Engineering — FastAPI, PostgreSQL, REST APIs, WebSockets, Redis, Celery, pgvector, RLS, Docker"/>
  <img src="https://raw.githubusercontent.com/sahilmhatre4796/sahilmhatre4796/main/assets/skill-frontend.svg" width="49%" alt="Frontend Development — React, Next.js, TypeScript, Vite, Tailwind CSS"/>
  <br/>
  <img src="https://raw.githubusercontent.com/sahilmhatre4796/sahilmhatre4796/main/assets/skill-ai.svg" width="49%" alt="AI and Automation — LLM integrations, RAG, pgvector, Groq, OpenAI, Anthropic"/>
  <img src="https://raw.githubusercontent.com/sahilmhatre4796/sahilmhatre4796/main/assets/skill-crypto.svg" width="49%" alt="Crypto and Real-Time Systems — Binance USD-M, CCXT, market data, WebSockets, real-time processing"/>
</p>

<p align="center"><code>languages — python · javascript · typescript · sql</code><br/><code>also — mongodb · supabase · git · github actions · linux · prometheus · grafana</code></p>

<p align="center"><img src="https://raw.githubusercontent.com/sahilmhatre4796/sahilmhatre4796/main/assets/divider.svg" alt="" width="90%"/></p>

## `//` github analytics

<p align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=sahilmhatre4796&theme=onedark&no-frame=true&no-bg=true&margin-w=6&row=1&column=6" alt="GitHub trophies"/>
</p>

<p align="center">
  <img height="165" src="https://github-stats-extended.vercel.app/api?username=sahilmhatre4796&show_icons=true&theme=dark&hide_border=false&include_all_commits=true&count_private=true" alt="GitHub stats"/>
  <img height="165" src="https://github-stats-extended.vercel.app/api/top-langs/?username=sahilmhatre4796&layout=compact&theme=dark&hide_border=false&include_all_commits=true&count_private=true" alt="Top languages"/>
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com/?user=sahilmhatre4796&theme=dark&hide_border=false" alt="GitHub streak"/>
</p>

<p align="center"><img src="https://raw.githubusercontent.com/sahilmhatre4796/sahilmhatre4796/main/assets/divider.svg" alt="" width="90%"/></p>

## `//` let's connect

<p align="center">
  <a href="mailto:sahilmhatre4796@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="https://www.linkedin.com/in/sahilmhatre4796"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="https://github.com/sahilmhatre4796"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a>
</p>

<p align="center"><i>Open to backend, full-stack and AI engineering opportunities — let's build something solid.</i></p>
