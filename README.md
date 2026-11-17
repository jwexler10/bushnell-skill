# Bushnell

**Immediate value for a newcomer. Meaningful depth on the hundredth use.**

An agent skill for progressive disclosure, drill-down interactions, layered visualizations, and products that reward repeated use.

## Install in one command

```bash
npx skills add jwexler10/bushnell-skill
```

Choose Claude Code, Cursor, Codex, or another supported agent in the installer.
Requires [Node.js](https://nodejs.org/) 22.20 or later. Installs to the current project
by default; add `--global` for a user-wide installation. See the
[skills CLI](https://github.com/vercel-labs/skills) for supported agents and options.

For a noninteractive installation to Claude Code, Cursor, and Codex together:

```bash
npx skills add jwexler10/bushnell-skill --skill bushnell --agent claude-code cursor codex --yes
```

Prefer a graphical install? Use the Claude marketplace option below.

## What it does

- States the first-encounter reward and the hundredth-use reward separately.
- Maps meaningful follow-up questions onto a disclosure ladder.
- Preserves context, accessible interactions, and a clear route back.
- Checks the behavior an interface creates, as well as the capabilities it exposes.

Depth means richer understanding and useful action. Extra controls, hidden essentials, and artificial unlocks do not supply it.

## Before vs. after

**Example request:** “Turn an analytics dashboard with twenty charts into something useful for beginners and experts.”

| Aspect | Without the skill: illustrative pitfall | With Bushnell: intended behavior |
|---|---|---|
| First encounter | Puts every chart on the page and adds collapsible sections. | Gives the initial surface one recognizable result and an obvious next action. |
| Repeated use | Adds more settings and panels as the advanced experience. | Reveals greater precision, relationships, and supporting evidence through meaningful questions. |
| Navigation | Replaces the overview whenever a detail opens. | Preserves context and state, with a clear route back at each layer. |

These are illustrative comparisons, not recorded model outputs or benchmark results.
Actual results depend on the model, the prompt, and the evidence you provide.

## Install as a Claude plugin

This repository is both a standalone skill and a single-plugin marketplace. The
plugin and the skills CLI install the same `SKILL.md`; choose one route per host
to avoid duplicate installations.

### Claude and Cowork: no terminal

1. Open **Plugins** (or **Customize → Plugins**, depending on your version).
2. Choose **Add → Add marketplace → Add from a repository**.
3. Enter `jwexler10/bushnell-skill` or `https://github.com/jwexler10/bushnell-skill`.
4. Select **Bushnell** and add the plugin. Find its skill through `/` or the
   skill picker; when namespaced commands are shown, use `/bushnell:bushnell`.

Availability and organization controls depend on your Claude plan and account.
See [Anthropic's plugin installation guide](https://support.claude.com/en/articles/13837440-use-plugins-in-claude).

### Claude Code: marketplace commands

Run these inside Claude Code:

```text
/plugin marketplace add jwexler10/bushnell-skill
/plugin install bushnell@jwexler10-bushnell
```

Then invoke `/bushnell:bushnell` followed by your task. The marketplace is defined in
[`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json), and the plugin
in [`.claude-plugin/plugin.json`](.claude-plugin/plugin.json).

### Manual installation

Download the repository using **Code → Download ZIP**, or clone it:

```bash
git clone https://github.com/jwexler10/bushnell-skill.git
```

Copy the entire `skills/bushnell` folder, including any supporting files, into the
appropriate directory in your target project:

| Agent | Project skill directory | Invocation |
|---|---|---|
| Claude Code, direct skill | `.claude/skills/bushnell/` | `/bushnell` |
| Codex | `.agents/skills/bushnell/` | `$bushnell` |
| Cursor | `.cursor/skills/bushnell/` | Ask the agent to use Bushnell. |

Each destination must contain `SKILL.md` directly. Other hosts may use different
discovery or invocation rules; follow their documentation. See the
[Codex skills guide](https://learn.chatgpt.com/docs/build-skills).

This is an instruction-only skill: no API key, MCP server, companion skill, or
executable script is required. Tools are useful when your actual task needs live
information or inspection of an existing project.

## Try it

The prompts below use Codex's `$bushnell` syntax. In Claude Code, use `/bushnell` for a
direct skills installation or `/bushnell:bushnell` for a marketplace plugin. In Cursor,
ask the agent to use Bushnell and give it the same task.


```text
$bushnell Design a project dashboard that helps a newcomer immediately and still supports deep investigation after months of use.
```

```text
$bushnell Review this chart-to-group-to-item drill-down. Where does the user lose context, and how should the route back work?
```

```text
$bushnell Our analytics page has twenty charts and many collapsible sections. Design a useful first layer and meaningful depth.
```

Expect two explicit rewards, a discovery path, a content split, and an interaction contract covering context and recovery.

## Adapt it

Supply your actual objective, constraints, evidence, and priorities. Edit the skill
to fit your workflow. It assumes no particular product, repository structure,
technology stack, or internal decision log. Applying a thinking skill does not
itself authorize changes, purchases, deployments, or other external actions.

## Related skills

Each skill works independently. Choose the workflow that matches your question:

| Skill | Use it to |
|---|---|
| [Aristotle](https://github.com/jwexler10/aristotle-skill) | Challenge assumptions and reason from first principles. |
| [Apple](https://github.com/jwexler10/apple-skill) | Work backward from the user experience to the technology. |
| [Syndesy](https://github.com/jwexler10/syndesy-skill) | Compare alternatives fairly and commit to a defensible choice. |
| [Evgenii](https://github.com/jwexler10/evgenii-skill) | Evaluate economic outcomes, incentives, and uncertainty. |

Read the practical guide: [Five reusable workflows for better product and engineering decisions](https://github.com/jwexler10/aristotle-skill/blob/main/docs/five-decision-workflows.md).
It includes a worked decision, installation steps, and the limits of the current validation.

## Repository contents

- [`.claude-plugin/plugin.json`](.claude-plugin/plugin.json): Claude plugin metadata.
- [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json): installable marketplace catalog.
- [`skills/bushnell/SKILL.md`](skills/bushnell/SKILL.md): the complete skill.
- [`LICENSE`](LICENSE): MIT license for these instructions and documentation.

Copyright © 2026 Jason Wexler.
