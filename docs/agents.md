# Multi-Agent Architecture

# ReguCompass AI Agent System

ReguCompass AI uses specialized AI agents coordinated through LangGraph orchestration.

---

# Agent Overview

| Agent | Responsibility |
|---|---|
| Ingestor Agent | document classification |
| Analyst Agent | compliance reasoning |
| Auditor Agent | verification |
| Risk Scoring Agent | risk evaluation |

---

# 1. Ingestor Agent

## Purpose
Handles document ingestion and metadata extraction.

---

## Responsibilities

- detect regulation type
- extract metadata
- classify severity
- identify compliance category

---

## Model Used

```text
Gemini Flash
```

---

## Input

- parsed PDF text
- metadata

---

## Output

```json
{
  "regulation_type": "RBI Circular",
  "priority": "HIGH"
}
```

---

# 2. Analyst Agent

## Purpose

Performs compliance reasoning.

---

## Responsibilities

- extract obligations
- identify impacted departments
- detect deadlines
- generate compliance insights

---

## Model Used

```text
DeepSeek Chat
```

---

## Output Example

```json
{
  "department": "IT Security",
  "obligation": "Enable MFA"
}
```

---

# 3. Auditor Agent

## Purpose

Validates AI-generated outputs.

---

## Responsibilities

- hallucination detection
- source verification
- citation mapping
- confidence scoring

---

## Model Used

```text
Claude Sonnet
```

---

## Verification Logic

Checks:
```text
Did AI output exist in source clauses?
```

---

# 4. Risk Scoring Agent

## Purpose

Assigns governance severity.

---

## Responsibilities

- risk classification
- severity scoring
- escalation priority

---

## Model Used

```text
Claude Sonnet
```

---

# Agent Workflow

```text
PDF
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

# Core Principle

> No recommendation is finalized without Auditor Agent verification.