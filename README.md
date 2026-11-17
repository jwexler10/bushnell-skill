# Bushnell

**Immediate value for a newcomer. Meaningful depth on the hundredth use.**

An agent skill for progressive disclosure, drill-down interactions, layered visualizations, and products that reward repeated use.

## What it does

- States the first-encounter reward and the hundredth-use reward separately.
- Maps meaningful follow-up questions onto a disclosure ladder.
- Preserves context, accessible interactions, and a clear route back.
- Checks the behavior an interface creates, as well as the capabilities it exposes.

Depth means richer understanding and useful action. Extra controls, hidden essentials, and artificial unlocks do not supply it.

## Install

This repository contains a portable, instruction-only agent skill. No API key,
MCP server, executable script, or companion skill is required. Tools are useful
when your task needs current information or inspection of an existing project.

1. Download this repository with **Code → Download ZIP**, or clone it:

   ```bash
   git clone https://github.com/jwexler10/bushnell-skill.git
   ```

2. For a Codex project, copy the entire `skills/bushnell` folder into the target
   project's `.agents/skills/` directory. The result should be:

   ```text
   your-project/
     .agents/
       skills/
         bushnell/
           SKILL.md
   ```

   Keep any supporting files inside that folder when copying. For user-wide local
   Codex discovery, use `~/.agents/skills/bushnell/` instead. Choose one scope to avoid
   installing duplicate copies.

3. In Codex, invoke the skill with `$bushnell` followed by your task, or let the
   agent select it when your task matches the description. If it does not appear,
   restart Codex. See the [official skills guide](https://learn.chatgpt.com/docs/build-skills).

For another agent that supports `SKILL.md`, use that agent's documented skills
directory. You can also explicitly ask an agent to read and apply
[`skills/bushnell/SKILL.md`](skills/bushnell/SKILL.md). Discovery and invocation syntax
depend on the host.

## Try it

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

## Repository contents

- [`skills/bushnell/SKILL.md`](skills/bushnell/SKILL.md): the complete skill.
- [`LICENSE`](LICENSE): MIT license for these instructions and documentation.

Copyright © 2026 Jason Wexler.
