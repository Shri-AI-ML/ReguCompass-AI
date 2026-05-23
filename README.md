# ReguCompass AI
## Agentic Regulatory Intelligence & Compliance Platform

> “From static compliance management to autonomous regulatory intelligence.”

---

# 🚀 Overview

ReguCompass AI is a verification-first, multi-agent regulatory intelligence platform designed for banking and enterprise governance systems.

The platform autonomously:
- Ingests RBI and regulatory circulars
- Parses complex compliance PDFs
- Extracts obligations and risk indicators
- Verifies AI-generated outputs
- Generates audit-ready compliance intelligence

Unlike generic AI copilots or standard RAG systems, ReguCompass AI is engineered specifically for:
- Banking governance
- Audit traceability
- Hallucination prevention
- Multi-agent verification
- Offline enterprise deployment

---

# 🧠 Problem Statement

Modern banking institutions face continuously evolving:
- RBI circulars
- CERT-In advisories
- DPDP regulations
- Cybersecurity mandates
- Governance obligations

Current workflows remain:
- Manual
- Slow
- Error-prone
- Difficult to audit

## Key Industry Bottlenecks

### 1. Manual Parsing Friction
Compliance teams manually review lengthy PDFs and circulars.

### 2. Delayed Interpretation Cycles
Compliance validation may take days or weeks.

### 3. Missing Audit Traceability
Organizations struggle to map recommendations back to exact source clauses.

### 4. LLM Hallucination Risk
Generic AI copilots often produce unverifiable outputs.

---

# 🎯 Vision

ReguCompass AI transforms compliance from:
```text
Reactive Documentation
        ↓
Autonomous Regulatory Intelligence
```

The platform acts as:
# A Compliance Operating System
—not merely an AI chatbot.

---

# 🏗 Prototype Architecture

```text
┌──────────────────────────────────────────────┐
│              USER / COMPLIANCE TEAM          │
└──────────────────────┬───────────────────────┘
                       ↓
══════════════════════════════════════════════════════

┌──────────────────────────────────────────────┐
│              PDF Upload API                  │
│                (FastAPI)                     │
└──────────────────────┬───────────────────────┘
                       ↓
══════════════════════════════════════════════════════

┌──────────────────────────────────────────────┐
│           DOCUMENT PARSING LAYER             │
├──────────────────────────────────────────────┤
│                                              │
│  PyMuPDF                                     │
│  → Raw text extraction                       │
│                                              │
│  Marker Framework                            │
│  → Layout & table preservation               │
│                                              │
│  Intelligent Clause Chunking                 │
│  → Compliance-aware segmentation             │
│                                              │
└──────────────────────┬───────────────────────┘
                       ↓
══════════════════════════════════════════════════════

┌──────────────────────────────────────────────┐
│             VECTOR KNOWLEDGE BASE            │
├──────────────────────────────────────────────┤
│                                              │
│  BGE-small Embeddings                        │
│                                              │
│  ChromaDB                                    │
│  → Semantic retrieval                        │
│  → Clause indexing                           │
│                                              │
└──────────────────────┬───────────────────────┘
                       ↓
══════════════════════════════════════════════════════

┌──────────────────────────────────────────────┐
│      LANGGRAPH MULTI-AGENT ORCHESTRATION     │
├──────────────────────────────────────────────┤
│                                              │
│  Ingestor Agent                              │
│  Analyst Agent                               │
│  Auditor Agent                               │
│  Risk Scoring Agent                          │
│                                              │
└──────────────────────┬───────────────────────┘
                       ↓
══════════════════════════════════════════════════════

┌──────────────────────────────────────────────┐
│          COMPLIANCE REPORT ENGINE            │
├──────────────────────────────────────────────┤
│                                              │
│  • Risk Scores                               │
│  • Action Checklist                          │
│  • Confidence Scores                         │
│  • Clause Traceability                       │
│                                              │
└──────────────────────┬───────────────────────┘
                       ↓
══════════════════════════════════════════════════════

┌──────────────────────────────────────────────┐
│              OUTPUT DASHBOARD                │
├──────────────────────────────────────────────┤
│                                              │
│  • Compliance Status                         │
│  • Risk Heatmaps                             │
│  • Audit Evidence                            │
│  • Agent Logs                                │
│  • Source Clause Mapping                     │
│                                              │
└──────────────────────────────────────────────┘
```

---

# 🤖 Multi-Agent + Multi-Model Architecture

ReguCompass AI uses:
# Adaptive Multi-Model Agent Routing

Different AI models are dynamically assigned specialized compliance tasks.

---

# 🧩 Model Assignment Strategy

| Agent | Model Used | Purpose |
|---|---|---|
| Ingestor Agent | Gemini Flash | Fast metadata extraction & classification |
| Analyst Agent | DeepSeek Chat | Regulatory reasoning & obligation extraction |
| Auditor Agent | Claude Sonnet | Verification & hallucination prevention |
| Risk Scoring Agent | Claude Sonnet | Risk severity evaluation |
| Summarization Layer | Gemini Flash | Executive summaries |
| Offline Fallback Layer | Llama3 via Ollama | Air-gapped banking deployment |

---

# 🧠 Why Different Models?

Different models specialize in different capabilities.

## Gemini Flash
Used for:
- ultra-fast extraction
- preprocessing
- summarization
- lightweight classification

Why?
Low latency and fast response generation.

---

## DeepSeek Chat
Used for:
- compliance reasoning
- obligation extraction
- contextual analysis
- department mapping

Why?
Strong reasoning performance with low operational cost.

---

## Claude Sonnet
Used for:
- hallucination detection
- verification
- source validation
- risk evaluation

Why?
High reliability and safer enterprise-grade reasoning.

---

## Llama3 (Offline Mode)
Used for:
- air-gapped banking infrastructure
- secure offline deployment
- fallback inference layer

Why?
Production banking environments may prohibit external API calls.

---

# 🔄 Multi-Agent Workflow

```text
PDF Upload
      ↓

Ingestor Agent
(Model: Gemini Flash)
      ↓

Analyst Agent
(Model: DeepSeek Chat)
      ↓

Auditor Agent
(Model: Claude Sonnet)
      ↓

Risk Scoring Agent
(Model: Claude Sonnet)
      ↓

Compliance Report
```

---

# 🔒 Security Architecture

ReguCompass AI is designed for:
- Banking-grade deployment
- Air-gapped environments
- Offline inference capability
- Internal infrastructure hosting
- Zero external data leakage

---

# 🛡 Hallucination Prevention

The platform uses:
# Retrieval-Grounded Generation

AI responses are generated only from retrieved compliance clauses.

---

## Verification Pipeline

Every AI-generated recommendation is:
- verified against source clauses
- mapped to evidence
- confidence scored
- audit traceable

---

# 📌 Citation Mapping

Every compliance insight maps to:
```text
Page → Clause → Evidence
```

Example:
```text
Enable MFA
↓
Page 4 → Clause 2.1
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
| Agent Orchestration | LangGraph |
| Model Routing | OpenRouter |
| Reasoning Models | Claude, DeepSeek, Gemini |
| Offline Fallback | Llama3 |
| Storage | SQLite |

---

# 🔄 Prototype Workflow

## Step 1 — Upload RBI Circular
Compliance officer uploads regulatory PDF.

---

## Step 2 — Intelligent Parsing
PyMuPDF extracts text.

Marker preserves:
- tables
- layouts
- clause hierarchy
- formatting

---

## Step 3 — Semantic Retrieval Layer
Compliance clauses converted into embeddings.

Stored inside ChromaDB for:
- semantic retrieval
- evidence grounding
- contextual search

---

## Step 4 — Multi-Agent Execution

### Ingestor Agent
- regulation classification
- metadata extraction
- severity assignment

### Analyst Agent
- compliance reasoning
- obligation mapping
- department impact analysis

### Auditor Agent
- hallucination detection
- evidence verification
- citation validation

### Risk Scoring Agent
- risk severity analysis
- governance prioritization

---

## Step 5 — Compliance Report Generation

System generates:
- compliance summary
- risk score
- action checklist
- confidence score
- audit traceability

---

# 📊 Sample Output

```json
{
  "regulation_type": "RBI Cybersecurity Circular",

  "priority": "HIGH",

  "analysis": {
    "department": "IT Security",
    "obligation": "Enable Multi-Factor Authentication",
    "deadline": "30 days"
  },

  "verified": true,

  "confidence_score": "94%",

  "risk_level": "HIGH",

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

# 🧩 Core Innovation

Unlike standard AI systems:
- Outputs are never accepted without validation
- Every recommendation is evidence-grounded
- Specialized models handle specialized governance tasks
- Multi-agent orchestration improves reliability
- Hallucination risks are minimized

---

# 🛣 Development Roadmap

## Week 1
- FastAPI setup
- PDF ingestion pipeline
- Parsing engine

## Week 2
- Intelligent chunking
- Embeddings
- ChromaDB integration

## Week 3
- LangGraph orchestration
- Multi-agent workflows

## Week 4
- Auditor verification loops
- Hallucination prevention
- Confidence scoring

## Week 5
- Dashboard integration
- Demo preparation
- Architecture visualization

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
│   │   ├── risk_agent.py
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

## Setup Environment Variables

Create `.env`

```env
OPENROUTER_API_KEY=your_key_here
```

---

## Optional Offline Mode

Install:
https://ollama.com

Run:

```bash
ollama run llama3
```

---

## Start Backend

```bash
uvicorn main:app --reload
```

---

# 🚀 Future Scope

Future enterprise deployment may include:
- Live RBI monitoring
- SIEM integration
- GRC integrations
- Ticket escalation systems
- Human approval workflows
- Compliance knowledge graphs
- Multi-bank governance deployment

---

# 🏆 Hackathon Focus

This prototype demonstrates:
# The Core Autonomous Verification Engine

of a future enterprise-scale:
# Compliance Operating System

---

# 📌 Core Principle

> “ReguCompass AI is designed as a governance operating layer, not merely an AI assistant.”

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
- OpenRouter
- PyMuPDF
- ChromaDB
- FastAPI
- Ollama
- Multi-Agent AI Systems
