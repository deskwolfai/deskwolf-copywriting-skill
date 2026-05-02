# DeskWolf Copywriting Skill

The skill DeskWolf uses with Claude Code to write sales copy that converts and doesn't sound AI-generated.

It's a `SKILL.md` plus a master rulebook (`copywriting_guidelines.md`) and a reference library — a system prompt Claude auto-invokes whenever you ask it to write a landing page, sales letter, ad, cold email, VSL, pricing page, or any other piece of revenue copy. It enforces direct one-reader voice, kills the AI cadence tells, and applies the proven Hormozi + Brunson framework stack underneath.

## What you get

- **Single source of truth for voice and anti-slop** — five voice attributes with gut-check questions, hard banned phrases, antithetical-construction zero-tolerance, restricted-word quotas, higher-order anti-pattern detection (overpromising, victim framing, feature laundry, corporate formality).
- **Direct address by default** — every piece speaks to ONE reader. No group address, no infomercial register, no lecture register.
- **Proven framework backbone** — Hormozi's Value Equation, Grand Slam Offer, Money Models + Brunson's Perfect Webinar, Epiphany Bridge, Soap Opera Sequence, Big Domino, Attractive Character, Traffic Temperature.
- **20+ named output templates** — landing pages, offer stacks, pricing pages, VSL scripts, cold emails, welcome sequences, ad copy, lead magnets, application pages, upsells, downsells, order bumps, retention emails. Each pre-mapped to the right framework combo.
- **Named headline formulas** — Outcome-First, Positioning Statement, Problem-Solution, Category Education, Direct Command. Pull from the catalog when stuck.
- **CTA library split** by intent class (primary conversion vs. secondary content consumption) with rules for action-verb-not-question construction.
- **Pricing language rules** — never lead with price, no apology language, no "starting at," anchor against value first.
- **Competitor handling policy** — no competitors named in public copy, scripts for redirecting comparison questions.
- **4-pass quality gate** — banned-phrase scan, specificity score, voice authenticity, reader value test. Run before every delivery.
- **Platform-specific tone direction** — website, LinkedIn, cold outreach, email nurture, advertising, newsletter, Threads/X, YouTube, Instagram/Facebook.

## Install (per team member)

Skills live in your personal Claude home directory. Clone this repo into the skills folder and Claude picks it up automatically — no config, no restart.

### macOS / Linux

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/deskwolfai/deskwolf-copywriting-skill.git ~/.claude/skills/sales-copywriter
```

### Windows (PowerShell)

```powershell
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.claude\skills" | Out-Null
git clone https://github.com/deskwolfai/deskwolf-copywriting-skill.git "$env:USERPROFILE\.claude\skills\sales-copywriter"
```

The folder name **must** be `sales-copywriter` — that's how the skill registers its trigger.

## Verify it's loaded

Open Claude Code in any project and ask:

> Write me a hero section for a local business AI receptionist — cold traffic, $997/mo offer.

Claude should auto-invoke `sales-copywriter`, ask about the offer specifics if needed, then return copy that follows Value Equation + Big Domino structure, addresses one reader directly, and runs clean against the anti-slop list.

## Repo layout

```
deskwolf-copywriting-skill/
├── README.md                       # This file
├── SKILL.md                        # The skill prompt — what Claude loads
├── copywriting_guidelines.md       # Master rulebook (voice, structure, anti-slop, quality)
└── references/
    ├── frameworks.md               # Full Hormozi + Brunson framework details
    └── output-templates.md         # Structural templates per output type
```

## How the skill operates

1. **Identify the output type** — maps the request to one of 20+ templates (landing page, cold email, VSL, etc.) and pulls the framework combo
2. **Assess traffic temperature** — hot/warm/cold determines whether story can be skipped
3. **Position on the value ladder** — tunes tone and length to price tier ($0 to $100K+)
4. **Load context** — pulls the master `copywriting_guidelines.md`, the framework reference, the output template, and any project-specific brand context
5. **Write** — applies the template using the frameworks
6. **Run quality gates** — framework compliance → persuasion architecture → anti-slop → voice direction → five voice attributes → conversion hygiene → brand check

## Updating the rules

The master file is `copywriting_guidelines.md`. When you find a phrase that should be banned, an anti-pattern that's slipping through, or a positive lexicon term that's worth canonizing, update that file directly and commit. Every piece of DeskWolf copy (and every client deliverable) inherits from this one document.

## Source pedigree

The frameworks are distilled from licensed, purchased works:
- Alex Hormozi — *$100M Offers*, *$100M Leads*, *$100M Money Models*
- Russell Brunson — *Expert Secrets*, *DotCom Secrets*

Plus DeskWolf operational learnings post-2026-04-30 — voice attributes, antithetical-construction ban, direct-address rule, higher-order anti-patterns. The skill produces original copy applying these principles. It does not reproduce, quote, or redistribute the source material.

## License

Internal DeskWolf tool. Not for redistribution.
