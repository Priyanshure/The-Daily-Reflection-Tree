# Daily Reflection Agent – Structured AI Agent Assignment

## Problem Understanding
The task requires a **deterministic decision tree** for daily reflection where:
- User answers → system asks next question → final output (insight + action)
- No open-ended hallucination
- Safe, repeatable, and controllable

## My Approach
I built a **rule-based agent** (not generative LLM) to:
- Eliminate hallucination risk entirely
- Ensure every user action leads to a predefined, safe output
- Use MCQ-style branches for clarity

## Decision Tree Explanation
The tree is depth = 2–3:
- Root: Goal completion (YES/NO)
- Second level: Emotional state (if YES) or failure reason (if NO)
- Third level (only for Distraction / Low motivation) for finer insight

Every leaf has two fixed components:
1. Insight (observational, not diagnostic)
2. Action (behavioral, not clinical)

## Guardrails (Critical for this assignment)
1. **No free-form generation** – All outputs are hardcoded strings.
2. **No mental health claims** – Words like “depression”, “anxiety”, “disorder” are absent.
3. **No extreme suggestions** – Actions are small, safe, and practical.
4. **Controlled vocabulary** – Users choose from limited, clear options.

> *“I prioritized deterministic reasoning over generative outputs to ensure reliability and reduce hallucination risk.”*

## AI Agent Explanation
This agent is a **finite-state machine**, not an LLM.  
It requires no API key, no prompt engineering, and no temperature tuning.  
It is 100% reproducible and verifiable – suitable for high-stakes reflection.
