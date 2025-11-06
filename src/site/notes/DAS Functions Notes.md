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
> image $f[A']$ can be read as "all members of A' that point to a member of B"
> Preimage $f⁻¹[B']$ can be read as "all members of A that are pointed at by a member of B'"
> (So basically all possible input and output values of f)

## Composing functions
Basically putting a function inside another function
The composition of a $f: A \rightarrow B$ and $g: A \rightarrow B$ would be $g \circ f = f(f(a))$.
### Identity Functions
A function $Id_A(x) = x$ on a set $A$ maps $A \rightarrow A$ and returns $x$. It's worth noting that $Id_A(x) = f^{-1}(f(x)) = f^{-1} \circ f$ for a function $f: A \rightarrow B$ (B being an arbitrary set).
## Inverses
Slides with illustrations: [[Lecture_2.pdf#page=95|Lecture_2, p.15-6]]
The inverse $f^{-1}$ for a function $f: A \rightarrow B$ maps back $B \rightarrow A$. ("Umkehrfunktion" in German). It can only be defined on a *bijective* $f$, since it would otherwise break the function definition by associating multiple codomain values of $f$ with single domain values.
