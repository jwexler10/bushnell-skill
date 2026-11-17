---
name: bushnell
description: Design progressive disclosure that gives beginners immediate value and experienced users meaningful depth. Use for drill-downs, layered visualizations, navigation, dashboards, and repeated-use experiences; evaluate both the first encounter and the hundredth use.
license: MIT
---

# Bushnell — Immediate Value, Lasting Depth

Apply the design principle commonly called Bushnell's Law: easy to learn, difficult
to master. For a product, this means **understood in seconds, rewarding across
repeated use**. Mastery should grow from richer understanding, not from deciphering
the interface.

Use this skill to design how depth unfolds. Settle the feature's purpose and basic
usability first. No companion skill, component library, or repository layout is
required.

## Define both rewards

**First-encounter reward:** what a new user understands or gains in the first few
seconds, before learning controls or exploring details. A chart might make a trend
visible immediately; a creation tool might provide a useful starting result.

**Hundredth-use reward:** what remains meaningful after familiarity. Useful sources
include greater precision, new relationships among familiar objects, evidence behind
a claim, expressive combinations, and changes in the user's own data or work.

Do not offer the same summary twice at different sizes. The deeper layer must answer
a new question or support a new action.

## Build a disclosure ladder

The initial surface answers the common question. An explicit, discoverable action
opens a less common question. Choose the split around the user's needs, not around
how the backend stores data.

| Layer | Suitable content | Design obligation |
|---|---|---|
| Initial surface | Main result, primary visualization, essential status | Communicate value without exploratory interaction. |
| Precision on demand | Exact values, definitions, comparisons | Support pointer, keyboard, and touch access as appropriate; avoid hover-only essentials. |
| Investigation | Members, examples, related objects, editable details | Make the trigger and its result predictable. |
| Evidence or method | Sources, calculations, uncertainty, limitations | Keep it available and understandable without overwhelming the main task. |
| Internal machinery | Implementation-only scores and identifiers | Expose only if they help the user's task, with meaningful labels. |

These are roles, not mandated widgets. Collapsing a section does not itself create
depth; it helps only when the initial content is useful and the revealed content
answers a meaningful follow-up question.

## Apply the principle recursively

A feature several layers deep still needs an understandable entry point and a
reason to explore. For example:

```text
overview -> select a group -> inspect a member -> inspect supporting evidence
```

Each transition should add understanding while preserving orientation. More curiosity
may be required; more interface literacy should not be.

Depth comes from meaningful relationships between a few understandable elements,
not from the number of panels, controls, or invented terms. A diagram's visual
grammar must not imply a relationship, such as causation, that the evidence cannot
support.

## Make the interaction contract explicit

- **Resolve competing gestures.** Define what selection, dragging, background clicks,
  search, and navigation do when they coexist. Avoid accidental activation.
- **Preserve context.** A deeper layer should retain the parent or offer an obvious
  way back with relevant state intact. Use adjacent panels, breadcrumbs, a stack,
  or another pattern appropriate to the device and task.
- **Answer the question that was asked.** Selecting an item within a group should
  explain that item in that context. Offer its broader history as a separate path.
- **Reuse established containers.** Add a new subject to an existing detail pattern
  before introducing another navigation system.
- **Reveal deliberately.** Avoid permanent callouts that dominate the surface to
  answer an uncommon question.
- **Fold honestly.** Indicate omitted counts or scope. Expanding a list should not
  silently change the meaning or scale of the information already shown.
- **Make recovery visible.** Provide close, back, reset, or undo when relevant.
  Preserve deliberate user adjustments unless they choose to reset them.

Adapt the exact layout and gestures to accessibility needs and available space.
A desktop arrangement is not a requirement for a small screen.

## Design the behavior the system creates

Ask what people will do, not only what the feature permits:

| Capability | Behavior to check |
|---|---|
| Clickable data points | Purposeful investigation rather than aimless panel opening. |
| Search | Orientation rather than unwanted navigation or state changes. |
| Drag, pan, and zoom | A clearer view with a reliable route back. |
| Multiple detail layers | Accumulating understanding while retaining context. |
| Customization | Useful control without making configuration a prerequisite. |
| Deep navigation | Confidence that the user can return without losing their work. |

When actual use contradicts the intended behavior, revise the design. Recovery and
continuity are conditions that make exploration possible.

## Make unfamiliar ideas legible

Name the referent rather than an internal unit: prefer "1.4 times your usual weekly
total" over an unexplained score. Keep an adjective connected to the quantity and
comparison that support it. Define unfamiliar terms where they are needed.

State when evidence is thin. Do not fill a gap with an unsupported conclusion.
Optional generated explanation should not block an otherwise useful result; required
work must still communicate progress, failure, and recovery honestly.

## Workflow

1. Locate the feature in the user's overall journey. Identify who encounters it and
   what they already know. Inspect the existing product or code when available.
2. Write its first-encounter reward and hundredth-use reward, one sentence each.
3. Map the primary action, the question it opens, and the next useful step.
4. Assign content to the disclosure ladder. Remove duplicate summaries and controls
   that add learning without adding value.
5. Specify context preservation, gesture priority, accessible access, and recovery.
6. Use established implementation patterns when implementation is requested.
7. Review once as a newcomer and once as a returning user. Check the behavior as
   well as whether the controls technically work.

For an overview, favor immediate value and a clear route to richer material. For a
mid-depth feature, organize around the user's questions. For evidence beneath a
claim, prioritize provenance, scope, uncertainty, and the path back.

## Avoid

- A surface that says nothing until it is operated.
- Hiding essential functionality or accessibility behind discovery.
- Adding controls, charts, or settings and calling the result depth.
- Requiring internal terminology to understand ordinary results.
- Replacing the parent so thoroughly that the user loses the question they asked.
- Treating badges, streaks, or artificial unlocks as substitutes for meaningful value.
- Enforcing product-specific limits or layouts without checking the current context.

In the handoff, name the two rewards and the discovery path. Scale the explanation
to the task, and support claims about the current product with actual observations
or code references.
