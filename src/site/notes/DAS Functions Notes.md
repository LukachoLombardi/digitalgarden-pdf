---
{"dg-publish":true,"permalink":"/das-functions-notes/"}
---

# Definition
**Informally**: a function from A to B is a recipe to transform an element of A into an element of B

> [!SUMMARY] Notation
> $f:A \rightarrow B$ The function $f$ maps elements from $A$ to $B$

A function $f:A \rightarrow B$ is a set $f\subseteq A\times B$, such that for ***every*** $a \in A$, there exists a **unique** $b \in B$, such that $(a,b) \in f$ (**NOTE:** "unique" as in n:1 for A to B, not 1:1. This basically means that 1:n is disallowed, e.g. $\{(1,2), (2,2), (1,1)\}$ is *not a function*)

**Remark**: Definition corresponds to the idea of a "graph of a function"

**Also See [[Analysis Maths 1\|Analysis Maths 1]] (see definitions of domain and codomain)**
## Images and preimages
![Pasted image 20251027160822.png](/img/user/Attachments/Pasted%20image%2020251027160822.png)

> [!NOTE] 
> image $f[A']$ can be read as "all members of B that point to a member of A'"
> Preimage $f⁻¹[B']$ can be read as "all members of B' that are pointed at by a member of A"

## Composing functions
Basically putting a function inside another function
The composition of a $f: A \rightarrow B$ and $g: A \rightarrow B$ would be $g \circ f = f(f(a))$

## inverses
[[Lecture_2.pdf#page=95|Lecture_2, p.15-6]]

> [!WARNING] 
> have another look at this and take some notes
