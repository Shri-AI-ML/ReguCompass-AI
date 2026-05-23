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

Unlike Generic AI copilots or standard RAG systems, ReguCompass AI is engineered specifically for:
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
> A Compliance Operating System, not merely an AI chatbot.

---

# Prototype Architecture

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
│                                              │
│                                              │
└──────────────────────────────────────────────┘
```

---

# 🤖 Multi-Agent + Multi-Model Architecture

ReguCompass AI uses:
# Adaptive Multi-Model Agent Routing

Different AI models are dynamically assigned specialized compliance tasks.

---

# Model Assignment Strategy

| Agent | Model Used | Purpose |
|---|---|---|
| Ingestor Agent | Gemini Flash | Fast metadata extraction & classification |
| Analyst Agent | DeepSeek Chat | Regulatory reasoning & obligation extraction |
| Auditor Agent | Claude Sonnet | Verification & hallucination prevention |
| Risk Scoring Agent | Claude Sonnet | Risk severity evaluation |
| Summarization Layer | Gemini Flash | Executive summaries |
| Offline Fallback Layer | Llama3 via Ollama | For Safe Banking deployment |

---

# 🧠 Why Different Models?

> Different models specialize in different capabilities.

## Gemini Flash
Used for:
- Ultra-fast extraction
- Preprocessing
- Summarization
- Lightweight classification

Why?
> Low latency and fast response generation.

---

## DeepSeek Chat
Used for:
- Compliance reasoning
- Obligation extraction
- Contextual analysis
- Department mapping

Why?
> Strong reasoning performance with low operational cost.

---

## Claude Sonnet
Used for:
- Hallucination detection
- Verification
- Source validation
- Risk evaluation

Why?
> High reliability and safer enterprise-grade reasoning.

---

## Llama3 (Offline Mode)
Used for:
- Air-gapped or Safe Banking infrastructure
- Secure offline deployment
- Fallback inference layer

Why?
> Production Banking environments may prohibit external API calls.

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
- Verified against source clauses
- Mapped to evidence
- Confidence scored
- Audit traceable

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

# 🔄 Prototype Workflow

## Step 1 — Upload RBI Circular
Compliance officer uploads regulatory PDF.

---

## Step 2 — Intelligent Parsing
PyMuPDF extracts text.

Marker preserves:
- Tables
- Layouts
- Clause hierarchy
- Formatting

---

## Step 3 — Semantic Retrieval Layer
Compliance clauses converted into embeddings.

Stored for:
- Semantic retrieval
- Evidence grounding
- Contextual search

---

## Step 4 — Multi-Agent Execution

### Ingestor Agent
- Regulation classification
- Metadata extraction
- Severity assignment

### Analyst Agent
- Compliance reasoning
- Obligation mapping
- Department impact analysis

### Auditor Agent
- Hallucination detection
- Evidence verification
- Citation validation

### Risk Scoring Agent
- Risk severity analysis
- Governance prioritization

---

## Step 5 — Compliance Report Generation

System generates:
- Compliance summary
- Risk score
- Action checklist
- Confidence score
- Audit traceability

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

# 🧩 ANY NEW INNOVATION?

Unlike standard AI systems:
- Outputs are never accepted without validation
- Every recommendation is evidence-grounded
- Specialized models handle specialized governance tasks
- Multi-agent orchestration improves reliability
- Hallucination risks are minimized

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


# 📌 Core Focus

> ReguCompass AI is designed as an Autonomous Verification Engine on the Enterprise Scale which operates as a Compliance Operating System.

---

# 👥 Team

The Wolves
Theme: Agentic Regulatory Intelligence & Compliance
Mail: tyagishubh.workspace@gmail.com

---
