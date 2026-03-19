# Protocol Pattern

Use this pattern to reduce ambiguity before it becomes memory drift.

## Default labels

- 【同步】 status sharing, no output required by default
- 【快答】 short answer first
- 【分析】 reasoning, comparison, diagnosis, reflection
- 【执行】 direct output or task completion
- 【存档】 save durable information

## Mandatory fallback

When the user sends an unlabeled message and intent is not obvious, ask:

> 这条你要我按哪种处理？【同步 / 快答 / 分析 / 执行 / 存档】

## Protocol rules

1. Do not assume intent when unclear.
2. Do not default to copywriting mode during status-sharing.
3. Keep labels lightweight and memorable.
4. Use the protocol to reduce friction, not to over-mechanize the relationship.

## Why this matters

A good protocol lowers:
- misfires
- repeated clarification loops
- accidental overproduction
- context bloat from unnecessary branching
