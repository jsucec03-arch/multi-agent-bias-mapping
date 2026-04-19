
---

# Quickstart: Multi-Agent Bias Mapping System (MABMS)

## Purpose

This quickstart provides a minimal setup for experimenting with the MABMS framework.

The goal is not full implementation, but to:

* generate multi-perspective interpretations
* observe divergence
* identify minority signals
* apply basic adversarial evaluation

---

## What You Need

* Access to any LLM (e.g., ChatGPT, API, or local model)
* Ability to run 5 separate prompts
* Optional: spreadsheet or simple script for comparison

No coding is required for the basic version.

---

## Step 1: Define the Input

Start with a short, ambiguous input.

Example:

> “A company reports a 20% increase in revenue after implementing a new AI system. Employee turnover also increased by 15% during the same period.”

Keep inputs:

* short
* information-dense
* slightly ambiguous

---

## Step 2: Run 5 Perspective Prompts

Use the same input for each perspective.

---

### 1. Empirical Perspective

**Prompt:**

> Analyze the input using only explicitly stated information.
> Avoid assumptions, interpretations, or inferred causality.
> List observable facts and derive a minimal conclusion.

---

### 2. Interpretive (Narrative) Perspective

**Prompt:**

> Construct a coherent explanation of the situation.
> Identify possible causal relationships and provide a meaningful interpretation.

---

### 3. Skeptical (Critical) Perspective

**Prompt:**

> Critically evaluate the input.
> Identify weaknesses, missing information, and potential alternative explanations.
> Challenge any implied conclusions.

---

### 4. Systemic Perspective

**Prompt:**

> Place this situation within a broader system.
> Consider external factors, dependencies, and wider implications.

---

### 5. Pragmatic Perspective

**Prompt:**

> Focus on practical implications.
> What actions should be taken based on this information?
> What is useful or actionable?

---

## Step 3: Compare Outputs

Read all 5 outputs and identify:

* which conclusions are similar
* which differ significantly

---

### Define:

* **Majority** → interpretations that broadly agree
* **Minority** → interpretations that diverge

---

## Step 4: Identify Minority Signal

Ask:

* Is the minority pointing out something others missed?
* Is it coherent and internally consistent?
* Is it simply noise or a meaningful alternative?

---

## Step 5: Apply Anti-Agent (Manual Version)

If:

* there is a clear split (e.g., 3 vs 2)
  OR
* the empirical perspective disagrees with the majority

Run this prompt:

---

### Anti-Agent Prompt

> The majority interpretation is: [summarize majority]
> Challenge this conclusion.
> Identify hidden assumptions, weaknesses, and generate a strong counter-interpretation.
> Then evaluate whether the minority interpretation provides a more robust explanation.

---

## Step 6: Optional — Mirror Test

Pick one perspective and run:

---

### Mirror Prompt (Example)

> Re-analyze the input by inverting the core assumptions of your previous reasoning.
> Provide an alternative interpretation based on these inverted constraints.

---

Compare:

* original vs mirror output

Ask:

* does the conclusion change drastically?
* is the reasoning stable?

---

## Step 7: Interpret Results

You are not looking for “truth”.

Instead, evaluate:

* where perspectives agree
* where they diverge
* whether minority signals are meaningful
* whether majority conclusions are robust

---

## What to Look For

### Strong Case

* perspectives converge
* Anti-Agent fails to break majority

---

### Interesting Case

* minority explains something majority missed
* Anti-Agent supports minority

---

### Weak Case

* outputs diverge randomly
* no coherent structure

---

## Minimal Output Format

You can summarize results like this:

```
Input:
[Text]

Perspectives:
Empirical: ...
Narrative: ...
Skeptical: ...
Systemic: ...
Pragmatic: ...

Majority:
...

Minority:
...

Anti-Agent Result:
...

Final Insight:
...
```

---

## Tips

* Keep inputs simple at first
* Don’t overthink scoring
* Focus on patterns, not precision
* Run multiple examples

---

## Next Steps

After trying this:

* test multiple inputs
* compare patterns across runs
* experiment with fewer agents (e.g., 3 instead of 5)
* try simple scoring methods

---

## Summary

This quickstart demonstrates the core idea of MABMS:

> Multiple constructed perspectives transform the same input differently, and structured analysis of their divergence reveals insights not visible from a single interpretation.

---
