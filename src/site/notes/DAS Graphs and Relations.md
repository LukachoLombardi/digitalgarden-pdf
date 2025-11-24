---
{"dg-publish":true,"permalink":"/das-graphs-and-relations/"}
---

# Binary Relations
> [!SUMMARY] 
> $R\subseteq A \times B$ is a binary relation (with R being a Set).
> $A,B,.../A_1,...,A_n$ are called **features**

The Reason why R is a subset of the Cartesian product, is that it doesn't *have* to provide all possible connections between elements of A and B, but simply any valid subset of these connections.
# Graphs and directed graphs
> [!SUMMARY] 
> $R \subseteq A \times B$ with $B=A$ Is a directed graph. ($R \subseteq A \times A$)
> Elements of $A$ are the vertices (points), while elements of $R$ are the edges (connections).

# Composition on Relations
> [!SUMMARY] 
> Let $R ⊆ A × B$ and $S ⊆ B × C$. The composition is defined by $S ◦ R = \{(a, c) ∈ A × C | ∃b ∈ B ((a, b) ∈ R ∧ (b, c) ∈ S)\}$.

# Identity
> [!SUMMARY]
> Theorem. Let $IdB = {(b, b) ∈ B × B}$. For all $R ⊆ A × B$, we have $IdB ◦ R = R$ and $R ◦ IdA = R$. 
> (For Understanding: $(b,b)$ already implies that both members of the pair are the same)

# Relation properties

![[Lecture_4.pdf#page=55&rect=-16,416,973,647|Lecture_4, p.14-1]]

# "Inverses" (It's called a transpose dumbass)
Since relations aren't functions, there's no guarantee that a *single* $b$ or $(a,b)$ is found by looking for an edge pointing from a vertice a  $a$ in a relation $R \subseteq A \times B$. The other way around, this is also the case. However, we can compute the so called **transpose**, which is really just the original relation in reverse:
$$
S^T=\{(b,a) \in B \times A:(a,b) \in S\}
$$
(Assuming some $S \subseteq A \times B$).

If our relation is "bijective" (meaning $\forall \{(b,a),(b',a')\} \in S^T \times S^T: b=b' \Rightarrow a=a'$, or in english: $S^T$'s edges contain each vertice exactly **once**), this is actually an inverse. *If an inverse exists, the transpose **is** the inverse.* Have fun with this information.

# Closure Operations
> [!SUMMARY] 
> Closures are the smallest possible superset-relations of original relations, that satisfy specific properties.

Take 
$$
S = \{(1,2),(1,3)\}
$$
The symmetric closure for $S$ would be 
$$
S' = \{(1,2), (2,1), (1,3), (3,1)\}
$$
Note that the closure isn't the *modification* that needs to be applied, but the *result* of said modification.

![[Lecture_4.pdf#page=69&rect=-2,18,1169,595|Lecture_4, p.15-5]]

There's formal notation for computing these, but I don't think that's relevant right now.

TODO: Add content from missed lecture (17.11.25)