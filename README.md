<h1 align="center">Sahil Mhatre</h1>
<h3 align="center">Backend &amp; Full-Stack Software Engineer | AI, Crypto &amp; Real-Time Systems</h3>

<p align="center">
  I build scalable backend services, full-stack applications and intelligent systems.<br/>
  My work spans API development, database architecture, AI-powered applications,<br/>
  cryptocurrency platforms and workflow automation.
</p>

<p align="center">
  <a href="https://github.com/sahilmhatre4796"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub"></a>
  <a href="https://www.linkedin.com/in/sahilmhatre4796"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:sahilmhatre4796@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email"></a>
</p>

---

## About Me

I'm a software engineer with a backend-first focus: I design data models and APIs, build the services around them, and ship the frontend that makes them usable. I care about systems that are honest about what they can and can't do — real data, real error handling, no fabricated metrics.

- **Currently building:** Agency Growth Automation Platform — AI-powered lead discovery and outreach automation (in active development)
- **Core focus:** Backend architecture, API engineering, database design, real-time systems
- **Also experienced in:** Full-stack delivery with React/Next.js frontends and LLM/RAG integration
- **Open to:** Backend, full-stack and AI engineering roles

---

## Featured Projects

### 1. [Agency Growth Automation Platform](https://github.com/sahilmhatre4796/agency-growth-automation-platform)
*AI-powered backend and automation platform for B2B agency growth — in active development.*

International lead-discovery, prospect-qualification, CRM and campaign-orchestration system built for multi-country, multi-industry B2B agencies.

**Implemented**
- Multi-tenant CRM with organization-scoped PostgreSQL Row-Level Security (RLS enforced and tested)
- Bounded discovery campaign orchestration — credits/budgets, automatic page continuation, row-locked leases, pause/resume/cancel, per-page rejection diagnostics
- Serper search adapter with anti-directory filtering and business-identity verification (dedup by domain/identity)
- Evidence-cited lead qualification with automatic routing to human review on ambiguity; opt-in, audit-bound contact enrichment
- Audit trail on all mutations (`audit_events`); every record organization-scoped; edge-first secrets, nothing sensitive in the browser
- 650+ tests (Vitest + PGlite in-memory Postgres) with GitHub Actions CI: lint → typecheck → test → build

**In progress / not yet live**
- Production deployment (pending final integration sign-off), load testing, verified sender onboarding
- Live email sending is **disabled by default** — no provider is connected; sends require explicit organization approval (multi-sender Gmail pool architecture is implemented, with suppression/unsubscribe gating)

**Stack:** Next.js 16 · React 19 · TypeScript · Tailwind CSS 4 · Supabase (PostgreSQL + RLS + Edge Functions) · Vitest

---

### 2. [Adaptive Crypto Trading System](https://github.com/sahilmhatre4796/adaptive-crypto-trading-system)
*Python framework for researching adaptive, multi-timeframe crypto strategies — simulated/paper execution only.*

Honest status: this is a research and paper-execution framework, **not a live trading system**. There is no code path anywhere that places, modifies or cancels orders or moves funds.

**What it does**
- Binance USD-M public market-data ingestion (finalized candles, pair synchronization, stale-data and duplicate rejection)
- Composable strategy pipeline: pattern detection → ATR-normalized market structure → multi-timeframe context (4h regime / 1h direction) → signal qualification → risk approval
- Risk engine with user-selected policy (≤10% planned equity loss per trade, `Decimal` arithmetic, enforced at the execution boundary)
- Simulated execution bridge (propose → admit → fill lifecycle), append-only journals, deterministic replay, crash recovery, hash-pinned release closure
- Live public-data **shadow evaluation** (M13): decisions journaled against real Binance candles without execution; 52 signal decisions journaled in live shadow runs
- Authenticated, read-only local monitoring dashboard (fail-closed rendering)

**Verification**
- 522 tests, fully offline (no exchange credentials required)
- Strategy edge is **unvalidated** — no historical dataset tracked yet (M11 not implemented); shadow evaluation is not paper trading and not evidence of profitability

**Stack:** Python 3.13 · pandas · numpy · SQLite journals · Binance USD-M public API · unittest

---

### 3. [Crypto Pulse](https://github.com/sahilmhatre4796/cryptopulse-backend/tree/main/cryptopulse-backend/cryptopulse-backend)
*Cryptocurrency market intelligence platform — Express API, PostgreSQL, live market data.*

A market tracking and intelligence application: live prices and global stats, portfolio tracking, watchlists, price alerts and a static dashboard frontend.

**Implemented**
- Express + PostgreSQL backend: JWT access/refresh auth, bcrypt, helmet, CORS allowlist, rate limiting, centralized error handling
- Market data pipeline with caching and provider fallback: CoinGecko (primary) → CoinPaprika, plus DexScreener DEX pair endpoints, Alternative.me Fear &amp; Greed and RSS news aggregation (CoinDesk / CoinTelegraph / Decrypt)
- Feature APIs: portfolio with holdings and P&amp;L, watchlist, price-alert state machine, transaction history, encrypted exchange API-key storage (AES-256-GCM at rest), subscription tier gating (Stripe stubs)
- 32 integration tests against a real PostgreSQL instance
- Static frontend (vanilla JS) deployed on Netlify; backend targets Render/Railway

**Honest scope**
- Exchange API keys are stored encrypted with CRUD only — live balance fetching is planned, not implemented
- Trading bots are config/status/P&amp;L tracking — the execution engine is planned, not implemented
- Subscriptions are schema + tier gating + Stripe stubs — webhooks not wired yet

**Stack:** Node.js · Express · PostgreSQL (pg) · JWT · vanilla JS frontend · Netlify / Render

---

### 4. [AI Flow](https://aiflow-ai.vercel.app/)
*AI-powered SaaS platform for building no-code RAG chatbots — live site.*

A self-hosted, multi-tenant alternative to Intercom-style bot builders: teams create bots with custom personas, feed them knowledge bases, and embed them on any site via a single script tag.

**Backend ([ai-flow-backend](https://github.com/sahilmhatre4796/ai-flow-backend)) — implemented**
- FastAPI + async PostgreSQL (asyncpg) + pgvector; Celery + Redis ingestion workers (separate sync engine by design)
- Full RAG pipeline: document ingestion (PDF / DOCX / CSV / URL / sitemap) → sentence-boundary chunking → OpenAI/Ollama embeddings → cosine-distance retrieval → grounded replies with `retrieved_chunk_ids` audit trail
- Multi-tenant isolation via `CurrentMembership` dependency (404, not 403, for non-members) with role-based access (owner/admin/agent/viewer)
- Real-time WebSocket chat routed through Redis pub/sub (correct across multiple uvicorn workers); swappable chat providers (OpenAI / Anthropic / Ollama)

**Frontend ([ai-flow-frontend](https://github.com/sahilmhatre4796/ai-flow-frontend)) — implemented**
- Vite + React dashboard wired to the real backend: Bot Builder, Knowledge Base, Conversations, Leads, Analytics, Marketplace, Team, Settings, Billing
- Embeddable chat widget (`widget.js`) for customer sites; JWT auth with refresh-token session restore
- Marketing landing page deployed at [aiflow-ai.vercel.app](https://aiflow-ai.vercel.app/)

**Current gaps (tracked, not hidden):** agent live-conversation WebSocket is implemented on the backend but not yet wired into the dashboard UI (REST polling today); document-status updates poll every 3s.

**Stack:** Python · FastAPI · PostgreSQL · pgvector · Redis · Celery · Docker · Nginx · React · Vite

---

### 5. [FlowForge](https://github.com/sahilmhatre4796/flowforge)
*Event-driven workflow automation platform — webhooks in, actions out.*

A webhook automation platform inspired by Zapier/n8n/Make: incoming HTTP events are published to Kafka, consumed by worker pools, and executed as a DAG of typed nodes.

**Implemented**
- Webhook ingest at `/hooks/{slug}` with HMAC-SHA256 signature verification; JWT auth (30-min access + 14-day refresh); API keys encrypted at rest (Fernet); Redis fixed-window rate limiting; RBAC via `is_admin`
- Kafka event bus: `webhook-events`, `workflow-executions` (retry), `notifications`, `audit-logs`, `workflow-executions-dlq` — consumer groups give exactly-one-worker-per-event at any replica count
- DAG executor: trigger (webhook / schedule / manual) → logic (filter / if-else / delay / transform) → actions (HTTP, Slack, Discord, Telegram, SMTP email, allow-listed SQL INSERT), with `{{field}}` templating
- Next.js 15 frontend: visual builder, execution history, integrations, monitoring, admin panel
- Full Docker Compose stack: PostgreSQL 16 + Alembic, Redis, Kafka + Zookeeper, nginx, Prometheus + Grafana

**Stack:** Python · FastAPI · Kafka · PostgreSQL · Redis · Next.js 15 · TypeScript · Docker · Prometheus

---

## Tech Stack

**Languages**
<img src="https://img.shields.io/badge/python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/javascript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript">
<img src="https://img.shields.io/badge/typescript-007ACC?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
<img src="https://img.shields.io/badge/sql-4479A1?style=flat-square" alt="SQL">

**Backend**
<img src="https://img.shields.io/badge/fastapi-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI">
<img src="https://img.shields.io/badge/postgresql-316192?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL">
<img src="https://img.shields.io/badge/rest%20apis-009688?style=flat-square" alt="REST APIs">
<img src="https://img.shields.io/badge/websockets-010101?style=flat-square&logo=socketdotio&logoColor=white" alt="WebSockets">
<img src="https://img.shields.io/badge/jwt-000000?style=flat-square&logo=jsonwebtokens&logoColor=white" alt="JWT Auth">
<img src="https://img.shields.io/badge/celery-A9CC42?style=flat-square&logo=celery&logoColor=black" alt="Celery">

**Frontend**
<img src="https://img.shields.io/badge/react-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React">
<img src="https://img.shields.io/badge/next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js">
<img src="https://img.shields.io/badge/vite-646CFF?style=flat-square&logo=vite&logoColor=white" alt="Vite">
<img src="https://img.shields.io/badge/tailwind%20css-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS">

**Databases &amp; Infrastructure**
<img src="https://img.shields.io/badge/mongodb-47A248?style=flat-square&logo=mongodb&logoColor=white" alt="MongoDB">
<img src="https://img.shields.io/badge/redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis">
<img src="https://img.shields.io/badge/supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=black" alt="Supabase">
<img src="https://img.shields.io/badge/pgvector-336791?style=flat-square" alt="pgvector">
<img src="https://img.shields.io/badge/docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker">
<img src="https://img.shields.io/badge/nginx-009639?style=flat-square&logo=nginx&logoColor=white" alt="Nginx">

**AI &amp; Automation**
<img src="https://img.shields.io/badge/llm%20integrations-412991?style=flat-square&logo=openai&logoColor=white" alt="LLM integrations">
<img src="https://img.shields.io/badge/rag-7C3AED?style=flat-square" alt="RAG">
<img src="https://img.shields.io/badge/groq-F55036?style=flat-square" alt="Groq">
<img src="https://img.shields.io/badge/kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white" alt="Kafka">

**Crypto &amp; Real-Time Systems**
<img src="https://img.shields.io/badge/exchange%20apis-F0B90B?style=flat-square&logo=binance&logoColor=black" alt="Exchange APIs">
<img src="https://img.shields.io/badge/market%20data-0ECB81?style=flat-square" alt="Market data">
<img src="https://img.shields.io/badge/ccxt-1B5CC4?style=flat-square" alt="CCXT">
<img src="https://img.shields.io/badge/real--time%20processing-010101?style=flat-square" alt="Real-time processing">

**Tools &amp; DevOps**
<img src="https://img.shields.io/badge/git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git">
<img src="https://img.shields.io/badge/github%20actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions">
<img src="https://img.shields.io/badge/linux-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux">
<img src="https://img.shields.io/badge/prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white" alt="Prometheus">
<img src="https://img.shields.io/badge/grafana-F46800?style=flat-square&logo=grafana&logoColor=white" alt="Grafana">
<img src="https://img.shields.io/badge/vercel-000000?style=flat-square&logo=vercel&logoColor=white" alt="Vercel">

---

## How I Work

- **Architecture first** — data model and API contracts before code
- **Backend-first, full-stack delivery** — from schema and migrations to deployment
- **Production instincts** — auth, RLS, rate limiting, encryption and audit trails designed in, not bolted on
- **Honest systems** — no fabricated data, no exaggerated claims; unvalidated stays unvalidated

---

## GitHub Stats

<p align="center">
  <img height="165" src="https://github-stats-extended.vercel.app/api?username=sahilmhatre4796&show_icons=true&theme=dark&hide_border=false&include_all_commits=true&count_private=true" alt="GitHub stats" />
  <img height="165" src="https://github-stats-extended.vercel.app/api/top-langs/?username=sahilmhatre4796&layout=compact&theme=dark&hide_border=false&include_all_commits=true&count_private=true" alt="Top languages" />
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com/?user=sahilmhatre4796&theme=dark&hide_border=false" alt="GitHub streak" />
</p>

---

## Let's Connect

- **Email:** sahilmhatre4796@gmail.com
- **LinkedIn:** [linkedin.com/in/sahilmhatre4796](https://www.linkedin.com/in/sahilmhatre4796)
- **GitHub:** [github.com/sahilmhatre4796](https://github.com/sahilmhatre4796)

<p align="center"><i>Open to backend, full-stack and AI engineering opportunities.</i></p>
