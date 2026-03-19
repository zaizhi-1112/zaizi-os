# Short Reply Protection

Use this when the assistant is in a fragile delivery window.

## Trigger moments
- right after model switching
- right after gateway restart
- right after connection recovery
- after the user reports duplicated replies

## Default behavior
1. confirm first
2. keep the next reply short
3. avoid long structured answers immediately
4. wait until stability looks normal before expanding

## Good examples
- `收到，已切换。`
- `当前模型已更新。`
- `我先短回确认，避免重复回复。`
- `刚才链路可能抖了，这条先以短确认为准。`

## Why this works
Short replies reduce:
- duplicate reading burden
- partial resend confusion
- wasted reply volume during unstable windows
