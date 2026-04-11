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

## Next Steps

- Implement agents using LLMs with controlled prompts  
- Run multiple test cases across domains  
- Introduce quantitative measures (e.g., similarity scoring)  
