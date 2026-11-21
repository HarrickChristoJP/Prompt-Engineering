# 📚 Hands-on Mastery of Prompt Engineering

> An academic lab assignment exploring how different prompting techniques influence the accuracy, consistency, reasoning, and reliability of Large Language Models (LLMs).

---

## 🎯 Overview

This repository contains a complete, structured prompt engineering experiment report covering three core techniques tested using **Gemini 1.5 Flash** on **Google AI Studio**:

| # | Technique Pair | Task |
|---|---|---|
| 1 | **Zero-Shot vs Few-Shot Prompting** | Sentiment Classification |
| 2 | **Standard vs Chain-of-Thought (CoT)** | Multi-step Logical Reasoning |
| 3 | **Unstructured vs Structured JSON Output** | Product Information Extraction |

All experiments were conducted manually — **no code, no API calls, no scripts**.

---

## 📂 Repository Structure

```
Prmotp Engineering/
│
├── README.md                        ← You are here
└── prompt-engineering-report.md    ← Full report: prompts, outputs,
                                       evaluation tables & conclusions
```

---

## 🧪 Experiment Summary

### Phase 2 — Zero-Shot vs Few-Shot (Sentiment Classification)

**Task:** Classify 6 customer feedback statements as `Positive`, `Negative`, or `Neutral`.

| Experiment | Technique | Accuracy |
|---|---|---|
| A | Zero-Shot | 6/6 (100%) |
| B | Few-Shot (4 examples) | 6/6 (100%) |

**Key Finding:** Both techniques matched on this dataset. Few-shot provides a critical advantage on mixed/ambiguous statements (e.g., A4 — excellent sound but poor battery) by anchoring the classification pattern through examples, reducing model interpretation variance on edge cases.

---

### Phase 3 — Chain-of-Thought Prompting (Logical Reasoning)

**Task:** Solve 4 multi-step math and logic problems.

| Experiment | Technique | Accuracy | Reasoning Visible? |
|---|---|---|---|
| C | Standard (direct answer) | 4/4 (100%) | ❌ |
| D | Chain-of-Thought | 4/4 (100%) | ✅ |

**Key Finding:** Accuracy was equal on these problems, but CoT output is fully verifiable and auditable. For complex multi-step problems with 5+ stages, research shows CoT improves accuracy by 20–40% over standard prompting.

---

### Phase 4 — Structured JSON Output (Data Extraction)

**Task:** Extract product information from 3 customer reviews.

| Experiment | Technique | Schema Compliance |
|---|---|---|
| E | Unstructured (no schema) | 0/9 fields (Markdown prose returned) |
| F | Structured JSON (schema defined) | 9/9 fields ✅ |

**Key Finding:** Without schema instructions, the model defaults to human-readable Markdown. With an explicit JSON schema, the model returns perfectly typed, machine-parseable data — directly usable in a database or API.

---

## 🔧 Testing Environment

| Setting | Value |
|---|---|
| **Platform** | Google AI Studio |
| **Model** | Gemini 1.5 Flash (gemini-1.5-flash-002) |
| **Temperature** | 1.0 (default) |
| **Interface** | Manual — single-turn prompts |
| **Code Used** | ❌ None |
| **API Used** | ❌ None |
| **Date Tested** | 20 November 2026 |

---

## 📄 Report Contents

The full deliverable is [`prompt-engineering-report.md`](./prompt-engineering-report.md):

- ✅ Title, student detail placeholders, and abstract
- ✅ Introduction, objective, tools, and methodology
- ✅ All **6 experiment prompts** — exact, verbatim, copy-paste ready
- ✅ All **6 model outputs** — verbatim from Gemini 1.5 Flash
- ✅ Pre-defined expected answers with reasoning
- ✅ Accuracy comparison tables for all phases
- ✅ Format and schema compliance checklists
- ✅ Detailed analysis for each phase
- ✅ Overall findings and cross-phase discussion
- ✅ Conclusion and academic references (8 sources)

---

## 📋 Expected Answers Reference

### Phase 2 — Sentiment Classification

| ID | Statement | Expected | Result |
|---|---|---|---|
| A1 | Fast delivery, perfect condition | **Positive** | ✅ Both |
| A2 | App crashes on account open | **Negative** | ✅ Both |
| A3 | Parcel arrived, item not used | **Neutral** | ✅ Both |
| A4 | Excellent sound, poor battery | **Negative** (mixed → dominant) | ✅ Both |
| A5 | Support solved issue quickly | **Positive** | ✅ Both |
| A6 | Wrong colour, damaged box | **Negative** | ✅ Both |

### Phase 3 — Logical Reasoning

| Q# | Question | Expected Answer | Result |
|---|---|---|---|
| Q1 | 4 apples × \$3 + 5 oranges × \$2 | **\$22** | ✅ Both |
| Q2 | 60 km/h × 2.5 hours | **150 km** | ✅ Both |
| Q3 | % boys after 3 join 30-student class | **45.45%** | ✅ Both |
| Q4 | John > Mary > Tom — who is youngest? | **Tom** | ✅ Both |

### Phase 4 — JSON Schema Fields

Required: `product_name` (string) · `price_usd` (number) · `rating_out_of_5` (number) · `pros` (array) · `cons` (array)

---

## 🎓 Key Concepts

| Concept | Definition |
|---|---|
| **Zero-Shot Prompting** | Task completed with instructions only — no examples provided. |
| **Few-Shot Prompting** | 2–5 labelled input→output examples included in the prompt. |
| **Chain-of-Thought (CoT)** | Model instructed to reason step-by-step before giving a final answer. |
| **Structured Output** | Explicit schema (e.g., JSON) specified in the prompt for machine-readable output. |
| **In-Context Learning** | Model adapts its behaviour at inference time based on examples or instructions in the prompt. |

---

## 📚 References

| # | Citation |
|---|---|
| 1 | Brown et al. (2020) — *Language Models are Few-Shot Learners* · arXiv:2005.14165 |
| 2 | Wei et al. (2022) — *Chain-of-Thought Prompting Elicits Reasoning in LLMs* · arXiv:2201.11903 |
| 3 | White et al. (2023) — *A Prompt Pattern Catalog* · arXiv:2302.11382 |
| 4 | Google DeepMind (2024) — *Gemini: A Family of Highly Capable Multimodal Models* |
| 5 | Google AI Studio — https://aistudio.google.com |
| 6 | Sahoo et al. (2024) — *A Systematic Survey of Prompt Engineering* · arXiv:2402.07927 |
| 7 | Kojima et al. (2022) — *Large Language Models are Zero-Shot Reasoners* · arXiv:2205.11916 |
| 8 | Liu et al. (2023) — *Pre-train, Prompt, and Predict* · ACM Computing Surveys |

---

## 📝 License

This project is submitted as part of an academic assignment. All content is original work by the student unless cited above.

---

*Last updated: November 2026 · Model: Gemini 1.5 Flash · Platform: Google AI Studio*
