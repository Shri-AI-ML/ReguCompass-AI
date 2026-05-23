# ReguCompass AI  
## Agentic Regulatory Intelligence & Compliance Platform

> “From static compliance management to autonomous regulatory intelligence.”

---

# 📌 Overview

ReguCompass AI is a multi-agent AI-powered regulatory intelligence and compliance orchestration platform designed for banking and enterprise governance systems.

The system autonomously:
- Parses RBI and compliance circulars
- Extracts obligations
- Detects risk
- Verifies outputs
- Generates audit-ready compliance intelligence

Unlike generic AI chatbots or basic RAG systems, ReguCompass AI focuses on:
- Hallucination prevention
- Audit traceability
- Multi-agent verification
- Offline enterprise deployment
- Deterministic workflows

---

# 🚨 Problem Statement

Modern banks face massive regulatory overload due to:
- RBI circulars
- CERT-In advisories
- SEBI notifications
- DPDP compliance mandates
- Cybersecurity governance updates

Current workflows remain:
- Manual
- Slow
- Error-prone
- Difficult to audit

## Industry Bottlenecks

### 1. Manual Parsing Friction
Compliance teams manually parse large PDFs and circulars.

### 2. Interpretation Delays
Compliance validation cycles take weeks.

### 3. Missing Audit Traceability
Difficult to map recommendations back to source clauses.

### 4. LLM Hallucination Risk
Generic AI copilots generate unverifiable outputs.

---

# 🎯 Our Solution

ReguCompass AI introduces a:
# Verification-First Multi-Agent Compliance Operating System

Core capabilities:
- Autonomous PDF parsing
- Retrieval-grounded reasoning
- Multi-agent orchestration
- Auditor-based validation
- Audit-ready compliance reporting

---

# 🏗 Prototype Architecture

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
│         LANGGRAPH AGENT ORCHESTRATION        │
├──────────────────────────────────────────────┤
│  Ingestor Agent                              │
│  Analyst Agent                               │
│  Auditor Agent                               │
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
├──────────────────────────────────────────────┤
│  Compliance Status                           │
│  Risk Heatmaps                               │
│  Audit Evidence                              │
│  Agent Logs                                  │
└──────────────────────────────────────────────┘
```

---

# ⚙️ Tech Stack

| Layer | Technology |
|---|---|
| Backend API | FastAPI |
| PDF Parsing | PyMuPDF |
| Layout Reconstruction | Marker |
| Embeddings | BGE-small |
| Vector Database | ChromaDB |
| LLM | Llama3 (Ollama) |
| Agent Orchestration | LangGraph |
| Dashboard | React + Tailwind |
| Storage | SQLite |

---

# 🤖 Multi-Agent Architecture

## 1. Ingestor Agent
Responsibilities:
- Extract metadata
- Detect regulation type
- Assign severity
- Validate document integrity

---

## 2. Analyst Agent
Responsibilities:
- Interpret clauses
- Extract obligations
- Identify impacted departments
- Generate compliance recommendations

---

## 3. Auditor Agent
Responsibilities:
- Verify AI outputs
- Prevent hallucinations
- Match evidence with source clauses
- Generate confidence scores

---

# 🔒 Security Architecture

ReguCompass AI is designed for:
- Air-gapped deployment
- Offline inference
- No external API dependency
- Internal banking infrastructure
- Immutable audit logs

## Hallucination Prevention
The system uses:
- Retrieval-grounded generation
- Source verification loops
- Auditor-agent validation
- Citation traceability

---

# 🔄 Prototype Workflow

## Step 1 — Upload RBI Circular
User uploads PDF through FastAPI endpoint.

---

## Step 2 — Parsing Layer
PyMuPDF extracts raw text.

Marker preserves:
- Tables
- Headings
- Layout structure

---

## Step 3 — Chunking & Embeddings
Documents split into intelligent clause chunks.

Embeddings stored in ChromaDB.

---

## Step 4 — Multi-Agent Analysis
LangGraph orchestrates:
- Ingestor Agent
- Analyst Agent
- Auditor Agent

---

## Step 5 — Verification
Auditor Agent validates:
- Source grounding
- Evidence linkage
- Confidence scores

---

## Step 6 — Compliance Report
System generates:
- Risk level
- Obligations
- Impacted departments
- Audit traceability

---

# 📊 Sample Output

```json
{
  "regulation_type": "RBI Cybersecurity Circular",
  "priority": "HIGH",

  "analysis": {
    "department": "IT Security",
    "obligation": "Enable MFA",
    "deadline": "30 days"
  },

  "verified": true,

  "confidence_score": "94%",

  "source_reference": {
    "page": 4,
    "clause": "2.1"
  }
}
```

---

# 📈 Expected Impact

| Metric | Traditional Workflow | ReguCompass AI |
|---|---|---|
| Regulatory Parsing | Days | Minutes |
| Clause Interpretation | Weeks | Minutes |
| Audit Preparation | Days | Real-Time |
| Manual Review Effort | High | Reduced by 90–95% |

---

# 🧠 Key Innovation

Unlike standard AI systems:
- Outputs are never accepted without validation
- Every recommendation is source-grounded
- Multi-agent workflows improve reliability
- Hallucination risks are minimized

---

# 🛣 Development Roadmap

## Week 1
- FastAPI setup
- PDF upload system
- Parsing engine

## Week 2
- Chunking
- Embeddings
- ChromaDB integration

## Week 3
- LangGraph orchestration
- Analyst Agent
- Auditor Agent

## Week 4
- Hallucination testing
- Verification loops
- Confidence scoring

## Week 5
- Dashboard integration
- Demo polishing
- Architecture visualization

---

# 🚀 Future Scope

Future enterprise-scale implementation may include:
- Live RBI monitoring
- SIEM integration
- SOC integrations
- Compliance ticketing systems
- Human approval workflows
- Policy knowledge graphs
- Multi-bank deployment

---

# 📂 Project Structure

```text
backend/
│
├── app/
│   ├── agents/
│   │   ├── ingestor.py
│   │   ├── analyst.py
│   │   ├── auditor.py
│   │
│   ├── parser/
│   │   ├── pdf_parser.py
│   │   ├── chunker.py
│   │
│   ├── rag/
│   │   ├── embeddings.py
│   │   ├── vectordb.py
│   │
│   ├── graph/
│   │   ├── workflow.py
│   │
│   ├── api/
│   │   ├── routes.py
│
├── data/
│
├── main.py
│
├── requirements.txt
```

---

# 🧪 Installation

## Clone Repository

```bash
git clone https://github.com/your-team/regucompass-ai.git
cd regucompass-ai
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Run Ollama

Install:
https://ollama.com

Run model:

```bash
ollama run llama3
```

---

## Start Backend Server

```bash
uvicorn main:app --reload
```

---

# 📌 Core Principle

> “ReguCompass AI is designed as a compliance operating layer, not merely an AI assistant.”

---

# 👥 Team

Canara Bank SuRaksha Cyber Hackathon 2.0  
Track 2 — Agentic Regulatory Intelligence & Compliance

---

# 📜 License

MIT License

---

# 🙌 Acknowledgements

Built using:
- LangGraph
- Ollama
- PyMuPDF
- ChromaDB
- FastAPI
- Layout-aware AI systems

---

# 📧 Contact

For collaboration or enterprise deployment inquiries:

Team ReguCompass AI
