# My quests

A starter repo for [Quest Log](https://tasks.patrick-mckinley.com), the project tracker you play
as a retro platformer. Your projects, worlds and levels live here as plain JSON, so you own every
bit of it and get full history for free.

## Get started

1. **Use this template** (the green button at the top of the repo page) → **Create a new
   repository**. Make it private if you like; Quest Log works either way.
2. Open **https://tasks.patrick-mckinley.com** and connect your new repo: follow **Get started**,
   or paste the repo name and a fine-grained token with *Contents: read and write* for it under
   ⚙ Settings. (*Sign in with GitHub* is on its way and will make this one click.)
3. Press **New game** and start your first project.

That's it. Every tick, step and level you add is saved as a small commit in `data/`.

## What's in here

```
data/
  settings.json                 repo-wide settings (optional; choose a default hero here)
  automation.json               what the Quest Log workflow does (managed in the app)
  <project>/project.json        one folder per project, appears once you make one
  <project>/<world>/world.json
  <project>/<world>/<level>.json
.github/workflows/quest.yml     the Quest Log workflow (written by the app, don't edit it)
AGENTS.md                       points AI assistants at the Quest Log skill
```

The format is documented at
[tasks.patrick-mckinley.com/schema](https://tasks.patrick-mckinley.com/schema/), and every file
names its schema in `$schema`, so most editors autocomplete it.

## Working with an AI assistant

Want help planning? Point Claude, ChatGPT or another assistant at this repo and the
[Quest Log skill](https://tasks.patrick-mckinley.com/skills/quest-log/SKILL.md). It knows the
format, validates its own changes and can open a pull request for you to review. `AGENTS.md` tells
assistants that read repo instructions where to find it.

## Automation

`.github/workflows/quest.yml` runs the Quest Log action. Out of the box it validates `data/` on
every push and pull request; on a pull request it also comments with what the change adds,
changes and removes, so an accidental deletion stands out. Notifications are off, so the workflow
has no schedule and uses no Actions minutes between changes.

Manage it from ⚙ Settings → **Automation** in the app, which keeps the workflow in step with
`data/automation.json`. Don't edit the workflow by hand; the app rewrites it. You can delete it if
you don't want it; the app doesn't need it.
