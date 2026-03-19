---
name: openclaw-communication-protocol
description: Create and apply a lightweight communication protocol between an OpenClaw user and their assistant to reduce misfires, improve response speed, and keep context manageable. Use when the user wants smoother collaboration, clearer message intent, reusable message tags, better memory handoff, or a shareable communication framework for OpenClaw assistants.
---

# OpenClaw Communication Protocol

Use this skill to help a user and their OpenClaw assistant communicate with less ambiguity and less context bloat.

## Core workflow

1. Clarify whether the user wants to:
   - design a new protocol
   - improve an existing protocol
   - apply a protocol to current conversations
   - package a protocol for sharing with others
2. Keep the protocol simple enough to remember in daily use.
3. Default to five intent labels unless the user requests a different system:
   - `【同步】` share status only
   - `【快答】` short answer first
   - `【分析】` deeper reasoning
   - `【执行】` produce output or complete the task
   - `【存档】` save durable information
4. Add an assistant-side fallback rule: when the user does not label a message and intent is unclear, ask them to choose one of the five labels.
5. Separate active context from durable memory:
   - active context contains the current task and recent useful turns
   - durable memory contains stable preferences, recurring rules, and long-term agreements
6. End with a compact operating agreement the user can actually follow.

## Recommended protocol structure

When writing a protocol, prefer this structure:

### 1. Goal
State that the protocol exists to improve flow, reduce misunderstandings, and keep the assistant responsive.

### 2. Core principles
Recommend these defaults:
- 按任务分流
- 按重要性存档
- 按阶段总结
- 按用途沟通

### 3. Intent labels
Define the five labels with plain-language meanings.

### 4. Assistant defaults
Specify what the assistant should do when:
- the user does not label a message
- the user is only syncing state
- the user wants execution
- a task is ending, pausing, or switching

### 5. Quick examples
Provide one-line examples for each label.

### 6. Context hygiene
Add lightweight rules for:
- separating chat from task execution
- summarizing at phase boundaries
- saving stable preferences outside the live thread

## Rules to include by default

Unless the user asks otherwise, include these rules:

- Do not default to copywriting/output mode when the user is only sharing status.
- Ask for label selection when intent is unclear.
- Summarize progress when a task completes or pauses.
- Save only distilled durable agreements into memory, not raw conversation dumps.

## Mandatory enforcement rules

These rules apply to every agent using this protocol:

### 1. Always prompt for label when unclear
When the user sends a message without a label and the intent is not obvious, the agent MUST ask:
> 这条你要我按哪种处理？【同步 / 快答 / 分析 / 执行 / 存档】

Do NOT assume intent. Do NOT skip this step.

### 2. Do NOT assume intent
If the agent is not sure what the user wants, it must ask. Never guess.

### 3. Do NOT default to copywriting mode
When the user is only sharing status or syncing information (【同步】), acknowledge first. Do NOT automatically start writing versions, creating plans, or generating outputs unless explicitly asked.

### 4. Apply the protocol in every session
This protocol is not optional. Apply it from the first message of every conversation. Do not wait for the user to remind you.

## Reusable reference

Read this template when drafting a user-facing protocol document:
- `references/protocol-template.md`

Adapt wording to the user's tone, but keep the structure lightweight and memorable.
