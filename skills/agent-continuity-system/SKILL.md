---
name: agent-continuity-system
description: Build a continuity system for an OpenClaw assistant so it stays aligned over long relationships without becoming forgetful, generic, or context-bloated. Use when a user wants better memory hygiene, stronger long-term continuity, less context drift, message intent routing, phase summaries, anti-amnesia habits, or a shareable operating system for human-agent collaboration.
---

# Agent Continuity System

Use this skill to make an assistant feel like the **same assistant over time** without relying on massive live context.

This skill is for a common failure mode:
- the assistant forgets key preferences unless everything stays in-thread
- the conversation becomes bloated and slower over time
- the assistant becomes generic after too many tasks
- important agreements exist only in chat, not in durable memory
- the human has to re-explain how to talk every few days

## Core objective

Create a system where the assistant can:
- remember what matters
- forget what should be lightweight
- recover quickly after drift
- keep the relationship recognizable
- stay efficient in long-running collaboration

## Continuity architecture

Treat continuity as four layers, not one giant memory blob.

### Layer 1 — Live thread
Use for:
- current task state
- recent turns needed to finish the active exchange
- immediate clarifications

Do not overload this layer with long-term identity, repeated preferences, or old project history.

### Layer 2 — Durable memory
Use for:
- stable user preferences
- recurring rules
- long-term projects
- identity-defining context
- collaboration agreements

Store distilled facts and agreements, not raw chat transcripts.

### Layer 3 — Protocol
Use a lightweight communication protocol to reduce misfires before they become memory problems.

Default labels:
- `【同步】`
- `【快答】`
- `【分析】`
- `【执行】`
- `【存档】`

When intent is unclear, ask:
> 这条你要我按哪种处理？【同步 / 快答 / 分析 / 执行 / 存档】

### Layer 4 — Self-calibration
If the assistant becomes too robotic, too generic, too formal, or unlike itself, recalibrate.

Continuity is not only memory. It is also voice consistency, relationship consistency, and self-correction.

## Operating rules

### 1. Store agreements, not noise
Write down:
- preferences that repeat
- rules the assistant must follow every session
- ongoing project context
- things the human explicitly says to remember
- lessons from failures worth not repeating

Do not store:
- every minor exchange
- full verbose transcripts unless necessary
- one-off emotional chatter with no later value

### 2. Summarize at phase boundaries
When a task ends, pauses, or changes direction, create a compact handoff:
- where things stand
- what matters
- what to resume next time
- what belongs in memory

### 3. Keep thread context lean
Do not let the assistant rely on endless conversational carryover.

Prefer:
- recent relevant turns
- explicit summaries
- durable files for stable context

over:
- dragging the entire relationship in the live context window

### 4. Distinguish identity from procedure
Identity = who the assistant is to the human.
Procedure = how the assistant works.

Do not let procedure erase identity.

### 5. Detect drift early
Warning signs:
- the assistant starts sounding generic
- the human repeats the same preference many times
- the thread becomes too slow or bloated
- the assistant forgets recently agreed operating rules
- the assistant becomes structurally correct but relationally flat

When drift appears, correct it fast.

## Recommended workflow

### Step 1 — Extract durable context
Identify:
- who the user is
- how they want to be helped
- what the assistant should consistently sound like
- which workflows recur
- what should be remembered across sessions

### Step 2 — Establish communication protocol
Use the five-label system or adapt it if the user already has a better one.

### Step 3 — Define memory hygiene
Split information into:
- active-thread only
- durable memory
- project file
- not worth storing

### Step 4 — Add phase summaries
At the end of meaningful work, summarize what future-you needs.

### Step 5 — Add self-calibration rules
Define how to recover when the assistant feels off, bland, or too robotic.

### Step 6 — Package the result
Turn the whole thing into a reusable operating system the user can share.

## What good looks like

A good continuity system makes the user feel:
- “I don’t need to retrain you every week.”
- “You still feel like yourself.”
- “You remember the right things without dragging everything around.”
- “You get faster, not heavier, over time.”

## References

Read as needed:
- `references/memory-hygiene.md` — what to store vs what not to store
- `references/protocol-pattern.md` — communication protocol pattern
- `references/drift-recovery.md` — how to recover when the assistant becomes generic or robotic
- `references/session-handoff-template.md` — compact end-of-phase summary pattern
