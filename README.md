## rai-compact-saver

Purpose: save tokens with strict minimal replies.

## Install
1. Copy this folder into your local skills directory.
2. Ensure `SKILL.md` remains at the skill root.
3. Reload/restart your Codex session so the skill is discovered.

## Includes
- `SKILL.md`: behavior contract and output rules.
- `references/examples.md`: minimal ON-state output examples.
- `LICENCE`: project license text.

## Commands
- `/startsaving`: enable saver mode (`ON`).
- `/stopsaving`: disable saver mode (`OFF`).

## Behavior Summary
- Default state is `OFF`.
- In `ON`:
  - Non-code requests return 1-2 short lines.
  - Code requests return full implementation plus edited file paths.
  - Blocked requests return one line: `BLOCKED: missing <exact requirement>.`

## License
Licensed under the terms in [LICENCE](/Users/raikonif/Desktop/Projects/personal/rai-saver-skill/LICENCE).

Specification lives in `SKILL.md`.
Examples live in `references/examples.md`.
