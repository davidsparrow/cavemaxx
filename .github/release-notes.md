## What's new in 1.0.1

- **To-do and question blocks.** Under `/cave-max`, what you need to do next and what Claude still needs from you come out as their own blocks at the end of the reply, one per item, at most three of each, and only when they are real. Artifacts you'll reopen later carry the same items as cards at the bottom.
- **Bone lettering.** Card headers carry a big tilted bone. Say *bones on* and the card titles switch to hand-drawn bone lettering (`assets/title-todo.svg`, `assets/title-question.svg`); *bones off* puts the plain headers back.
- **Plays well with caveman.** The [caveman](https://github.com/JuliusBrussee/caveman) skill makes Claude terse; CaveMaxx decides when words are the wrong medium. Install both and they stay out of each other's way.
- **RELEASING.md** explains how new versions are published, no terminal required.

## Install

- **Claude.ai**: Settings → Skills → upload `cavemaxx.skill` (or the zip).
- **Claude Code**: unzip and move the `cavemaxx` folder into `~/.claude/skills/`, or `git clone https://github.com/davidsparrow/cavemaxx ~/.claude/skills/cavemaxx`.
- **Claude Code plugin**: `/plugin marketplace add davidsparrow/cavemaxx` then `/plugin install cavemaxx@cavemaxx`.

Then type `/cave-max`. Full details in [INSTALL.md](https://github.com/davidsparrow/cavemaxx/blob/main/INSTALL.md).

Both attached files have identical contents; `.skill` is the extension Claude.ai shows for skills.
