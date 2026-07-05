
# AGENTS.md

# Context Cost Model (CCM)

## Mission

This repository develops the **Context Cost Model (CCM)**, a formal theory for
describing, analyzing and ultimately quantifying the cost of context in software
engineering and other knowledge-intensive activities.

The long-term objective is a mathematically rigorous, empirically testable model.

---

# Central Thesis

The dominant cost of many engineering tasks is not writing code but acquiring,
reconstructing, maintaining and integrating the context required to perform the
task correctly.

Software architecture can therefore be viewed primarily as **context
management**.

---

# Scope

CCM currently focuses on:

- Software architecture
- Software development
- Knowledge work
- Team organization
- AI-assisted engineering

The model should remain sufficiently general to apply to additional domains.

---

# Scientific Principles

Always distinguish between:

1. Definition
2. Observation
3. Hypothesis
4. Conjecture
5. Theorem
6. Empirical Result

Do not present hypotheses as established facts.

Do not invent evidence.

---

# Canonical Definitions

## Context

All information required to perform a task correctly.

## Context Requirement (CR)

The amount of context required by a task.

## Context Cost

The effort required to acquire, reconstruct, maintain or transfer context.

## Context Reconstruction Cost (CRC)

Effort required to reconstruct the context necessary for a task.

## Context Maintenance Cost (CMC)

Effort required to keep the required context active while performing a task.

## Context Switching Cost (CSC)

Cost incurred when changing from one context to another.

## Human Context Capability (HCC)

Maximum amount of context that a human can reliably maintain simultaneously.

## Artifact Context Cost (ACC)

Cost for a particular person to reconstruct the context represented by a
specific artifact.

## Context Overlap

Reusable context shared between multiple artifacts.

## Integration Cost (IC)

Additional effort required to combine individually understood artifacts into one
coherent mental model.

---

# Canonical Equations

## Total Context Cost

TCC = CRC + CMC + CSC

## Context Reconstruction

CRC(T,p) = Σ ACC(a,p) − O(A) + IC(T)

where

- T = task
- p = person
- A = required artifacts
- O(A) = reusable context overlap
- IC(T) = integration cost

General dependency:

CRC = f(documentation, architecture, experience, tooling, AI)

---

# Working Hypotheses

- Better modularization reduces context cost.
- Documentation primarily reduces reconstruction cost.
- Architecture is primarily context management.
- Experience reduces reconstruction cost rather than eliminating it.
- AI primarily functions as an external context processor.
- Many software engineering practices can be interpreted as minimizing context
  cost.

---

# Mathematical Guidelines

- Prefer explicit notation.
- Every symbol must be defined.
- Introduce equations incrementally.
- Build hierarchical models instead of isolated formulas.
- Separate measurable variables from latent variables.
- Minimize redundant notation.

---

# Writing Style

- Use precise scientific English.
- Avoid marketing language.
- Avoid unnecessary adjectives.
- Prefer short definitions.
- Distinguish assumptions from conclusions.
- State limitations explicitly.

---

# Repository Conventions

Suggested structure:

README.md
AGENTS.md
paper.md
definitions.md
notation.md
mathematics.md
examples.md
experiments.md
references.bib

---

# Agent Instructions

When modifying this repository:

- Preserve terminology unless a strong justification exists.
- Do not redefine canonical symbols without updating all references.
- Keep equations internally consistent.
- Explain proposed changes before replacing existing mathematics.
- Prefer extending existing concepts over introducing new terminology.
- Avoid duplicate concepts with different names.
- Ensure examples are consistent with definitions.
- Never fabricate references or empirical validation.
- Mark speculative ideas as hypotheses.
- Favor formalism over prose where practical.

---

# Open Research Topics

- Formal definition of Context.
- Units for measuring context.
- Context graphs.
- Context entropy.
- Context compression.
- Context bandwidth.
- Context latency.
- Organizational context economics.
- Experimental validation.
- Relationship to cognitive load theory.
- Relationship to information theory.
- Relationship to software architecture metrics.

---

# Long-Term Goal

Develop CCM into a rigorous, falsifiable and practically useful theory capable
of explaining and predicting engineering effort through the explicit modelling
of context.
