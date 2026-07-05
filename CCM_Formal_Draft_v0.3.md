# Context Cost Model (CCM) --- Formal Draft v0.3

## Variables

| Symbol | Meaning |
| --- | --- |
| HCC | Human Context Capability |
| CRC | Context Reconstruction Cost |
| CMC | Context Maintenance Cost |
| CSC | Context Switching Cost |
| ACC(a,p) | Artifact Context Cost of artifact *a* for person *p* |
| C(T) | Context required for task *T* |
| O(T1,T2) | Context overlap between two tasks |
| AI | AI assistance factor |

------------------------------------------------------------------------

## Total Context Cost

$$
TCC = CRC + CMC + CSC
$$

------------------------------------------------------------------------

## Context Reconstruction

For a task requiring artifacts $A$:

$$
CRC(T,p)=\sum_{a\in A} ACC(a,p)
$$

Generalized:

$$
CRC=f(documentation, architecture, experience, tooling, AI)
$$

------------------------------------------------------------------------

## Human Feasibility

A task is completely representable only if

$$
C(T) \le HCC
$$

Otherwise

$$
C(T) > HCC
$$

implies that the required context exceeds simultaneous human processing
capability.

------------------------------------------------------------------------

## AI Assistance

Effective capability:

$$
HCC_{eff}=HCC+\Delta_{AI}
$$

Alternative:

$$
CRC_{AI}=CRC\cdot(1-\alpha)
$$

where

$$
0\le\alpha\le1
$$

------------------------------------------------------------------------

## Context Switching

$$
CSC(T_1,T_2)=\beta\left(C(T_1)+C(T_2)-O(T_1,T_2)\right)
$$

where:

-   $\beta$ = switching penalty
-   $O$ = reusable context overlap

------------------------------------------------------------------------

## Context Maintenance

$$
CMC=\gamma\cdot C(T)
$$

where $\gamma$ models cognitive maintenance effort.

------------------------------------------------------------------------

## Productivity

Hypothesis:

$$
Productivity \propto
\frac{Delivered\ Value}{CRC+CMC+CSC}
$$

------------------------------------------------------------------------

## Architectural Quality

$$
Architecture\ Quality \propto
\frac{1}{Expected\ Context\ Cost}
$$

------------------------------------------------------------------------

## Research Directions

-   Context entropy
-   Context compression
-   Context bandwidth
-   Context latency
-   Context graph theory
-   Team context capacity
-   Organizational context economics

------------------------------------------------------------------------

## Central Thesis

Most software engineering techniques---including modularization,
abstraction, documentation, bounded contexts, APIs, and AI
assistance---can be interpreted as mechanisms for minimizing total
context cost.
