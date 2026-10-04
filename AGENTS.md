# Quest Log data repo

This repo holds [Quest Log](https://tasks.patrick-mckinley.com) data: plain JSON under `data/`.
There's no app code here.

AI assistants: before reading or changing anything, load the Quest Log skill and follow it.

- Skill: https://tasks.patrick-mckinley.com/skills/quest-log/SKILL.md
- Helper script: https://tasks.patrick-mckinley.com/skills/quest-log/scripts/quest.py
- Schemas: https://tasks.patrick-mckinley.com/schema/

Validate the whole tree (`python3 quest.py validate .`) before you commit. Never edit `stats` on
a level: the app maintains it.
