# Context Cost Model (CCM)

## Abstract

The **Context Cost Model (CCM)** is a conceptual framework that models
software engineering and other knowledge work as a process dominated by
the acquisition, reconstruction, maintenance, and transfer of context.

The central thesis is:

> The dominant cost of many engineering tasks is not writing code, but
> reconstructing and maintaining the required context.

------------------------------------------------------------------------

# Core Concepts

## Context

The complete information required to perform a task correctly.

Examples include:

-   business rules
-   architecture
-   APIs
-   source code
-   documentation
-   operational knowledge
-   historical design decisions

------------------------------------------------------------------------

## Context Reconstruction Cost (CRC)

The effort required to reconstruct a context after it has been lost or
was never acquired.

CRC is affected by:

-   documentation quality
-   architecture
-   tooling
-   developer experience
-   AI assistance

------------------------------------------------------------------------

## Context Maintenance Cost (CMC)

The effort required to keep an active context available while solving a
task.

Large systems increase CMC because more information must remain
simultaneously active.

------------------------------------------------------------------------

## Context Switching Cost (CSC)

The cost incurred when switching between two unrelated contexts.

Includes:

-   unloading previous context
-   reconstructing the new context
-   interruption overhead

------------------------------------------------------------------------

## Human Context Capability (HCC)

The maximum amount of context a person can reliably process
simultaneously.

HCC varies between individuals and depends on:

-   experience
-   expertise
-   cognitive ability
-   fatigue
-   tooling

------------------------------------------------------------------------

## Artifact Context Cost (ACC)

The reconstruction cost of a specific artifact such as:

-   source file
-   service
-   API
-   database schema
-   document

ACC is person-dependent.

------------------------------------------------------------------------

# Core Observations

1.  Architecture primarily manages context.
2.  Modularization reduces required context.
3.  Documentation reduces CRC.
4.  Experienced developers often have lower CRC rather than simply more
    knowledge.
5.  Large organizations frequently fail because context becomes too
    expensive to manage.
6.  Many software engineering practices can be interpreted as strategies
    to reduce context costs.

------------------------------------------------------------------------

# AI

AI functions as an **external context processor**.

It can:

-   reconstruct context
-   summarize large systems
-   answer architectural questions
-   reduce CRC
-   effectively extend usable human context

AI does not replace human intent or decision making.

------------------------------------------------------------------------

# Testable Predictions

-   Better modularization reduces CRC.
-   Better documentation reduces onboarding time.
-   Interruptions increase CSC and reduce productivity.
-   AI-assisted development reduces reconstruction time.
-   Teams with lower context overlap scale more efficiently.

------------------------------------------------------------------------

# Possible Future Formalization

For a task:

    Total Context Cost = CRC + CMC + CSC

Potential extensions:

-   Context entropy
-   Context overlap
-   Context compression
-   Context latency
-   Context bandwidth

------------------------------------------------------------------------

# Motivation

CCM attempts to provide a unified explanation for many established
software engineering principles by treating **context** as the primary
optimization variable rather than code volume or complexity alone.

------------------------------------------------------------------------

# Personal Origin

CCM was derived from observing a personal workflow pattern: for some
workers, the limiting factor is not execution speed, but **Context
Reconstruction Cost**.

Once the relevant context is reconstructed, implementation may be
comparatively fast. The dominant cost is often recovering the artifacts,
constraints, prior decisions, and mental model required to act correctly.

This makes context cost person-dependent. The same task can have very
different cost depending on prior exposure, notes, tooling, fatigue,
interruptions, and available externalized context.
