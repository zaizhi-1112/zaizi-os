---
name: message-idempotency-and-retry-guard
description: Reduce duplicate replies, partial resend behavior, and retry-related response glitches in long-running OpenClaw conversations. Use when an assistant sometimes sends the same reply twice, sends a broken half-reply followed by a full one, or needs protection rules around model switching, gateway restarts, and unstable messaging windows.
---

# Message Idempotency and Retry Guard

Use this skill to reduce a frustrating class of failure in real-world chat systems:
- duplicate full replies
- half replies followed by a second full reply
- repeated responses after model switching or gateway restarts
- unnecessary token burn caused by retry behavior

This skill is about **防重复回复** and **重试保护**.

## Core goal

Help the assistant behave more safely and economically when the message pipeline is unstable.

The target behavior is:
- fewer duplicate replies
- shorter replies during risky windows
- clearer handling after retries or restarts
- less waste of user attention and token budget

## When this skill matters most

Apply stronger protection when any of these are true:
- the model was just switched
- the gateway was just restarted
- the session looks freshly resumed
- the user reports duplicate or broken replies
- the platform shows signs of resend or delivery instability

## Main causes to watch for

Common causes include:
1. message delivery retry
2. gateway restart during reply generation
3. model switch during or near a response
4. partial stream delivery followed by retry
5. weak one-message-one-reply protection in unstable windows

## Guard workflow

### 1. Recognize the risky window
Treat these as high-risk moments:
- immediately after model switching
- immediately after gateway restart
- immediately after connection recovery
- after the user reports duplicate replies

### 2. Enter short-reply protection mode
In a risky window, do not start with a long answer unless necessary.

Preferred behavior:
- reply with a short confirmation first
- avoid long multi-section answers right away
- avoid split, streaming-style verbose replies if a retry seems likely

Good examples:
- `收到，已切换。`
- `当前模型已更新。`
- `我先短回确认，等链路稳定再展开。`

### 3. Avoid duplicate expansion
If the assistant suspects the previous reply may have been duplicated or partially delivered:
- do not fully restate the same long answer immediately
- prefer a short clarification like:
  - `刚才那条如果重复了，以这条为准。`
  - `上一条链路可能抖了，我先短确认。`

### 4. Prefer one stable final answer over two unstable ones
When unstable, compress.
A short correct reply is better than two long overlapping replies.

### 5. Preserve user trust
A duplicate reply is not just a cosmetic issue. It creates:
- confusion
- extra reading cost
- potential extra token cost
- reduced confidence in the assistant

Treat it as a real quality issue.

## Integration with model switching

When the user changes models, the assistant must assume the next reply window is fragile.

### Required rule
After a model switch or gateway restart, enter **short-reply protection mode** for the next response or two.

That means:
- acknowledge first
- keep it short
- avoid long analytical replies until stability is clearer

## Suggested response patterns

### After model switch
- `已切换。`
- `当前模型已更新。`
- `我先短回确认，避免切换窗口重复回复。`

### After duplicate-reply complaint
- `你说得对，刚才那条像是重发了。后面我会先走短回复保护。`
- `刚才链路可能抖了，我先短回，别再重复烧字。`

## What to document

When this issue appears in a real collaboration, it is worth recording:
- what triggered the duplicate-reply window
- whether a model switch or gateway restart happened nearby
- whether short-reply protection helped

## References

Read as needed:
- `references/retry-patterns.md` — common duplicate-reply patterns
- `references/short-reply-protection.md` — practical short-reply protection rules
