# Consuming xAIML

This guide explains how to read and use a xAIML file correctly.

---

## Fundamental Rule

xAIML only describes what is explicitly declared.  
Nothing must be inferred, calculated, or assumed.

---

## Reading Order

### 1. Root Document

Check:
- `xaiml_version`
- `app`

Ensure compatibility before processing.

---

### 2. Nodes and Hierarchy

Rebuild hierarchy exclusively using:
- `parent`
- `children`

No other field should influence structure.

---

### 3. Types

The `type` field indicates perceived UX role only.

It does not imply behavior or navigation.

---

### 4. States

`stateLabel` describes visible UI conditions.

States must never be interpreted as rules.

---

### 5. Semantic Fields

Semantic UX fields are the primary value of xAIML.

They explain:
- why a screen exists
- what the user wants
- what is visibly expected
- what happens next

---

### 6. Transitions

`leadsTo` describes explicit, certain transitions only.

If a transition is not declared, it must not be assumed.

---

### 7. Workflows

Workflows represent recommended paths.

They are:
- non-exhaustive
- non-calculated
- non-binding

---

## Common Mistakes

- Inferring navigation
- Treating states as logic
- Completing missing information
- Optimizing user paths

xAIML is intentionally incomplete.

