# xAIML Builder – User Guide

This guide explains how to use the xAIML Builder.

---

## Purpose of the Builder

The Builder is:
- a declarative editor
- a pedagogical tool
- a visual support for humans

It is not:
- an automatic generator
- a rules engine
- an intelligent system

---

## Recommended Workflow

### 1. Create or Load a Project

- New project
- Import existing xAIML
- Load example dataset

---

### 2. Define Nodes

For each node:
- choose a clear title
- select a UX type
- attach to a parent if applicable

Think in screens, not components.

---

### 3. Add UX Context

Fill semantic fields when relevant:
- purpose
- userGoal
- userActionExpected
- blockingReason
- nextVisibleOutcome

These fields are optional but highly recommended.

---

### 4. Declare Transitions

Use `leadsTo` only when the transition is visually certain.

---

### 5. Define Workflows

Workflows should be:
- simple
- readable
- non-exhaustive

They describe recommendations, not rules.

---

## Best Practices

- Favor clarity over completeness
- Avoid implicit logic
- Do not mirror business rules
- Keep descriptions human-readable
