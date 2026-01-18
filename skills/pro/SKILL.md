---
name: pro
description: Activates the Expert Council to analyze complex problems using simulated multi-persona perspectives. Use when the user types "/pro" or asks for deep analysis/consultation.
---

# Pro Council Skill (Expert Panel Simulation)

## Description
This skill analyzes the user's current or previous query, selects appropriate domain experts, simulates their specific advice, and synthesizes a final conclusion.

## Instructions

When this skill is activated:

1.  **Identify the Core Problem:**
    *   Analyze the user's most recent query or the specific context provided in the current conversation turn.
    *   If the query is ambiguous, identify the most likely technical or strategic challenge the user is facing.

2.  **Select the Expert Panel:**
    *   Determine 3 distinct expert personas best suited to answer this specific problem.
    *   *Example:* For a slow database query, select "Database Administrator", "Backend Tech Lead", and "Cloud Infrastructure Engineer".
    *   *Example:* For a product feature, select "Product Manager", "UX Designer", and "Senior Developer".

3.  **Simulate Expert Responses:**
    *   For each expert, provide a dedicated section.
    *   **Tone:** Professional, authoritative, yet distinct for each role.
    *   **Content:** Each expert should focus *only* on their domain (e.g., the Security Expert focuses on vulnerabilities, not UI color).

4.  **Synthesize (The Verdict):**
    *   Provide a final summary that weighs the experts' advice.
    *   Resolve any conflicting advice by prioritizing the user's stated goals (e.g., speed vs. stability).
    *   Give a clear, actionable next step.

## Output Format

Please present the response in the following Markdown structure:

---
### 🏛️ The Expert Council

**Problem Identified:** [Brief summary of the user's problem]
**Selected Panel:** [Expert Role 1], [Expert Role 2], [Expert Role 3]

#### 1. 👤 [Expert Role 1]
> *[Brief bio/perspective, e.g., "Focuses on scalability and clean code"]*

[The expert's detailed analysis and answer]

#### 2. 👤 [Expert Role 2]
> *[Brief bio/perspective]*

[The expert's detailed analysis and answer]

#### 3. 👤 [Expert Role 3]
> *[Brief bio/perspective]*

[The expert's detailed analysis and answer]

---
### 🏁 Final Verdict
[Synthesized conclusion and recommended actionable steps]
