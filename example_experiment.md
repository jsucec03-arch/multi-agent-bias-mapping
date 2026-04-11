# Example Experiment: Bias Divergence Test

## Goal

Demonstrate how different bias models produce different interpretations of the same input, and identify patterns of convergence and divergence.

## Setup

Define 4 agents, each representing a distinct interpretative bias:

- Empirical Agent → focuses only on observable facts, avoids assumptions  
- Narrative Agent → constructs meaning, causality, and story  
- Pragmatic Agent → evaluates usefulness and practical implications  
- Skeptical Agent → questions assumptions and challenges conclusions  

## Input

Provide the same input to all agents.

### Example Input

"A company introduces a new AI system to automate customer support. Within 3 months, costs are reduced by 30%, but customer satisfaction drops by 15%."

## Task

Each agent must answer:

1. What is happening in this situation?  
2. What is the most important factor?  
3. What should be done next?  

## Expected Behavior

Each agent should produce a distinct interpretation:

- Empirical → focuses on measurable trade-offs (cost vs satisfaction)  
- Narrative → frames a story (e.g., efficiency vs human connection)  
- Pragmatic → evaluates outcome (is this acceptable or not?)  
- Skeptical → questions data, assumptions, or hidden variables  

## Analysis

Compare outputs across agents and evaluate:

### 1. Convergence
- Do any agents reach similar conclusions?
- Which aspects of the situation are consistently identified?

### 2. Divergence
- Where do interpretations differ significantly?
- Which biases lead to conflicting conclusions?

### 3. Stability
- If input is slightly modified, do conclusions remain consistent?
- Which agents are more sensitive to changes?

## Hypothesis

Different bias models will produce systematically different interpretations, even with identical input.

Patterns of convergence may indicate:
- more stable interpretations
- lower interpretative distortion

Patterns of divergence may indicate:
- bias-driven distortion
- areas of ambiguity in the input

## Limitations

- This is a conceptual experiment  
- No quantitative metrics defined yet  
- Results depend on implementation of agents  

## Quantitative Evaluation (Agreement & Divergence Metrics)

To move beyond qualitative comparison, we introduce simple scoring metrics:

### 1. Agreement Score (AS)

Measures how similar agent conclusions are.

**Method:**
- Extract key conclusions from each agent (1–3 statements)
- Compare overlap between agents

**Scoring:**
- 1.0 → all agents agree (same conclusion)
- 0.5 → partial overlap
- 0.0 → completely different conclusions

**Example:**
- 3/4 agents recommend “improve customer satisfaction” → high agreement (~0.75)

---

### 2. Divergence Score (DS)

Measures how much interpretations differ.

**Method:**
- Identify conflicting conclusions or priorities
- Count distinct interpretation clusters

**Scoring:**
- 0.0 → no divergence (all agree)
- 1.0 → maximum divergence (all agents differ)

**Simple formula:**

DS = (number of unique interpretations - 1) / (number of agents - 1)

---

### 3. Bias Influence Score (BIS)

Measures how strongly a specific bias shapes conclusions.

**Method:**
- Compare each agent’s output to a neutral baseline (if defined)
- Evaluate how much the conclusion deviates

**Interpretation:**
- High BIS → strong bias-driven interpretation
- Low BIS → closer to shared/common interpretation

---

### 4. Stability Score (SS)

Measures consistency of interpretations under small input changes.

**Method:**
- Slightly modify input (e.g. change % values or context)
- Compare outputs before/after

**Scoring:**
- 1.0 → no change in conclusions
- 0.0 → completely different conclusions

---

## Composite Insight

Using these metrics together:

- High AS + Low DS → stable, low-distortion interpretation  
- Low AS + High DS → high uncertainty or strong bias influence  
- High SS → robust interpretation  
- Low SS → sensitive to framing / input variation  

---

## Baseline Agent (Minimal-Bias Reference)

### Purpose

The Baseline Agent serves as a reference point for evaluating bias influence.

It does not eliminate bias (which is impossible), but minimizes assumptions and applies consistent interpretation rules.

---

### Definition

The Baseline Agent operates under the following constraints:

- Uses only explicitly stated information  
- Avoids inference beyond given data  
- Does not assign meaning, intention, or narrative  
- Does not optimize for usefulness or outcome  
- Does not challenge assumptions unless contradictory  

---

### Behavior

Given an input, the Baseline Agent:

1. Extracts observable facts  
2. Lists measurable relationships  
3. Avoids conclusions unless directly supported  

---

### Example Output

Input:

"A company introduces a new AI system to automate customer support. Within 3 months, costs are reduced by 30%, but customer satisfaction drops by 15%."

Baseline Agent Output:

- Costs decreased by 30% after implementation  
- Customer satisfaction decreased by 15%  
- There is a trade-off between cost reduction and satisfaction  
- No causal explanation is confirmed by the data  

---

### Role in Evaluation

The Baseline Agent is used to:

- Compare deviation of other agents (Bias Influence Score)  
- Identify added assumptions or interpretations  
- Serve as a minimal-reference interpretation  

---

### Limitations

- Still subject to structural bias (selection, framing)  
- Cannot represent “true objectivity”  
- May under-interpret meaningful patterns  

---

### Integration into Metrics

- Used as reference for Bias Influence Score (BIS)  
- Helps define “distance from minimal interpretation”  
- Anchors comparison across agents  
