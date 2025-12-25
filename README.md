# xAIML

**xAIML (eXtended AI Markup Language)** is a declarative language designed to provide AI assistants with explicit UI context, as perceived by a human user in a modern application.

xAIML is not an AI system, not a framework, and not a navigation engine.  
It is a **context support format**.

---

## Problem Statement

In modern web applications (SPA, PWA, dynamic apps):

- there is no universal equivalent to HTML `<meta>` for UI context
- AI assistants do not know:
  - which screen the user is on
  - the visible UI state
  - the UI hierarchy
  - the recommended user path
- automatic approaches (DOM scanning, routes, heuristics) are:
  - fragile
  - project-specific
  - hard to maintain

---

## The xAIML Approach

**The human is the source of truth.**

xAIML relies on explicit, manual, declarative descriptions of:

- screens and views
- UI hierarchy
- visible states
- perceived transitions

No inference.  
No logic.  
No automation.

---

## What xAIML Does

- describes meaningful UI elements
- captures visible UI states
- declares explicit transitions
- provides structured context for AI assistants

## What xAIML Does Not Do

- no code or DOM scanning
- no business logic
- no rules engine
- no prompt generation
- no automatic reasoning

## Core Principle

xAIML describes what a human knows about the UI, not what a system could guess.

---

## Minimal Example

```json
{
  "xaiml_version": "1.0",
  "app": "Example App",
  "nodes": [
    {
      "id": "home",
      "title": "Home",
      "type": "Page",
      "purpose": "Entry point of the application",
      "userGoal": "Start using the app"
    }
  ]
}
---
