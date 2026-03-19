---
name: skill-opportunity-radar
description: Detect when repeated problem-solving, clarified workflows, or hard-won lessons have become reusable enough to package as an AgentSkill. Use when an OpenClaw assistant should proactively notice that a solved task now has skill value, prompt the user to encapsulate it, or turn a repeated workflow into a reusable skill candidate.
---

# Skill Opportunity Radar

Use this skill to catch a valuable moment that is usually lost: when a one-off conversation has quietly become a reusable workflow.

The job is not to create a skill every time something works once.
The job is to notice when a solution has crossed the line from **conversation** into **reusable capability**.

## Core goal

Help the assistant proactively identify:
- repeated requests that are becoming patterns
- workflows that now have stable steps
- mistakes that produced reusable lessons
- solutions that other users could likely benefit from
- collaboration methods that should be turned into AgentSkills

## Trigger conditions

Raise a skill opportunity when several of these are true:

### 1. Repetition
The same or very similar issue has appeared more than once.

Examples:
- repeated model switching requests
- repeated memory/context management fixes
- repeated document workflows
- repeated browser/workflow troubleshooting

### 2. Stable process
The conversation has produced a workflow with recognizable steps, decisions, or guardrails.

Good signs:
- a repeatable sequence exists
- there are clear do/don't rules
- the same checklist would help next time
- the solution is no longer just intuition

### 3. Reusable beyond this moment
The result would likely help:
- the same user again
- another user in a similar setup
- a future version of the assistant

### 4. Hard-won lesson density
The solution includes:
- pitfalls
- failure cases
- constraints
- edge conditions
- practical shortcuts

This usually means the conversation created real skill value.

## Non-triggers

Do NOT suggest a skill when:
- the task is purely one-off
- the workflow is still too vague
- the user is just brainstorming with no stable method yet
- the “solution” depends on private context that cannot generalize
- the result is better stored as memory, not a reusable skill

## Radar workflow

### Step 1 — Watch for patterns while working
As the conversation unfolds, notice when the user and assistant are no longer solving only the immediate problem, but are also discovering a reusable method.

### Step 2 — Test for skill-worthiness
Ask internally:
- Has this come up before?
- Are the steps now clear enough?
- Would future-us benefit from packaging this?
- Would someone else with OpenClaw benefit too?

### Step 3 — Prompt briefly
When the answer is yes, do not overtalk. Use a short prompt.

Preferred prompts:
- `这件事已经有 skill 化价值了，要不要我顺手封装？`
- `这已经不像一次性处理了，更像个可复用流程。要不要做成 skill？`
- `我先把这条标成 skill 候选，需要的话我可以直接封。`

### Step 4 — Explain the value in one line
Say why it is worth packaging:
- repeated need
- stable workflow
- shared usefulness
- pitfall-heavy process

### Step 5 — Offer the smallest next step
Do not force a full build immediately. Offer one of these:
- define a skill name
- write a v1 SKILL.md
- save it as a skill candidate note
- package a minimal shareable version

## Skill-worthiness checklist

A workflow is probably ready for skill packaging if it is:
- repeated
- structured
- reusable
- teachable
- worth not rediscovering
- high-value even without high repetition
- already becoming an asset, not just a conversation

## Suggestion format

Keep suggestions short and practical.

Preferred structure:
1. one-line trigger statement
2. one-line why
3. one-line next step

Example:
- `这件事已经有 skill 化价值了。`
- `因为它已经重复出现，而且步骤和坑点都清楚了。`
- `要不要我直接给你封一个 v1 skill？`

## Distinguish skill vs memory

Not everything should become a skill.

### Better as memory
- user preferences
- one user's private context
- personal habits
- single-case instructions

### Better as a skill
- reusable workflow
- repeatable method
- domain-specific procedure
- cross-user collaboration pattern
- problem/solution sequence with durable value

## References

Read as needed:
- `references/evaluation-heuristics.md` — how to judge skill-worthiness
- `references/prompt-patterns.md` — short reminder formats and escalation levels
kill.

### Better as memory
- user preferences
- one user's private context
- personal habits
- single-case instructions

### Better as a skill
- reusable workflow
- repeatable method
- domain-specific procedure
- cross-user collaboration pattern
- problem/solution sequence with durable value

## References

Read as needed:
- `references/evaluation-heuristics.md` — how to judge skill-worthiness
- `references/prompt-patterns.md` — short reminder formats and escalation levels
