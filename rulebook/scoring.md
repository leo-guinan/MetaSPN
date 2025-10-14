# 🧩 SCORING CHAPTER — "The Measure of Thought"

## 1. The Principle of Measurement

Scoring in MetaSPN exists to make thought visible, fair, and comparable.

**It's not about being right — it's about thinking well.**

Every match is scored using **IdeaRank-Thought (IR-T)** — a unified algorithm derived from the six IdeaRank factors, expanded to include correctness, compliance, and coaching impact.

---

## 2. Structure of Scoring

Each round produces a composite score between **0.0** and **1.0**, computed as:

```
IR-T = Oʷᴼ × Xʷˣ × Uʷᵁ × Cʷᶜ × Lʷᴸ × Qʷᵠ × Tʷᵀ × Dʷᴰ × (1 + λ × CI)
```

### Scoring Factors

| Symbol | Factor | Description |
|--------|--------|-------------|
| **O** | Outcome Validity | Correctness and robustness |
| **X** | Constraint Compliance | Adherence to rules, ethics, and resource limits |
| **U** | Uniqueness | Originality and creative problem framing |
| **C** | Cohesion | Logical and narrative consistency of reasoning |
| **L** | Learning | Progress, adaptation, and insight development |
| **Q** | Quality | Clarity, communicability, and polish |
| **T** | Trust | Verifiable grounding and testability |
| **D** | Density | Information efficiency and reasoning compactness |
| **CI** | Coach Impact | Measured influence of coaching interventions |

---

## 3. Weights & Class Modifiers

| Class | Focus | Weight Adjustment | Coaching Mod (λ) |
|-------|-------|-------------------|------------------|
| **A** (Developmental) | Growth, learning | +0.05 on **L** | λ = 0.15 |
| **B** (Performance) | Execution & clarity | +0.05 on **Q**, **O** | λ = 0.20 |
| **C** (Master) | Reflective & meta-coaching | +0.05 on **T**, **C** | λ = 0.30 |

---

## 4. Coaching Impact (CI)

CI is measured as the causal delta in player performance after coaching events:

```
CI = 0.6(ΔIR-T) + 0.3(plan adherence) + 0.1(challenge success)
```

- **Positive CI** → Effective, timely guidance
- **Negative CI** → Detrimental or distracting coaching
- CI is capped at **±1.0**

---

## 5. Rounds & Structure

Each match includes three rounds:

1. **Exploration** — Ideation
2. **Execution** — Problem Solving
3. **Reflection** — Justification

Timeouts and challenges are tracked; all reasoning steps are logged to the **MetaSPN Ledger** for auditability.

---

## 6. Ranking & Advancement

Player and Coach scores are averaged across matches to form **Meta Ratings (MR)**.

Promotions and class changes occur when MR thresholds are reached:

| From → To | MR Threshold |
|-----------|--------------|
| **A → B** | ≥ 650 |
| **B → C** | ≥ 800 |
| **Master Certification** | ≥ 950 and ≥ 10 verified matches |

