
---

# docs/concepts.md

```md
# xAIML – Core Concepts

This document explains the fundamental concepts behind xAIML.

---

## Node

A Node represents a UI element that is meaningful from a human perspective.

Examples:
- Page
- Modal
- Section
- Tab
- View

A node is not a technical component and is not tied to any framework.

---

## Hierarchy

Hierarchy is defined exclusively through:
- `parent`
- `children`

Depth is never stored.

Hierarchy is data. Depth is a view concern.

---

## Type (UX Role)

The `type` field describes the perceived UX role of a node.

- It does not imply hierarchy
- It does not imply behavior
- It does not imply navigation

Types are semantic, not technical.

---

## State (`stateLabel`)

States describe visible UI conditions.

Examples:
- empty
- loading
- with-data
- success

States are descriptive only and carry no logic.

---

## Transitions (`leadsTo`)

Transitions describe what a human knows can happen next.

A transition is valid only if a human can visually explain a before/after situation.

No conditions.
No inference.

---

## UX Semantic Fields

xAIML supports optional semantic fields:

- `purpose`
- `userGoal`
- `userActionExpected`
- `blockingReason`
- `nextVisibleOutcome`

These fields capture human-perceived intent and context.

A human should be able to fill them by simply looking at the screen.
