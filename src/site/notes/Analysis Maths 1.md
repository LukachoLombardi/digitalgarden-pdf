---
{"dg-publish":true,"permalink":"/analysis-maths-1/"}
---

Some more stuff about Proofs
## Implications
![Pasted image 20251023114430.png](/img/user/Attachments/Pasted%20image%2020251023114430.png)
## Contrapositions
> [!SUMMARY]
> Proving the contraposition ($\lnot B ⇒ \lnot A$) is just as good as to proposition  ($B ⇒ A$) 

![Pasted image 20251023122747.png](/img/user/Attachments/Pasted%20image%2020251023122747.png)
# Functions

> [!SUMMARY] Definition
> A function is generally defined as a mapping between **domain** (let's call that Set X) and **codomain** (Y) values.
> $$
f: X \rightarrow Y
$$

Notation of all (co-)domain values' mapping: $$x \mapsto f(x)$$
## "-jectivity" types

- general function: codomain values can have many domain values ($f(x_1)=f(x_2) \rightarrow x_1=x_2$, )
- injective: codomain values have **at most one** domain value (every y element Y: y=f(x), A to B is {0,1}:1)
- surjective: codomain values have **at least one** domain value(A to B is \[1-n\]:1)
- bijective: There is **exactly one** domain value per codomain value (1:1 mapping of domain to codomain values)
### Proving mapping types

> [!NOTE] 
> Surjectivity proofs won't come up on exams

- injectivity: **Prove** if $f(a) = f(a')$, then $a=a'$
- not injective: **find** $a \neq a'$ for $f(a) = f(a')$
- surjective: for every $b \in B$, **find** $a \in A$ such that $f(a) = b$ 
- not surjective: To check that f is not surjective: find $b ∈ B$ and **prove** that there is no $a ∈ A$ such that $f(a) = b$.
# Trigonometric functions
you learned this in school. x is cos, y is sin, imagine the circle, etc....
Derivatives follow the order: sin -> -sin -> cos -> -cos

# Sequences
A sequence is a function $x: \mathbb{N} \rightarrow \mathbb{R}$. Application of such a function is noted as $x_n$, **NOT** $\cancel{x(n)}$. The whole function can also be written as $(x_n)_{n \in \mathbb{N}}$, $(x_n)_{n=1}^{\infty}$ or just $(x_n)_n$.

## Convergence
This is basically just $\lim\limits_{x\to\infty} (x_n)_n$.
See [[Ana1_EN-1.pdf#page=8|Ana1_EN-1, p.4]] for more info.
TODO: Look at 2.3 and 2.4 again

