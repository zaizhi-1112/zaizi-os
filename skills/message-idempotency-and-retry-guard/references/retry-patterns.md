# Retry Patterns

Use this reference to recognize common duplicate-reply situations.

## Pattern 1 — Full reply repeated twice
Likely caused by message retry or uncertain delivery acknowledgement.

## Pattern 2 — Partial reply, then full reply
Likely caused by stream interruption followed by rerun.

## Pattern 3 — Duplicate reply after model switch
Likely caused by unstable window during configuration reload or gateway restart.

## Pattern 4 — Duplicate reply after gateway restart
Likely caused by the old run and the new run both attempting to answer.

## Practical rule
If a recent model switch, gateway restart, or reconnect happened, assume reply duplication risk is elevated.
