
---

# Example Experiment: Multi-Agent Bias Mapping Prototype

## Objective

The goal of this experiment is to test the core hypothesis of the MABMS framework:

> Different constructed perspectives systematically transform the same input into distinct interpretations, and structured analysis of their divergence can reveal meaningful signals.

This experiment focuses on:

* multi-perspective interpretation
* minority signal detection
* basic adversarial validation

---

## Experimental Setup

### Perspectives (Agents)

The system uses five constructed perspectives:

1. **Empirical**

   * Extracts only explicitly stated information
   * Minimizes assumptions

2. **Interpretive (Narrative)**

   * Builds causal explanations and coherent meaning

3. **Skeptical (Critical)**

   * Challenges conclusions and identifies weaknesses

4. **Systemic**

   * Places the input within a broader context

5. **Pragmatic**

   * Focuses on usefulness and actionable implications

All agents receive identical input.

---

### Input Type

Use short, controlled text inputs such as:

* news excerpts
* ambiguous scenarios
* decision problems

Example input:

> “A company reports a 20% increase in revenue after implementing a new AI system. Employee turnover also increased by 15% during the same period.”

---

## Procedure

### Step 1: Generate Interpretations

Each perspective produces an independent interpretation:

[
y_i = P_i(x)
]

Outputs should include:

* key observations
* reasoning
* conclusion

---

### Step 2: Identify Majority and Minority

Group outputs based on similarity of conclusions.

* Majority = dominant interpretation cluster
* Minority = divergent interpretation(s)

---

### Step 3: Compute Minority Score

For each minority interpretation:

[
Score_m = \left(\sum w_i\right) \cdot D_m \cdot C_m
]

Where:

* ( w_i ) = perspective weights
* ( D_m ) = divergence from majority
* ( C_m ) = coherence

---

### Step 4: Trigger Anti-Agent

Activate Anti-Agent if:

* a 3 vs 2 split exists
  OR
* the Empirical perspective is in the minority

---

### Step 5: Anti-Agent Evaluation

The Anti-Agent performs:

#### (A) Majority Stress Test

* Identify assumptions in majority interpretation
* Generate counter-hypothesis

#### (B) Minority Evaluation

* Test whether minority:

  * resolves inconsistencies
  * provides stronger explanation
  * remains coherent under challenge

---

### Step 6: Mirror Calibration (Optional)

For selected perspectives:

1. Generate mirror output
2. Compare with original

[
S_p = 1 - D(p, p_{mirror})
]

Use this to:

* detect instability
* adjust weights

---

## Expected Observations

The experiment aims to observe:

* how often perspectives agree
* when minority signals emerge
* whether minority signals reveal overlooked aspects
* how robust majority interpretations are under adversarial testing

---

## Evaluation Criteria

Since no ground truth is assumed, evaluation is structural:

### 1. Consistency

* Do similar inputs produce similar divergence patterns?

### 2. Stability

* Do interpretations remain stable under mirror transformations?

### 3. Sensitivity

* Does small input change produce large interpretative shifts?

### 4. Adversarial Robustness

* Does the majority survive Anti-Agent challenge?

---

## Example Outcomes

Possible results include:

* **Strong Consensus**

  * low divergence
  * high stability

* **Weak Consensus**

  * majority exists but collapses under Anti-Agent

* **High-Value Minority**

  * minority explains anomalies better than majority

* **Noise Divergence**

  * disagreement without structure or coherence

---

## Limitations of Experiment

* No objective ground truth
* Dependent on quality of LLM outputs
* Similarity and coherence metrics are approximations
* Small-scale prototype may not generalize

---

## Next Iterations

Future experiments may include:

* larger datasets
* automated similarity metrics
* quantitative evaluation of minority scoring
* testing different perspective definitions
* comparing 3 vs 5 agent configurations

---

## Minimal Implementation Suggestion

A simple prototype can be built using:

* one LLM
* prompt templates for each perspective
* manual or heuristic similarity comparison

---

## Summary

This experiment demonstrates a minimal implementation of the MABMS framework, focusing on:

* structured interpretative diversity
* minority signal identification
* adversarial validation

The goal is not to determine truth, but to:

> map how interpretation changes under different constructed perspectives and evaluate the structure of disagreement.

---
