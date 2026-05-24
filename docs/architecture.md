# System Architecture

# ReguCompass AI
## Agentic Regulatory Intelligence & Compliance Platform

---

# Overview

ReguCompass AI is a verification-first multi-agent compliance intelligence system designed for banking governance workflows.

The platform autonomously:
- parses regulatory circulars
- extracts obligations
- validates recommendations
- generates audit-ready compliance intelligence

The architecture focuses on:
- deterministic workflows
- audit traceability
- hallucination prevention
- secure enterprise deployment

---

# High-Level Prototype Architecture

```text
┌──────────────────────────────────────────────┐
│              USER / COMPLIANCE TEAM          │
└──────────────────────┬───────────────────────┘
                       ↓

┌──────────────────────────────────────────────┐
│              PDF Upload API                  │
│                (FastAPI)                     │
└──────────────────────┬───────────────────────┘
                       ↓

┌──────────────────────────────────────────────┐
│           DOCUMENT PARSING LAYER             │
├──────────────────────────────────────────────┤
│  PyMuPDF                                     │
│  Marker Framework                            │
│  Intelligent Clause Chunking                 │
└──────────────────────┬───────────────────────┘
                       ↓

┌──────────────────────────────────────────────┐
│             VECTOR KNOWLEDGE BASE            │
├──────────────────────────────────────────────┤
│  BGE-small Embeddings                        │
│  ChromaDB                                    │
│  Semantic Retrieval                          │
└──────────────────────┬───────────────────────┘
                       ↓

┌──────────────────────────────────────────────┐
│      LANGGRAPH MULTI-AGENT ORCHESTRATION     │
├──────────────────────────────────────────────┤
│  Ingestor Agent                              │
│  Analyst Agent                               │
│  Auditor Agent                               │
│  Risk Scoring Agent                          │
└──────────────────────┬───────────────────────┘
                       ↓

┌──────────────────────────────────────────────┐
│          COMPLIANCE REPORT ENGINE            │
├──────────────────────────────────────────────┤
│  Risk Scores                                 │
│  Action Checklist                            │
│  Confidence Scores                           │
│  Clause Traceability                         │
└──────────────────────┬───────────────────────┘
                       ↓

┌──────────────────────────────────────────────┐
│              OUTPUT DASHBOARD                │
└──────────────────────────────────────────────┘
```

---

# Core Architectural Principles

## 1. Verification-First AI

No AI-generated output is accepted without verification.

---

## 2. Retrieval-Grounded Generation

All reasoning is grounded on retrieved compliance clauses.

---

## 3. Multi-Agent Orchestration

Specialized agents handle:
- ingestion
- reasoning
- validation
- risk scoring

---

## 4. Multi-Model Routing

Different models are assigned specialized tasks.

---

## 5. Audit Traceability

Every recommendation maps to:
```text
Page → Clause → Evidence
```

---

# Technology Stack

| Layer | Technology |
|---|---|
| Backend | FastAPI |
| Parsing | PyMuPDF |
| Layout Preservation | Marker |
| Vector DB | ChromaDB |
| Embeddings | BGE-small |
| Agent Framework | LangGraph |
| Model Routing | OpenRouter |
| Offline Fallback | Llama3 |
| Storage | SQLite |

---

# Enterprise Deployment Vision

Future enterprise deployment may include:
- SIEM integrations
- GRC systems
- Human approval workflows
- Live RBI monitoring
- Ticket escalation systems
- Knowledge graphs