<div align="center">

<img src="assets/logo.png" alt="Quarzos" width="120" />

# The Quarzos Project

**A complete back office for a small business — run from your phone.**

One server. One assistant. Everything a retail store needs to manage customers, orders, inventory, and communications — without an IT department.

</div>

---

## The Situation

A retail store specializing in crystals, minerals, and specialty coffee. Walk-in customers, Instagram DMs, WhatsApp conversations, supplier relationships, and inventory that changes daily.

The owner manages everything from her phone and tablet. She doesn't use a terminal. She doesn't SSH into anything. She talks to her assistant — in Spanish — and things get done.

That assistant runs on a single server with 31 containers, handling:

- **Customer management** — contacts, purchase history, follow-ups
- **Order tracking** — from inquiry to fulfillment
- **Inventory** — stock levels, restock alerts, supplier data
- **Messaging** — WhatsApp routing, Instagram DM handling
- **Research** — product catalogs, supplier research, market info
- **Automation** — appointment reminders, restock alerts, social media scheduling

---

## How It Works

```
  Phone / Tablet / Laptop
          │
          ▼
    ┌───────────┐
    │ Assistant  │  "¿Cuántos cuarzos rosa quedan?"
    └─────┬─────┘
          │
    ┌─────▼─────┐
    │  Gateway   │  Routes intent to the right tool
    └─────┬─────┘
          │
    ┌─────┴─────────────────────┐
    │                           │
    ▼                           ▼
┌────────┐              ┌────────────┐
│  CRM   │              │ Knowledge  │
│ Orders │              │   Search   │
│  Inv.  │              │  Research  │
└────────┘              └────────────┘
    │                           │
    └─────────┬─────────────────┘
              │
        ┌─────▼─────┐
        │ Automation │  Reminders, alerts, messages
        └───────────┘
```

The owner asks a question or gives an instruction. The system figures out where it goes — CRM lookup, knowledge search, order update, or outbound message — and handles it.

---

## What's Running

| Layer | What It Does |
|-------|-------------|
| **Assistant** | Bilingual executive assistant (Spanish/English) with business domain guardrails |
| **CRM** | Customer records, order tracking, inventory management via spreadsheet interface |
| **Knowledge** | Document processing, RAG search, indexed business knowledge |
| **Research** | Product research, supplier analysis, notes, podcast generation |
| **Automation** | Workflow engine with 400+ integrations for scheduling, alerts, and routing |
| **Messaging** | WhatsApp and Instagram DM handling, customer communication |
| **Database** | PostgreSQL with auth, storage, and realtime subscriptions |
| **Queue** | Task dispatch with parallel agent workers for background processing |

**31 containers. One server. Runs itself.**

---

## The Assistant

The assistant is purpose-built for this business. It:

- Speaks Mexican Spanish naturally
- Knows which questions go to which database table
- Requires confirmation before sending any customer message
- Cannot access banking, payment credentials, or server infrastructure
- Logs every action for audit
- Learns from corrections overnight

It's not a general-purpose chatbot. It's a trained executive assistant with strict boundaries and a memory that gets better over time.

---

## Built With

All open-source. All self-hosted. The owner's data never leaves the server.

| Tool | Role |
|------|------|
| [Archon](https://github.com/coleam00/Archon) | Knowledge engine — RAG search, document processing, task management |
| [NocoDB](https://github.com/nocodb/nocodb) | CRM — spreadsheet interface for customers, orders, inventory |
| [OpenNotebook](https://github.com/lfnovo/open-notebook) | Research — PDFs, video, audio, web content processing |
| [n8n](https://github.com/n8n-io/n8n) | Automation — workflows, integrations, scheduling |
| [Supabase](https://github.com/supabase/supabase) | Database — PostgreSQL with auth, storage, realtime |
| [RabbitMQ](https://github.com/rabbitmq/rabbitmq-server) | Queue — parallel task dispatch and agent workers |
| [Caddy](https://github.com/caddyserver/caddy) | Gateway — automatic HTTPS, reverse proxy |
| [Redis](https://github.com/redis/redis) | Memory — conversation cache, session state, audit log |

---

## Range

This same architecture has been deployed for two fundamentally different businesses:

| | Main Street | Wall Street |
|--|-------------|-------------|
| **Business** | Retail — crystals, minerals, specialty coffee | Investor relations firm |
| **Users** | Owner on phone/tablet, walk-in customers | Analysts, portfolio managers |
| **CRM** | Customer contacts, purchase history, events | Investor contacts, deal pipeline, compliance |
| **Automation** | Restock alerts, appointment reminders, social | Report distribution, meeting prep, follow-ups |
| **Knowledge** | Product catalogs, supplier research | Market analysis, regulatory filings |
| **Language** | Spanish | English |

One architecture. Two worlds. That's the point.

---

## Current Status

All services deployed and running in production.

| Service | Status |
|---------|--------|
| Gateway | ● Live |
| Assistant | ● Live |
| CRM | ● Live |
| Knowledge Engine | ● Live |
| Research | ● Live |
| Automation | ● Live |
| Database (PostgreSQL + 13 services) | ● Live |
| Task Queue | ● Live |

---

## What This Repo Contains

This is a **showcase** — it documents what has been built without exposing configuration or credentials.

For deployment inquiries or a live walkthrough, reach out directly.

---

<div align="center">

*Built by hand. Runs from your pocket.*

</div>
