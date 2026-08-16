<div align="center">

# Sahil Mhatre

### Full-Stack Software Engineer | AI/ML Enthusiast | Backend Architect

Building intelligent systems that bridge AI capabilities with real-world applications.

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/sahilmhatre4796)
[![Email](https://img.shields.io/badge/-Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:sahilmhatre4796@gmail.com)
[![GitHub](https://img.shields.io/badge/-GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/sahilmhatre4796)

</div>

---

## What I Build

I specialize in building **full-stack applications** with a focus on **AI-powered platforms**, **real-time systems**, and **financial technology**. My work spans from designing scalable backend architectures to crafting polished, interactive user interfaces.

---

## Featured Projects

### AI Flow â€” No-Code AI Chatbot Platform

<div align="center">

[![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)]()
[![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)]()
[![React](https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black)]()
[![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)]()
[![Redis](https://img.shields.io/badge/-Redis-DC382D?style=flat-square&logo=redis&logoColor=white)]()
[![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white)]()

</div>

A production-grade **no-code AI chatbot builder** â€” a self-hosted alternative to Botpress and Intercom bots. Users create AI-powered chatbots with custom personas, feed them knowledge bases from multiple sources (PDFs, URLs, sitemaps), and embed them on any website via a single `<script>` tag.

**Backend** (`ai-flow-backend`) â€” Built with **FastAPI**, **PostgreSQL + pgvector**, **Celery**, and **Redis**:
- Multi-tenant workspace system with role-based access control
- Full RAG pipeline: document ingestion (5 source types) â†’ sentence-boundary chunking â†’ OpenAI/Ollama embeddings â†’ pgvector cosine-distance retrieval
- Real-time WebSocket chat via Redis pub/sub (horizontally scalable)
- Swappable AI provider abstraction (OpenAI, Anthropic, Ollama)
- Stripe billing with tiered plans (Free / Pro / Business)
- 14-table database schema with Alembic migrations

**Frontend** (`ai-flow-frontend`) â€” Built with **React**, **Vite**, **Framer Motion**, and **Three.js**:
- Dual-build architecture: SPA dashboard + framework-free embeddable widget (IIFE)
- Three.js 3D floating particle background with WebGL
- Pervasive animation system (page transitions, staggered reveals, spring physics)
- Transparent JWT token refresh without external libraries

> A single `CurrentMembership` FastAPI dependency enforces tenant isolation at the checkpoint level. Non-members get 404 (not 403) to prevent leaking workspace existence.

---

### Crypto Compass â€” Sentiment-Driven Trading Platform

<div align="center">

[![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)]()
[![React](https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black)]()
[![MongoDB](https://img.shields.io/badge/-MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)]()
[![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)]()
[![Tailwind](https://img.shields.io/badge/-Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)]()

</div>

A **full-stack crypto trading dashboard** that aggregates real-time news, performs NLP sentiment analysis, and uses sentiment signals to automatically execute trades on **Binance** and **Bybit**.

**Key capabilities:**
- Multi-source news aggregation (RSS feeds from CoinTelegraph, Decrypt, CoinDesk + CoinGecko API)
- VADER sentiment analysis with per-coin attribution (10 coins)
- Asynchronous trading bot engine with configurable thresholds, leverage, and position management
- Dual exchange abstraction (CCXT for Binance, pybit for Bybit) with identical interfaces
- WebSocket real-time market data streaming
- Telegram trade alert integration
- Paper trading mode for risk-free testing

> The trading bot runs as independent `asyncio` tasks per user, polling sentiment every 30 seconds and executing trades without blocking the FastAPI event loop.

---

### SportsIQ â€” AI-Powered Sports Intelligence

<div align="center">

[![React](https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black)]()
[![Groq](https://img.shields.io/badge/-Groq-FF6B35?style=flat-square&logoColor=white)]()
[![Recharts](https://img.shields.io/badge/-Recharts-3B82F6?style=flat-square&logoColor=white)]()
[![Vite](https://img.shields.io/badge/-Vite-646CFF?style=flat-square&logo=vite&logoColor=white)]()

</div>

An **AI-powered sports intelligence platform** with real-time insights, predictions, analytics, and a conversational AI assistant powered by **Llama 3.3 70B** via Groq.

**Features include:**
- AI Copilot for sports analysis and predictions (Football, Cricket, Basketball, Tennis)
- Fantasy lineup optimizer with AI-generated picks and confidence scores
- Match prediction tracking with accuracy analytics
- Athlete discovery with radar charts and form data
- Gamification system (points, badges, streaks, leaderboards)
- Glassmorphism dark theme with magnetic card hover effects and aurora backgrounds

---

### Additional Projects

| Project | Description | Stack |
|---------|-------------|-------|
| [CryptoPulse](https://github.com/sahilmhatre4796/cryptopulse-frontend) | Real-time crypto dashboard with live market data and portfolio tracking | React, JavaScript |
| [CryptoPulse Backend](https://github.com/sahilmhatre4796/cryptopulse-backend) | API backend powering the CryptoPulse dashboard | Node.js, Express |
| [FlowForge](https://github.com/sahilmhatre4796/flowforge) | Webhook automation platform for workflow orchestration | TypeScript |
| [Binance Bot](https://github.com/sahilmhatre4796/Binance_bot) | Automated trading bot for Binance Futures Testnet (USDT-M) | Python, Binance API |

---

## Tech Stack

<div align="center">

![Python](https://img.shields.io/badge/-Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/-React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/-MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/-Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/-AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Git](https://img.shields.io/badge/-Git-F05032?style=for-the-badge&logo=git&logoColor=white)

</div>

---

## GitHub Stats

<div align="center">

<img height="180em" src="https://github-readme-stats.vercel.app/api?username=sahilmhatre4796&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" />
<img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=sahilmhatre4796&layout=compact&theme=tokyonight&hide_border=true" />

</div>

---

## What I'm Focused On

- Building **AI-powered applications** with real-world impact
- Designing **scalable backend architectures** with clean API design
- Exploring **RAG pipelines**, vector databases, and LLM orchestration
- Creating **real-time systems** with WebSocket and event-driven patterns
- Developing **fintech solutions** with automated trading and market analysis

---

<div align="center">

![Profile Views](https://komarev.com/ghpvc/?username=sahilmhatre4796&color=0A66C2&style=for-the-badge&label=PROFILE+VIEWS)

*"Building intelligent systems, one commit at a time."*

</div>
