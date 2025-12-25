# xAIML v1.0 — Official Specification

## 1. Introduction

xAIML (eXtended AI Markup Language) is a declarative language designed to provide AI assistants with explicit UI context, as perceived by a human user in a modern application.

xAIML is not an intelligent system.  
It does not infer, compute, or interpret behavior.

Its sole purpose is to expose human-visible UI context in a stable, explicit form.

---

## 2. Scope and Principles

xAIML is based on the following principles:

- The human is the source of truth
- No inference or deduction
- No business logic
- No automation
- No dependency on frameworks or code

xAIML describes what is visible and understandable to a human, nothing more.

---

## 3. Root Document

A xAIML document MUST have the following structure:

```json
{
  "xaiml_version": "1.0",
  "app": "string",
  "nodes": [],
  "workflows": [],
  "meta": {}
}
```
---

## 4. Node
A Node represents a UI element that is meaningful from a human perspective.

```
Node {
  id: string
  title: string
  type: NodeType

  parent?: string
  children?: string[]

  stateLabel?: string
  leadsTo?: string[]

  purpose?: string
  userGoal?: string
  userActionExpected?: string
  blockingReason?: string
  nextVisibleOutcome?: string

  meta?: object
}

```
All fields are declarative.
No field implies logic or behavior.

--- 

## 5. Hierarchy
Hierarchy is defined exclusively by:

- parent
- children

Depth MUST NOT be stored.

Hierarchy is data. Depth is a view concern.

--- 

## 6. Type (UX Role)
The type field describes the perceived UX role of a node.

It does not define:
- hierarchy
- behavior
- navigation

Allowed Types (alphabetical order)
- Accordion
- Action
- Breadcrumb
- Carousel
- Confirmation
- Drawer
- Group
- Help
- Modal
- Onboarding
- Overlay
- Page
- Panel
- Section
- Sheet
- Stepper
- Tab
- Tooltip
- View
- Wizard


--- 

## 7. State (stateLabel)
stateLabel describes a visible UI state.

- Optional
-Textual
- Descriptive only

Recommended values (non-exhaustive):
- blocked
- empty
- error
- initial
- loading
- partial
- readonly
- success
- with-data

--- 

## 8. Transitions (leadsTo)
leadsTo declares an explicit, certain transition.
- No conditions
- No probabilities
- No inference

If a human can visually explain a before/after situation, the transition is valid.

--- 

## 9. UX Semantic Fields
The following optional fields capture immediate human understanding:

- purpose
- userGoal
- userActionExpected
- blockingReason
- nextVisibleOutcome

A human should be able to fill these fields by simply looking at the screen.

--- 

## 10. Workflows
Workflows declare recommended user paths.

They are:
- Explicit
- Non-exhaustive
- Non-calculated
- Non-binding

--- 

## 11. Forbidden Concepts
xAIML v1.0 MUST NOT include:

- tags
- uiDepthHint
- business rules
- conditions
- permissions
- logic
- prompts
- DOM annotations
- automatic analysis

--- 

## 12. Final Principle
xAIML describes what a human knows about the UI, not what a system could guess.
