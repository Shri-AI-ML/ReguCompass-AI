# Multi-Model Routing Strategy

# Adaptive Multi-Model Intelligence Layer

ReguCompass AI uses specialized AI models for different governance tasks.

This improves:
- reliability
- speed
- cost efficiency
- audit quality

---

# Model Allocation

| Agent | Model | Purpose |
|---|---|---|
| Ingestor Agent | Gemini Flash | fast extraction |
| Analyst Agent | DeepSeek Chat | compliance reasoning |
| Auditor Agent | Claude Sonnet | verification |
| Risk Scoring Agent | Claude Sonnet | severity analysis |
| Summarization Layer | Gemini Flash | executive summaries |
| Offline Deployment | Llama3 | air-gapped banking environments |

---

# Why Multi-Model Routing?

Different models specialize in different tasks.

Using one model for everything:
- increases cost
- reduces reliability
- creates bottlenecks

ReguCompass AI dynamically routes tasks to the most suitable model.

---

# Gemini Flash

Used for:
- metadata extraction
- summarization
- preprocessing
- lightweight classification

Advantages:
- ultra-fast
- low latency
- cost efficient

---

# DeepSeek Chat

Used for:
- obligation extraction
- contextual reasoning
- department mapping
- compliance interpretation

Advantages:
- strong reasoning
- affordable inference
- structured outputs

---

# Claude Sonnet

Used for:
- hallucination prevention
- evidence verification
- citation validation
- risk scoring

Advantages:
- safer reasoning
- enterprise reliability
- strong long-context verification

---

# Llama3 (Offline Mode)

Used for:
- secure banking deployment
- air-gapped infrastructure
- local fallback inference

Advantages:
- offline execution
- zero external dependency
- banking compatibility

---

# Routing Flow

```text
Extraction?
 → Gemini Flash

Reasoning?
 → DeepSeek Chat

Verification?
 → Claude Sonnet

Offline Secure Mode?
 → Llama3
```

---

# Core Principle

> Specialized agents should use specialized models optimized for their governance tasks.