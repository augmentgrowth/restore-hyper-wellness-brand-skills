# Restore Hyper Wellness Brand Skills

Restore Hyper Wellness's brand voice + design system, packaged for Claude (and any other AI tool you use). Built by Augment Growth.

**Package version:** 1.0.0  •  **Brand voice skill:** 1.0.0  •  **Design system:** 1.0  •  **Updated:** 2026-05-20

---

## Quick start

1. **Clone this repo** to your Mac:
   ```bash
   git clone https://github.com/augmentgrowth/restore-hyper-wellness-brand-skills.git
   cd restore-hyper-wellness-brand-skills
   ```
   (If `git` is unfamiliar — open Terminal, paste the two lines above, hit Enter twice.)

2. **Run the install wizard.** Open Claude Code inside the cloned folder and follow [SETUP.md](SETUP.md). One paste. Takes about a minute.

3. **Test it.** In any new Claude Code session, type:
   > *"Write a Restore Hyper Wellness Instagram caption announcing our new studio opening with a Founding Member rate."*

   If the skill installed correctly, the response will sound unmistakably Restore Hyper Wellness.

---

## What's in here

```
restore-hyper-wellness-brand-skills/
├── README.md                                  ← you are here
├── SETUP.md                                   ← interactive install wizard
├── LICENSE                                    ← usage terms
├── 01_Brand_Voice/
│   ├── Restore_Brand_Voice_Guide.md     ← master voice doc
│   ├── Restore_Brand_Voice_Guide.pdf    ← same content, printable
│   ├── restore-hyper-wellness-voice/                          ← installable Claude skill (folder)
│   └── restore-hyper-wellness-voice.zip                       ← installable Claude skill (zip)
├── 02_Design_System/
│   ├── design.md                              ← design tokens (colors, type, spacing)
│   └── design.pdf                             ← printable version
└── 03_Demos/
    ├── Restore_Brand_In_Action.pdf     ← 4 demos of voice + design in use
    ├── brand_showcase.html                    ← open in browser: live design system
    └── welcome_email.html                     ← open in browser: live email mockup
```

---

## Pick your path

### "I want to read the voice guide myself."
Open **`01_Brand_Voice/Restore_Brand_Voice_Guide.pdf`**. Self-contained reference — voice attributes, do/don't tables, channel rules, worked examples, common scenario templates.

Use this when onboarding a new team member, briefing an agency or freelancer, or sitting down to write copy yourself.

### "I want Claude to write copy in our voice."
Follow [SETUP.md](SETUP.md) — that's the install wizard for the **restore-hyper-wellness-voice** skill.

Once installed, the skill auto-fires anytime you mention Restore Hyper Wellness in a writing prompt. Try:

> *"Write a Restore Hyper Wellness Instagram caption for our new IV Drip menu refresh."*
> *"A Client emails — 'I'm intimidated to try Cryotherapy for the first time.' Write a Studio Manager reply."*
> *"Write a Facebook post for our new Boulder studio opening on September 5. Founding Member rate $99/mo."*

The skill works the same way in Claude Code, Claude.ai, Cowork, and (with a manual paste) ChatGPT or Gemini.

### "I want our design tokens (colors, typography, spacing)."
Open **`02_Design_System/design.md`** — machine-readable YAML with the full color palette, typography scale and component patterns. The PDF version is at `02_Design_System/design.pdf`.

To get Claude to actually use it, drop the file into your prompt with `@`. In Claude Code you type `@` and a file picker appears — find `design.md` and select it. Examples:

```
Build me a landing page hero section using the brand colors and typography
from @design.md. Headline: "Fuel Your Body. Feel the Results."
```

```
I'm building a welcome email — reference @design.md and design three
CTA button variants in our primary color.
```

```
Generate a Tailwind CSS config from @design.md so my developer can use our
brand tokens directly.
```

**What's happening under the hood:** when you @ a file, Claude reads its full contents into context. For `design.md`, that's exact hex codes (`#055577` for primary), font families, spacing values. Claude uses those as authoritative values instead of guessing.

### "I just want to see what this can do."
Open **`03_Demos/Restore_Brand_In_Action.pdf`**. Four demos generated in single prompts.

For the live mockups: double-click **`03_Demos/brand_showcase.html`** or **`03_Demos/welcome_email.html`** — they open in your browser, no install needed.

---

## Skill vs `@design.md` — when to use which

These two assets do different jobs. Quick rule:

- **Use the restore-hyper-wellness-voice skill when you're writing copy** — captions, ad text, emails, blog posts, website headlines, scripts. Anything where voice, tone and word choice matter. The skill auto-fires whenever you mention Restore Hyper Wellness in a writing prompt.
- **Use `@design.md` when you're building something visual** — websites, email templates, mockups, Tailwind configs, slide decks, social graphics. Anything that needs exact brand colors, fonts or spacing values.

You can use both at once. Example: *"Write a Restore Hyper Wellness welcome email, then design the HTML using @design.md."*

---

## Keeping up to date

This repo is versioned. To pull the latest changes:

```bash
cd path/to/restore-hyper-wellness-brand-skills
git pull
```

Then re-run the update prompt at the bottom of [SETUP.md](SETUP.md) to refresh your installed skill and resources copies.

**Versioning convention:**
- Each release of the package is tagged in git (`v1.0.0`, `v1.0.1`, etc.). To roll back: `git checkout v1.0.0`.
- The brand voice skill carries its own internal version (`SKILL.md` frontmatter). The design system carries its own internal version (`design.md` frontmatter).
- Material changes ship as a new git tag with a note in the commit message.

---

## Editing the voice or design system

You have admin access to this repo and can invite your own team. To make changes:

1. Pull the latest (`git pull`).
2. Open Claude Code inside the cloned folder and paste the prompt below. Fill in the placeholder.

```
I want to make the following changes to the Restore Hyper Wellness brand voice guide
and/or design system:

[DESCRIBE YOUR EDITS HERE — be specific. Examples:
 - Change the "Words we don't use" list: add "X", remove "Y"
 - Update a stat
 - Add a new section on email subject lines with 3 examples in our voice
 - Change the primary color from #055577 to a new hex
 - Add a new sub-brand palette for an upcoming product line]

Please:
1. Edit 01_Brand_Voice/Restore_Brand_Voice_Guide.md and/or
   02_Design_System/design.md to apply the changes.
2. If the voice guide changed: re-sync the restore-hyper-wellness-voice skill so SKILL.md
   and references/ all reflect the same edits. Bump SKILL.md version field.
3. Re-zip the skill (`zip -r restore-hyper-wellness-voice.zip restore-hyper-wellness-voice/`
   from inside 01_Brand_Voice/).
4. Re-render the affected PDFs from the updated markdown (optional — skip
   if you want markdown-only for now).
5. Bump the version in the frontmatter of any file I edited.

Summarize what you changed when you're done.
```

3. Commit and push your changes:

```bash
git add .
git commit -m "Voice: <one-line summary of changes>"
git push
```

4. (Optional but recommended) Cut a new version tag if it's a material release:

```bash
git tag -a v1.1.0 -m "<one-line description>"
git push --tags
```

If you want Augment Growth to maintain this for you instead, reach out.

---

## Questions?

This package is yours to share internally with anyone at Restore Hyper Wellness who needs it. If anything is unclear or contradicts existing brand assets, reach out to Malachi at Augment Growth (malachi@augmentgrowth.ai).

---

*Restore does not provide medical services. We do not accept insurance. Individual results may vary.*
