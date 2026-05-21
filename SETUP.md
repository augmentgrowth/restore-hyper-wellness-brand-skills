# Setup

This package installs into your Claude Code + Obsidian setup in one paste. The prompt below is a setup wizard — Claude Code will ask you a couple of questions and put every file in the right place. You don't have to know any commands.

**Prerequisite:** Claude Code installed. If you don't have it: https://claude.com/claude-code

## How to install

1. Open Claude Code in this folder (the one you just cloned from GitHub).
2. Paste the entire prompt below into the chat.
3. Answer Claude's two questions when it asks.

```
You are running a setup wizard for the Restore Hyper Wellness Brand Skills package. The
current working directory contains the package files. Walk me through the
install step by step. Wait for my answers before moving on.

## What this package contains

- 01_Brand_Voice/Restore_Brand_Voice_Guide.md  — canonical voice guide
- 01_Brand_Voice/Restore_Brand_Voice_Guide.pdf — same, printable
- 01_Brand_Voice/restore-hyper-wellness-voice/                       — installable Claude skill
- 01_Brand_Voice/restore-hyper-wellness-voice.zip                    — zipped version of the skill
- 02_Design_System/design.md                                 — design tokens (colors, type)
- 02_Design_System/design.pdf                                — same, printable
- 03_Demos/Restore_Brand_In_Action.pdf         — 4 demos of voice + design
- 03_Demos/brand_showcase.html                               — live design system mockup
- 03_Demos/welcome_email.html                                — live email mockup

## Step 1 — Find my Obsidian vault

Ask me: "What's the full path to your Obsidian vault?" Give an example like
/Users/yourname/Documents/MyVault. If I don't use Obsidian, ask if I want to
put the docs somewhere else (default to ~/Documents/Restore Hyper Wellness Brand System/).

Verify the path exists. If it doesn't, ask me to correct it.

## Step 2 — Skill install location

Ask me: "Where do you want the restore-hyper-wellness-voice skill installed?" with two
options:

  A. Project-level (default) — inside my Obsidian vault at
     <vault>/.claude/skills/restore-hyper-wellness-voice/. The skill only fires when
     I'm working inside the vault. Good if I mostly write Restore Hyper Wellness copy
     while inside Obsidian.

  B. Global — at ~/.claude/skills/restore-hyper-wellness-voice/. The skill fires in
     every Claude Code session anywhere on this Mac. Good if I draft
     Restore Hyper Wellness copy in lots of different folders (codebases, side
     projects, scratch directories).

Tell me the default is A (project-level) because it keeps client work
scoped. Wait for my answer.

## Step 3 — Find my resources folder

Tell me you're going to put the brand guide, design tokens and demos
in my Obsidian vault's "resources" area (the place for reference
material I read but don't actively work on).

Look inside my vault for a folder that matches a resources pattern:
- "03_Resources" / "03_resources"
- "Resources" / "resources"
- "PARA/Resources"
- "References" / "references"

If you find one, tell me what you found and ask me to confirm. If you
don't find one, ask me what my resources folder is called or whether
to create "Resources/" at the vault root.

Inside the chosen resources folder, create a subfolder called
"Restore Hyper Wellness Brand System/" with the same internal structure (01_Brand_Voice,
02_Design_System, 03_Demos).

## Step 4 — Install

Once you have my answers for both location questions, do the following:

A. Copy the skill folder from this package's 01_Brand_Voice/restore-hyper-wellness-voice/
   into either <vault>/.claude/skills/ or ~/.claude/skills/ depending on
   my answer. Confirm the skill's SKILL.md ends up at the expected path.

B. Copy 01_Brand_Voice/Restore_Brand_Voice_Guide.md and .pdf into
   <resources>/Restore Hyper Wellness Brand System/01_Brand_Voice/.

C. Copy 02_Design_System/design.md and design.pdf into
   <resources>/Restore Hyper Wellness Brand System/02_Design_System/.

D. Copy 03_Demos/ (all three files) into
   <resources>/Restore Hyper Wellness Brand System/03_Demos/.

Create folders as needed. Use absolute paths. After each copy, ls the
target to confirm.

## Step 5 — Verify the skill

Tell me the skill is installed and we're going to test it. Run this prompt
yourself, in the same session, to verify the skill auto-fires:

   "Write a Restore Hyper Wellness Instagram caption announcing our new IV Drip 'Wonder Juice' — designed for athletic recovery clients."

If the skill loaded correctly, you'll write a caption that opens with a benefit (not "Restore"), uses "may help to..." for any claim, drops Oxford commas, capitalizes "IV Drip" and "Clients", and stays under 1 exclamation point.

Show me the output and tell me whether the skill fired.

## Step 6 — Summary

Print a short summary in this format:

   Installed:
   - Skill: <path>/restore-hyper-wellness-voice/  (version 1.0.0)
   - Docs:  <resources>/Restore Hyper Wellness Brand System/
   - Total files copied: <N>

   To use the skill: just mention "Restore Hyper Wellness" in any writing prompt — it
   auto-fires. Try "Write a Restore Hyper Wellness [channel] post about [topic]."

   To use the design tokens: tag the file in a prompt with @
   (in this vault, that's @<resources>/Restore Hyper Wellness Brand System/02_Design_System/design.md).

Then we're done.
```

## What to expect

The wizard will ask you two questions, run a few file copies and a verification test. Total install time: about 1 minute.

If anything goes sideways, tell Claude what happened — it can usually self-correct or back out.

## Updating later

When Restore Hyper Wellness's voice or design system evolves, you'll get a notification (or grab the latest by running `git pull` in this folder). To roll the updates into your installed skill:

```
The Restore Hyper Wellness Brand Skills package has been updated. Re-install everything:

1. Copy the restore-hyper-wellness-voice/ folder from 01_Brand_Voice/ to wherever
   the previous version is installed (either inside my Obsidian vault's
   .claude/skills/ or ~/.claude/skills/). Overwrite the old version.

2. Re-copy the markdown, PDFs and demos from this package into the
   "Restore Hyper Wellness Brand System/" folder in my resources area. Overwrite
   anything that's there.

3. Read 01_Brand_Voice/restore-hyper-wellness-voice/SKILL.md and tell me the new
   version number plus a one-line summary of what changed.
```

## Uninstall

```
Remove the restore-hyper-wellness-voice skill installed at either
<my Obsidian vault>/.claude/skills/restore-hyper-wellness-voice/ or
~/.claude/skills/restore-hyper-wellness-voice/ — whichever exists. Also remove the
"Restore Hyper Wellness Brand System/" folder from my vault's resources area.
Confirm with ls before and after.
```

## Trouble?

- **"Claude doesn't know what Restore Hyper Wellness sounds like"** — the skill didn't load. Run the install wizard again and watch for errors.
- **"The skill installs but the output still sounds generic"** — check that the path to SKILL.md ends in `restore-hyper-wellness-voice/SKILL.md`, not `restore-hyper-wellness-voice/restore-hyper-wellness-voice/SKILL.md` (a common double-nest from re-extracting the zip).
- **Anything else** — reach out to Malachi at Augment Growth.
