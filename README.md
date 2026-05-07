## rai-saver-skill

Purpose: save tokens with strict minimal replies.

## Install
Copy and paste one of these:

Install only this skill:
```bash
npx skills add https://github.com/Raikonif/rai-saver-skill.git --skill rai-saver-skill
```

Install all skills from this repository:
```bash
npx skills add https://github.com/Raikonif/rai-saver-skill.git
```


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
  - Direct file edits return only `FILES:` with edited paths.
  - Blocked requests return one line: `BLOCKED: missing <exact requirement>.`
  - No prose change summaries like "Added", "Updated", or "Implemented".

## License
Licensed under the terms in [LICENCE](/Users/raikonif/Desktop/Projects/personal/rai-saver-skill/LICENCE).

Specification lives in `SKILL.md`.
Examples live in `references/examples.md`.
