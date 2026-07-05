# Context Cost Model (CCM) --- Formal Draft v0.3

## Variables

| Symbol | Meaning |
| --- | --- |
| HCC | Human Context Capability |
| CRC | Context Reconstruction Cost |
| CMC | Context Maintenance Cost |
| CSC | Context Switching Cost |
| ACC(a,p) | Artifact Context Cost of artifact *a* for person *p* |
| CR(T) | Context Requirement of task *T* |
| O(T1,T2) | Context overlap between two tasks |
| O(A) | Reusable context overlap among artifacts in set *A* |
| IC(T) | Integration context cost between artifacts required for task *T* |
| E(T,p) | Externalized context available to person *p* for task *T* |
| E_AI(T,p) | AI-provided externalized context available to person *p* for task *T* |
| V_AI(T,p) | AI verification and supervision cost for task *T* by person *p* |
| AI | AI assistance factor |
| α | Fraction of CRC reduced by AI assistance |
| β | Context switching penalty coefficient |
| γ | Baseline context maintenance effort coefficient |
| δ | Overload cost coefficient |

------------------------------------------------------------------------

## Total Context Cost

$$
TCC = CRC + CMC + CSC
$$

------------------------------------------------------------------------

## Context Reconstruction

For a task requiring artifacts $A$:

$$
CRC(T,p)=\sum_{a\in A} ACC(a,p) - O(A) + IC(T)
$$

where $O(A)$ is reusable context overlap among required artifacts.

Generalized:

$$
CRC=f(documentation, architecture, experience, tooling, AI)
$$

------------------------------------------------------------------------

## Human Feasibility

A task is directly manageable with available externalized context only if

$$
CR(T) \le HCC + E(T,p)
$$

Otherwise

$$
CR(T) > HCC + E(T,p)
$$

implies that the required context exceeds the person's simultaneous
processing capability plus available externalized context.

------------------------------------------------------------------------

## AI Assistance

Effective capability:

$$
HCC_{eff}=HCC+E_{AI}(T,p)
$$

Alternative:

$$
CRC_{AI}=CRC\cdot(1-\alpha)+V_{AI}(T,p)
$$

where

$$
0\le\alpha\le1
$$

$E_{AI}$ represents AI-provided externalized context, not a literal
increase in human working memory.

------------------------------------------------------------------------

## Context Switching

$$
CSC(T_1,T_2)=\beta\left(CR(T_1)+CR(T_2)-O(T_1,T_2)\right)
$$

where:

-   $\beta$ = switching penalty
-   $O$ = reusable context overlap

------------------------------------------------------------------------

## Context Maintenance

$$
CMC=\gamma\cdot CR(T)+\delta\cdot \max(0,CR(T)-HCC-E(T,p))
$$

where $\gamma$ models baseline cognitive maintenance effort and $\delta$
models overload cost when required context exceeds available capability.

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
Context\ Managing\ Architectural\ Quality \propto
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

Many software engineering techniques---including modularization,
abstraction, documentation, bounded contexts, APIs, and AI
assistance---can be interpreted as mechanisms for minimizing total
context cost.
