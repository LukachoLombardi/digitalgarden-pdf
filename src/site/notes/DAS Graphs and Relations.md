---
{"dg-publish":true,"permalink":"/das-graphs-and-relations/"}
---

# Binary Relations
> [!SUMMARY] 
> $R\subseteq A \times B$ is a binary relation (with R being a Set).
> $A,B,.../A_1,...,A_n$ are called **features**

The Reason why R is a subset of the Cartesian product, is that it doesn't *have* to provide all possible connections between elements of A and B, but simply any valid subset of these connections.x
# Graphs and directed graphs
> [!SUMMARY] 
> $R \subseteq A \times B$ with $B=A$ Is a directed graph. ($R \subseteq A \times B$)
> Elements of $A$ are the vertices (points), while elements of $R$ are the edges (connections).

# Composition on Relations
> [!SUMMARY] 
> Let $R ⊆ A × B$ and $S ⊆ B × C$. The composition is defined by $S ◦ R = \{(a, c) ∈ A × C | ∃b ∈ B ((a, b) ∈ R ∧ (b, c) ∈ S)\}$.

# Identity
> [!SUMMARY]
> Theorem. Let $IdB = {(b, b) ∈ B × B}$. For all $R ⊆ A × B$, we have $IdB ◦ R = R$ and $R ◦ IdA = R$. 
> (For Understanding: $(b,b)$ means that both members of the pair are the same)

TODO: Add notes about inverses and relation properties