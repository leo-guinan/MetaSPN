## A1. Factor Computation Details

| Factor | Source Data | Computational Method |
|---------|--------------|----------------------|
| **U (Uniqueness)** | Graph similarity vs league corpus | Novelty z-score → sigmoid normalization |
| **C (Cohesion)** | Reasoning map analysis | Structural consistency, linguistic coherence |
| **L (Learning)** | Early/late checkpoint delta | Skill gain function over time |
| **Q (Quality)** | Human & AI rubric | Readability, completeness, clarity metrics |
| **T (Trust)** | Test logs, citations | Pass rate × citation quality |
| **D (Density)** | Tokens vs valid nodes | Information-per-step compression ratio |

## A2. Gate Formulas

* O (Outcome Validity):
  * 𝑂 = 0.7 × correctness + 0.3 × robustness
* X (Constraint Compliance):
  * 𝑋 = 1 − violation_penalty

## A3. Coaching Signal Processing
All coaching events are timestamped and cross-referenced with reasoning improvement metrics.  
Timeout deltas are measured over 3 checkpoints (pre/post).  
Plan adherence is calculated using semantic similarity of the prebrief plan to executed reasoning.

## A4. Integrity Protocols
- **Ledger Hashing:** Every match’s reasoning data is stored as an immutable hash for verification.  
- **Replay Validation:** AI models and human replays are cross-run for reproducibility.  
- **Anti-Gaming:** Multiplicative scoring punishes over-optimization of single factors.

## A5. Output Metrics
Each match produces:

- **IR-T Raw Score (0–1)**  
- **IR-T Class Adjusted Score**  
- **Coach Impact Index (CI)**
- **Meta Rating (MR)**
- **Entropy Index (EI) for tiebreaks**
  

## A6. Visualization Schema

Reason Map Overlays display:

* Node color → factor weight contribution
* Edge thickness → cohesion strength
* Halo glow → coaching intervention zones

## A7. Open Science Clause

All algorithms, rubrics, and evaluation criteria are open standard under the MetaSPN Charter.
Any team can audit or replicate scoring through the open IdeaRank SDK.
