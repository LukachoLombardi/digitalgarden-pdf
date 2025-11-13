---
{"dg-publish":true,"permalink":"/linear-algebra-maths-1/"}
---

# Some Notation
## Sets
See [[Discrete Algebraic Structures#A set\|this]]

> [!INFO] Profs notation
> Prof specified $S=\{...\}$ as $S:=\{...\}$
### Important Sets
- $\mathbb{N}$ all natural numbers
- $\mathbb{N_0}$ all natural numbers and zero
- $\mathbb{Z}$ set of all integers (ganze Zahlen), includes negative numbers
- $\mathbb{Q}$ all rational numbers (e.g. fractions)
- $\mathbb{R}$ all real numbers
### Equality
> [!INFO] Definition
> Sets are equal if they contain the same elements
### Additional Notation
$\forall$: For all
$\exists$: There exists
":": "such that" ("|" also works)
### Examples
All natural numbers: $\{x \in \mathbb{Z}:x² = 25\}$
All integers numbers: $\{x \in \mathbb{N}:x² = 25\}$
All real numbers: $\{x \in \mathbb{R}:x² = 25\}$

### Set operations
See [[Discrete Algebraic Structures#Selectors\|this]] about operations/selectors
## Intervals
$[]$: Inclusive
$()$: Exclusive
$\infty$: Used to specify unbounded interval borders

Backwards intervals are empty (as they're invalid)
## Absolute values
$|x|$: value of x (without signs)
When used with sets: Number of elements

For $x,y\in\mathbb{R}$: 
- $|a*b| = |x| * |y|$
- $|x+y|\le |x| + |y|$
## Sum Notation
From: [[Foundations_Ana_LinAlg_EN.pdf#page=7&offset=,212,|Foundations_Ana_LinAlg_EN, p.3]]
![Pasted image 20251021135417.png](/img/user/Attachments/Pasted%20image%2020251021135417.png)
### Index Shifts
From: [[Foundations_Ana_LinAlg_EN.pdf#page=12|Foundations_Ana_LinAlg_EN, p.8]]
![Pasted image 20251021140205.png](/img/user/Attachments/Pasted%20image%2020251021140205.png)
## Product Notation
From: [[Foundations_Ana_LinAlg_EN.pdf#page=11|Foundations_Ana_LinAlg_EN, p.7]]
![Pasted image 20251021135700.png](/img/user/Attachments/Pasted%20image%2020251021135700.png)

> [!NOTE] Sums and products
> Commutative, Associative and Distributive laws apply to sums and products

# Vector Recap
TODO: Write down the stuff from [[Math_1_LinAlg_VL03_print_EN.pdf]] that you feel worth remembering

# Linear Equation Systems (LES)
## Basic Definition
![[Math_1_LinAlg_VL04_print_EN.pdf#page=4&rect=131,40,487,806|Math_1_LinAlg_VL04_print_EN, p.4]]
Not really all that important, you learned this in High School.

## Graphic representation
You can graph LES with n=2 as linear graphs and n=3 as planes. You can't graph beyond that, since we can't see in 4D. The definitive intersection pinpoints the LES' result. This is also a pretty nice way to demonstrate special cases of solution sets $\mathbb{L}$:
n=2:
- Graphs intersect at one point: That's the solution
- Graphs are parallel: No solution
- Graphs are identical: Infinite solutions
n=3:
- All planes intersect at one point: Solution!
- Two planes intersect in some capacity and the third one is doing its own thing (being parallel and offset to one of the other two): No solution :(
- All planes are identical: Infinite solutions

# Matrices
You can write the coefficients of a LES as a so called **matrix**. This is what a matrix A could look like:
$$
A =\begin{pmatrix}
a_{11} & a_{12} & ... & a_{1n} \\
a_{21} & a_{22} & ... & a_{2n} \\
... & ... & ... & ... \\
a_{m1} & a_{m2} & ... & a_{mn}
\end{pmatrix}
$$
(We have $a_{ij} \in \mathbb{R}$ of course.)
as with a LES:
- m: height/rows
- n: width/columns
A Matrix A of height m and width n would be called a "$m \times n$ matrix" and written as 
$$
A \in \mathbb{R}^{m \times n}
$$
if m=n we call it a square matrix (because it's a square).

## Main diagonal
This is the longest possible diagonal across a matrix A.
It is formed by: 
$$D = \{x_{ij} \in A,with\,A \in R^{m \times n} : i=j \wedge (i,j) \leq k,with\, k = min(m,n)\}$$
## Multiplying Matrices and Vectors
Multiplying a vector x with a matrix A creates a vector b. We just multiply each matrix rows' columns with the equivalent vector row. As shown here (I'm too lazy to type this out):
![[Math_1_LinAlg_VL04_print_EN.pdf#page=9&rect=244,43,528,801|Math_1_LinAlg_VL04_print_EN, p.9]]

> [!WARNING] 
> The length n of your vector x need to be equivalent to the width n of your matrix. Otherwise we get an undefined multiplication.

## Rowwise and columnwise multiplication view
![[Math_1_LinAlg_VL04_print_EN.pdf#page=11&rect=109,38,528,803|Math_1_LinAlg_VL04_print_EN, p.11]]

# Matrices as LES mappings
We can use vectors as in/out values for functions. We take this a step further, by not only scaling, adding or coupling them with other vectors, but transforming them by applying a matrix. Look at the graphic:
![[Math_1_LinAlg_VL04_print_EN.pdf#page=12&rect=68,13,522,824|Math_1_LinAlg_VL04_print_EN, p.12]]
This is a subcategory of LES', specifically it is a **System of linear mappings** (LMS)

## Special types of LMS
1. Zero matrix: $0 \in \mathbb{R}^{m \times n}$ (all elements are zero)
	1. This mapping returns the zero vector $o$
	2. The mapping is called $f_0: \mathbb{R}^n \rightarrow \mathbb{R}^m, x \mapsto o$, or $x \mapsto x \times 0$
2. Identity matrix $I_n \in \mathbb{R}^{n \times n}$
	1. square matrix with it's main diagonal being 1.
	2. A pretty nifty way to just return the vector that's thrown into $I_n \times x$
	3. We call the mapping function using this matrix $f_I$
3. Reflection around the $x_2$ axis of $\mathbb{R}^2$
	1. if $D=\begin{pmatrix}-1&0\\0&1\end{pmatrix}$ then $f_d: \begin{pmatrix}x_1\\x_2\end{pmatrix} \mapsto \begin{pmatrix}-x_1\\x_2\end{pmatrix}$
4. Conversely the reflection around the $x_1$ axis of $\mathbb{R}^2$
	1. if $E=\begin{pmatrix}1&0\\0&-1\end{pmatrix}$ then $f_d: \begin{pmatrix}x_1\\x_2\end{pmatrix} \mapsto \begin{pmatrix}x_1\\-x_2\end{pmatrix}$
The last two seem pretty unnecessary imo

## In-/Sur-/Bijectivity of LMS
You can try memorizing this:
![[Math_1_LinAlg_VL04_print_EN.pdf#page=14&rect=111,38,527,799|Math_1_LinAlg_VL04_print_EN, p.14]]

But I honest to god have no fucking idea how you're supposed to apply this to arbitrary LMS. I'm not even sure LeBorne even made an attempt to explain it.

# Linearity
TODO