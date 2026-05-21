# restore-hyper-wellness-voice

The Claude skill that auto-writes copy in Restore Hyper Wellness's voice. Installed as either a project-level or global Claude Code skill (see top-level SETUP.md for the install wizard).

## What's in this folder

```
restore-hyper-wellness-voice/
├── SKILL.md                  ← always-loaded directive (the voice rules)
├── README.md                 ← you are here
└── references/               ← loaded on demand
    ├── channels.md           ← per-channel detailed rules
    ├── editing.md            ← 10-pass editing protocol
    ├── examples.md           ← calibration pairs (before → Restore)
    └── vocabulary.md         ← forbidden/preferred terms, therapy claims, brand stats
```

## How the skill loads

Claude reads `SKILL.md` whenever a prompt mentions Restore Hyper Wellness in a writing context. The minimal `SKILL.md` (~120 lines) carries the always-on rules: voice attributes, non-negotiables, channel cheat-sheet, generation protocol, and a routing block.

The four `references/*.md` files are loaded on demand based on the routing block. Loading on demand keeps every trigger lightweight — the agent only pulls the depth it needs.

## Install

Don't install this folder directly. Run the wizard at `../../SETUP.md` instead — it handles location, file copies and a verification test.

If you must install manually:

```bash
# Project-level (inside an Obsidian vault)
cp -r restore-hyper-wellness-voice/ <vault>/.claude/skills/

# Global (every Claude Code session)
cp -r restore-hyper-wellness-voice/ ~/.claude/skills/
```

Confirm the path ends in `restore-hyper-wellness-voice/SKILL.md` — a common error is double-nesting (`restore-hyper-wellness-voice/restore-hyper-wellness-voice/SKILL.md`).

## Verify

In a new Claude Code session:

> "Write a Restore Hyper Wellness Instagram caption announcing the new Wonder Juice IV Drip."

If the skill loaded correctly:
- Opens with a benefit, not the brand name
- Uses "may help to..." for every claim
- No Oxford commas (drops the comma before final "and" in lists)
- Caps "IV Drip", "Drips", "Members", "Cryotherapy" etc.
- Maximum 1 exclamation point
- Em dashes have no surrounding spaces

If the output uses "customers" or "products" or includes "!!" or stacks Oxford commas, the skill didn't load. Re-install.

## Versioning

`SKILL.md` carries the skill's version in frontmatter. Bump on every meaningful change:
- Patch (1.0.0 → 1.0.1): typo fix, single rule tightening
- Minor (1.0.0 → 1.1.0): new vocab term, new channel, new dead pattern
- Major (1.0.0 → 2.0.0): breaking voice change (rare)

Run `git pull` in the parent repo to get updates. Then re-run the install wizard's "update" prompt at the bottom of SETUP.md.
