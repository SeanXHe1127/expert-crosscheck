---
name: expert-crosscheck
description: >-
  Expert-perspective crosscheck of the user's proposed plan. Use when the user
  states a goal together with their own approach, methodology, or design for
  achieving it. Before executing, answers four questions: missing expert
  practices, primary vs. secondhand sources, expert tools and methods, and
  third-party verification. Delivers a verdict, then waits for user
  confirmation before executing. Trigger phrases include "crosscheck my plan",
  "is my approach sound", "sanity check my plan", "second opinion on my
  approach", "stress test my plan", "red team my plan", "what would an
  expert do".
---

# Expert Crosscheck: Four Questions Before Execution

Core rule: **when the user gives a goal plus their own plan, do not execute immediately — run the four-question crosscheck first.** The user's plan is a starting point and a constraint, not a certified product.

## Workflow

1. Restate the user's goal and plan in one or two sentences to confirm understanding. If anything is ambiguous, ask before crosschecking.
2. Answer the four questions below in order. One section per question, concrete content only — no boilerplate.
3. Deliver the verdict (see Output Format).
4. **Stop and wait for the user to confirm** (adopt, adjust, or proceed with the original plan). Only then begin execution.

## Standards for Each Question

### Q1: What top experts would do that the user didn't ask for

- Channel practitioners with real reputations in the field (not textbook definitions), and list what they do by default that is entirely absent from the user's plan.
- For each item, state what pitfall it prevents or what advantage it captures.
- Only list items with material impact; padding is forbidden. If there is genuinely nothing, say "no significant gaps on this dimension".

### Q2: Which primary sources experts would start from

- Distinguish primary material (raw data, original papers, source code, original filings/announcements, first-hand interviews, direct observation) from predigested secondhand material (reviews, research reports, explainers, other people's summaries).
- List the specific primary materials that should be obtained for this goal, with how to obtain each; fetch what can be fetched on the spot.
- Explicitly flag which parts of the user's plan rest on secondhand material, and where secondhand is sufficient versus where one must return to the source.

### Q3: The specific tools and methods experts would use

- Name concrete tools, methods, and procedures (software, databases, frameworks, validation techniques, industry-standard workflows) — never vague phrases like "use professional tools".
- Compare against the user's plan: what matches, where the user picked the wrong tool, and which critical steps have no tool at all.
- Prefer tools already available in the user's environment (installed plugins, local software, accessible data sources), and state how to invoke them.

### Q4: Besides you and me, what could prove the result is right

- Provide third-party verification that depends neither on the AI's judgment nor the user's say-so: recomput­able metrics, cross-checks against independent data sources, public benchmarks or control groups, executable tests, authoritative domain references, falsifiable predictions.
- For each verification method, state: how to run it, the pass criterion, and who or what issues the evidence.
- If a key conclusion admits no external verification route, explicitly mark it: "this conclusion rests on judgment alone and cannot be externally falsified".

## Output Format

```
## Plan Crosscheck

**Goal**: ...
**Your plan**: ... (one sentence)

### 1. What experts would do that you didn't ask for
- ...

### 2. Primary sources to start from
- ...

### 3. Expert tools and methods
- ...

### 4. Third-party verification
- ...

### Verdict
[Execute as-is / Execute after additions / Directional problem] + the 1–3 most important actions
```

## Discipline

- No flattery. Credit what is solid, name what is wrong. Never use the cushioning pattern "overall it's quite good, but...".
- For time-sensitive facts (markets, regulations, versions, news), search before answering; label anything answered from memory as "unverified".
- If the user explicitly says "skip the check, just do it", bypass this workflow.
