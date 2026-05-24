# Workflow Documentation

# Compliance Intelligence Workflow

---

# End-to-End Flow

```text
PDF Upload
 ↓
Text Extraction
 ↓
Layout Reconstruction
 ↓
Clause Chunking
 ↓
Embeddings Generation
 ↓
ChromaDB Storage
 ↓
Semantic Retrieval
 ↓
LangGraph Orchestration
 ↓
Ingestor Agent
 ↓
Analyst Agent
 ↓
Auditor Agent
 ↓
Risk Scoring Agent
 ↓
Compliance Report
```

---

# Step 1 — PDF Upload

Compliance officer uploads RBI circular.

FastAPI receives:
- PDF
- metadata
- upload information

---

# Step 2 — Parsing Layer

PyMuPDF extracts:
- raw text
- pages
- metadata

Marker reconstructs:
- tables
- layouts
- clause hierarchy

---

# Step 3 — Intelligent Chunking

Document split into:
- clause-aware chunks
- context-preserving segments

---

# Step 4 — Embeddings

BGE-small generates embeddings.

Stored in:
```text
ChromaDB
```

---

# Step 5 — Semantic Retrieval

Relevant compliance clauses retrieved for reasoning.

---

# Step 6 — Multi-Agent Execution

## Ingestor Agent
Classifies document.

## Analyst Agent
Extracts obligations.

## Auditor Agent
Verifies evidence.

## Risk Scoring Agent
Assigns severity.

---

# Step 7 — Compliance Report

Final report contains:
- compliance summary
- obligations
- risk score
- confidence score
- source traceability

---

# Verification Layer

All outputs verified against:
```text
Page → Clause → Evidence
```

---

# Hallucination Prevention

AI cannot generate unsupported claims.

Outputs require:
- evidence mapping
- clause grounding
- auditor verification