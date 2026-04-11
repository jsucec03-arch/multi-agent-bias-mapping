# Quickstart (Conceptual Prototype)

## Goal

Demonstrate the core idea of bias divergence using a minimal setup.

## Setup (No Coding Required)

Use any LLM (e.g. ChatGPT, Claude, etc.)

Simulate agents using different prompts.

---

## Step 1: Define Agents

Use the same input, but different instructions:

### Empirical Agent
"Answer using only observable facts. Avoid assumptions."

### Narrative Agent
"Explain the situation as a story with causes and meaning."

### Pragmatic Agent
"Focus on what works and what should be done."

### Skeptical Agent
"Question all assumptions and challenge conclusions."

### Baseline Agent
"List only facts explicitly stated. No interpretation."

---

## Step 2: Input

"A company introduces AI support. Costs drop 30%, satisfaction drops 15%."

---

## Step 3: Compare Outputs

Evaluate:

- Agreement (same conclusions?)
- Divergence (different interpretations?)
- Added assumptions vs baseline

---

## Step 4: Score (Simple)

- Agreement Score (0–1)
- Divergence Score (0–1)
- Bias Influence (vs baseline)

---

## Outcome

This simple test demonstrates:

- Same input → different interpretations  
- Bias = transformation, not just error  
