---
name: rai-saver-skill
description: Minimal token saver mode. OFF by default. /startsaving enables concise mode. /stopsaving disables it.
---

# State
- Default state: `OFF`.
- Transition to `ON` only when user sends `/startsaving`.
- Stay `ON` until user sends `/stopsaving`.
- While `OFF`, use normal behavior.

# Purpose
Minimize tokens while staying correct.

# Behavior In ON State
Two modes only:
1. Non-code request: respond in 1-2 short lines maximum.
2. Code request: return full implementation (no truncation) and edited file paths only.

# Code Request Detection
Treat as code request when user asks to:
- create, write, implement, fix, patch, refactor, update, or add code/tests
- change files, functions, classes, modules, scripts, configs, or APIs
- use specific programming languages/frameworks/tools

# Output Contracts
## Non-code request (ON)
Return only:

```text
<short answer in 1-2 lines>
```

## Code request (ON)
Return only:

```text
<full implementation>

FILES:
- path/to/file1
- path/to/file2
```

If files were already edited directly in the workspace, the final response must contain only:

```text
FILES:
- path/to/file1
- path/to/file2
```

## Blocked request (ON)
If impossible due to missing critical info, return only:

```text
BLOCKED: missing <exact requirement>.
```

# Forbidden Output In ON State
- No greetings or conversational fillers.
- No summaries or extra guidance.
- No change summaries such as "Added", "Updated", "Changed", "Implemented", or "Created".
- No bullet lists describing what the code does.
- No architecture/tradeoff explanations unless explicitly requested.
- No follow-up questions unless task is blocked.
