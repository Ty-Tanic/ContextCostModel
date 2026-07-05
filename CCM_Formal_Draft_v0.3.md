# Context Cost Model (CCM) --- Formal Draft v0.3

# Variables

  Symbol     Meaning
  ---------- ------------------------------------------------------
  HCC        Human Context Capability
  CRC        Context Reconstruction Cost
  CMC        Context Maintenance Cost
  CSC        Context Switching Cost
  ACC(a,p)   Artifact Context Cost of artifact *a* for person *p*
  C(T)       Context required for task *T*
  O(T1,T2)   Context overlap between two tasks
  AI         AI assistance factor

------------------------------------------------------------------------

# Total Context Cost

\[ TCC = CRC + CMC + CSC \]

------------------------------------------------------------------------

# Context Reconstruction

For a task requiring artifacts A:

\[ CRC(T,p)=`\sum`{=tex}\_{a`\in `{=tex}A} ACC(a,p) \]

Generalized:

\[ CRC=f(documentation, architecture, experience, tooling, AI) \]

------------------------------------------------------------------------

# Human Feasibility

A task is completely representable only if

\[ C(T)`\le `{=tex}HCC \]

Otherwise

\[ C(T)\>HCC \]

implies that the required context exceeds simultaneous human processing
capability.

------------------------------------------------------------------------

# AI Assistance

Effective capability:

\[ HCC\_{eff}=HCC+`\Delta`{=tex}\_{AI} \]

Alternative formulation:

\[ CRC\_{AI}=CRC`\cdot`{=tex}(1-`\alpha`{=tex}) \]

where

\[ 0`\le`{=tex}`\alpha`{=tex}`\le1`{=tex} \]

------------------------------------------------------------------------

# Context Switching

\[ CSC(T_1,T_2)=
`\beta`{=tex}`\left`{=tex}(C(T_1)+C(T_2)-O(T_1,T_2)`\right`{=tex}) \]

where

-   β = switching penalty
-   O = reusable context overlap

------------------------------------------------------------------------

# Context Maintenance

\[ CMC=`\gamma`{=tex}`\cdot `{=tex}C(T) \]

where γ models cognitive maintenance effort.

------------------------------------------------------------------------

# Productivity

Hypothesis:

\[ Productivity `\propto`{=tex} `\frac{Delivered\ Value}`{=tex}
{CRC+CMC+CSC} \]

------------------------------------------------------------------------

# Architectural Quality

\[ Architecture Quality `\propto`{=tex} `\frac{1}`{=tex}
{Expected Context Cost} \]

------------------------------------------------------------------------

# Research Directions

Potential future concepts:

-   Context entropy
-   Context compression
-   Context bandwidth
-   Context latency
-   Context graph theory
-   Team context capacity
-   Organizational context economics

------------------------------------------------------------------------

# Central Thesis

Most software engineering techniques---including modularization,
abstraction, documentation, bounded contexts, APIs, and AI
assistance---can be interpreted as mechanisms for minimizing total
context cost.
