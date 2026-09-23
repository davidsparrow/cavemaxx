**You already have the app builder. Turn it up.**

CaveMaxx is a free, tiny Claude Skill that changes how readily Claude answers with something you can look at or use (a diagram, a calculator, a comparison matrix, a dashboard, a mini-app) instead of another wall of text.

## Install

- **Claude.ai**: Settings → Skills → upload `cavemaxx.skill` (or the zip).
- **Claude Code**: unzip and move the `cavemaxx` folder into `~/.claude/skills/`, or `git clone https://github.com/davidsparrow/cavemaxx ~/.claude/skills/cavemaxx`.
- **Claude Code plugin**: `/plugin marketplace add davidsparrow/cavemaxx` then `/plugin install cavemaxx@cavemaxx`.

Then type `/cave-max`. Full details in [INSTALL.md](https://github.com/davidsparrow/cavemaxx/blob/main/INSTALL.md).

## What's in V1

- Three modes: `/cave-off`, `/cave-default`, `/cave-max`, plus plain-language equivalents.
- A text / visual / interactive / mini-app decision framework, and a one-line "Diagram · Interactive Surface · Skip" question for the genuinely ambiguous cases.
- Building rules: replace prose rather than duplicate it, useful on open, mobile-friendly, simple controls, self-contained, correct.
- To-do and question blocks at the end of replies, one per item, only when real.
- Reusable-interface and privacy rules: interface separated from today's data, private state by default.
- Examples for pricing, comparison, diagram and reusable data, a benchmark prompt set, and one real generated pricing simulator.

Both attached files have identical contents; `.skill` is the extension Claude.ai shows for skills.
