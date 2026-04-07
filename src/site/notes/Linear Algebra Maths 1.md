---
{"dg-publish":true,"permalink":"/linear-algebra-maths-1/"}
---

# Some Notation
## Sets
See [[Discrete Algebraic Structures#A set\|Discrete Algebraic Structures#A set]]

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
I'm gonna gloss over most of this since you probably know about it from High-School. The exact slides can be found in [[Math_1_LinAlg_VL03_print_EN.pdf]].
## Basic Rules
- Real Vectors are defined in $\mathbb{R}^n$, $n$ being the dimensions of the vector.
- Vectors can be scaled by a factor $\alpha$ (called scalar multiplication), multiplying all its rows/members by that factor.
- Two vectors of size $n$ can be added by adding every row of the two
- Two vectors of size $n$ can be multiplied using the *dot product*, denoted through $<v_1,v_2>$ or $v_1 \circ v_2$. 
	- This yields the scalar form $v_{11} \times v_{21} + v_{12} \times v_{22} + ... + v_{1n} \times v_{2n}$
	- This scalar is shows the cosine value of the angle between two normalized vectors.
	- If The dot product is $=0$, the two vectors are always orthogonal to each other.
- The cross product of two $v \in \mathbb{R}^n$ can be formed like this: ![[Math_1_LinAlg_VL03_print_EN.pdf#page=13&rect=30,608,566,718|Math_1_LinAlg_VL03_print_EN, p.13]]![[Math_1_LinAlg_VL03_print_EN.pdf#page=13&rect=37,140,315,319|Math_1_LinAlg_VL03_print_EN, p.13]]
## Special vectors
- The Zero Vector $o$: Zero for all elements
- Canonical Unit Vector for an $n$'th dimension: A vector $\in R^{\geq n}$ which is $o$ but has its $n$'th element $= 1$.
## Linear Combinations
![[Math_1_LinAlg_VL03_print_EN.pdf#page=9&rect=29,119,567,366|Math_1_LinAlg_VL03_print_EN, p.9]]

## Representing Spacial Sets
Just remember that most sets have parameter and normal forms (e.g. lines and planes).
![[Math_1_LinAlg_VL03_print_EN.pdf#page=12&rect=29,582,567,725|Math_1_LinAlg_VL03_print_EN, p.12]]
![[Math_1_LinAlg_VL03_print_EN.pdf#page=12&rect=246,105,579,369|Math_1_LinAlg_VL03_print_EN, p.12]]

## Affine and Convex Combinations
![[Math_1_LinAlg_VL03_print_EN.pdf#page=7&rect=30,204,567,331|Math_1_LinAlg_VL03_print_EN, p.7]]
A convex combination is of course $\subseteq$ affine combination. 
Both yield a position vector on the line through $A$ and $B$.
Only Convex Combinations yield a position vector which is *between* $A$ and $B$.
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
This is a kind of LES, specifically it may be called a **System of linear mappings** (LMS)

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

~~But I honest to god have no fucking idea how you're supposed to apply this to arbitrary LMS. I'm not even sure LeBorne even made an attempt to explain it.
I guess you could argue something about linear dependence here? A single row of the matrix might produce the same output for two different vector mults, but as long as the other rows aren't literally identical to it, they will produce a value different from the one contained in the "original" output. So as long as that second condition is satisfied, LMS' are bijective. Or I could be completely wrong about this idk~~

Regarding formal determination of sur-/injectivity and invertibility, see [[#Solvability]] further down below, specifically it's subheadings.

# Linearity
This determines whether or not we can call a LMS *linear*.
![[Math_1_LinAlg_VL04_print_EN.pdf#page=20&rect=110,40,275,801|Math_1_LinAlg_VL04_print_EN, p.20]]

> [!CAUTION] This is not "commutativity"
> As seen below, being able to write an operation on an element $op(a \,op' \, b)$  as $op(a)\, op'\, op(b)$ is **not** called *commutativity*. Hence the specific namings for this property, here specifically regarding vector to vector mappings inside vector space $R^n$:
> - ($+$): additive
> - ($\times$): homogeneous
> - ($+$) and ($\times$): linear


![[Math_1_LinAlg_VL04_print_EN.pdf#page=21&rect=137,37,326,806|Math_1_LinAlg_VL04_print_EN, p.21]]

# Solving LES
I'm not gonna recap this. The concept of augmented matrices and the Gauss/Gauss-Jordan Algorithm are explained in [[Math_1_LinAlg_VL05_print_EN.pdf#page=1|Math_1_LinAlg_VL05_print_EN, p.1]].
## Some additional terminology
- **row echelon form**: LES in which you can draw a line proceeding one to the bottom and at least one to the right per step, which only contains zeroed out elements below it.
- **pivot element**: (nonzero) Element that is used to zero out elements in rows below it
- **dependent variable**: Variable that has a pivot element in its column
- **free variable**: Variable that doesn't have a pivot element
If all LES variables are dependent, the solution is unique. One free variable already implies infinite solutions.
- **rank**: The rank of an LES ($rank()$), is the max count of its pivot elements/rows.
	- eliminating a LES to row echelon form will *always* yield the same amount of pivot rows
	- $rank(A) \leq m;\, rank(A) \leq n$ (at most one pivot element per row and per column).

![[Math_1_LinAlg_VL05_print_EN.pdf#page=19&rect=69,40,212,803&color=red|Math_1_LinAlg_VL05_print_EN, p.19]]

## The Kernel
![[Math_1_LinAlg_VL05_print_EN.pdf#page=20&rect=106,40,313,802&color=red|Math_1_LinAlg_VL05_print_EN, p.20]]
The kernel is also called nullspace (that's a way better name imo).

The Solution to the inhomogeneous LES is a linear combination of the unique inhomogeneous solution and arbitrary Kernel member vectors, i.e. solutions for the homogeneous systems. ([[Math_1_LinAlg_VL05_print_EN.pdf#page=21|Math_1_LinAlg_VL05_print_EN, p.21]])
## Noting infinite solutions spaces
![[Math_1_LinAlg_VL05_print_EN.pdf#page=24&rect=72,38,513,803|Math_1_LinAlg_VL05_print_EN, p.24]]
(at least that's what I think this is good for)
## The LES Range
Defined as 
$$
Ran(A) := \{Ax:x \in \mathbb{R}^n\} \,\text{which is} \subset \mathbb{R}^m \,\text{for some}\, A \subseteq \mathbb{R}^{m \times n}
$$
I'd memorize this as:
> The set of all possible outputs of an LMS using A (the codomain $B; b \in B$ if you will)

The course defines it as:
> The set of all possible linear combinations of A's columns

These are both true.

## Solvability
![[Math_1_LinAlg_VL06_print_EN.pdf#page=3&rect=109,41,510,803&color=red|Math_1_LinAlg_VL06_print_EN, p.3]]
The most important takeaway is probably that a $b$ has to be an element of $f_A: x \mapsto Ax :=b$'s codomain, meaning of $Ran(A)$, in order to create a solvable LES.

In addition to [[#Some additional terminology]], $rank(A) := m \leq n$ for the LES to be solvable.
Some additional equivalent statements:

### Unconditional solvability (surjectivity)
This is equivalent with surjectivity when treating the LES as a mapping. This implies a number of **non-unique** solutions.
![[Math_1_LinAlg_VL06_print_EN.pdf#page=4&rect=109,37,481,807&color=red|Math_1_LinAlg_VL06_print_EN, p.4]]

### Unique solvability (injectivity)
![[Math_1_LinAlg_VL06_print_EN.pdf#page=6&rect=113,36,511,804&color=red|Math_1_LinAlg_VL06_print_EN, p.6]]
![Pasted image 20260131174055.png](/img/user/Attachments/Pasted%20image%2020260131174055.png)
The most straightforward way to determine this case is probably to see if the kernel is $\{o\}$, or if the determinant is $\neq 0$.

### Determining the solvability
The best way to check sur-/injectivity is probably to check the rank and it's relation to $m,n$.

### Determining the invertibility
![[Math_1_LinAlg_VL06_print_EN.pdf#page=8&rect=116,37,508,801&color=red|Math_1_LinAlg_VL06_print_EN, p.8]]
Can't be bothered to actually understand this right now.

> [!WARNING] Proofs
> I didn't include the specific proofs here for brevity's sake, but since they're quite straightforward to understand, it's a good idea to read through and follow them, starting from [[Math_1_LinAlg_VL06_print_EN.pdf#page=4|Math_1_LinAlg_VL06_print_EN, p.4]].

### Specific implications for square matrices
![[Math_1_LinAlg_VL06_print_EN.pdf#page=9&rect=121,34,437,803&color=red|Math_1_LinAlg_VL06_print_EN, p.9]]

# Spans
A span represents any possible linear combination between the vectors provided to it, as in:
$$
span(v_1,...,v_k) = \{v_1 \lambda_1 + ... + v_k \lambda_k : \forall \lambda \in \mathbb{R}\} \subset \mathbb{R}^n \text{; n as length of all v's }
$$
this is also called the *linear hull*, because it's not like there's already enough synonyms to remember.

Spans are actually pretty cool. They can be used as shorthand notation for lines, planes or even polygons. See some [[Math_1_LinAlg_VL06_print_EN.pdf#page=10|Examples]].

For all $v \in span(v_1,...,v_k)$, any scalar multiplication of v is also part of the span, as in for some $\alpha \in \mathbb{R} : \alpha v \in span(...)$ .

This of course also holds for any linear combination of some $v,v' \in span(...)$.

# Vector Spaces
The set $R^n$ satisfying 
- componentwise addition $+ : R^n + R^n → R^n$ and the 
- scalar multiplication $· : R × R^n → R^n$ 
is a so-called vector space.  

> [!WARNING] Typo?
> The slide [[Math_1_LinAlg_VL06_print_EN.pdf#page=12|Math_1_LinAlg_VL06_print_EN, p.12]] defines the addition as $R^n \times R^n \rightarrow ...$. This is almost certainly a typo.

Note the following properties:
![[Math_1_LinAlg_VL06_print_EN.pdf#page=12&rect=226,49,517,797&color=red|Math_1_LinAlg_VL06_print_EN, p.12]]
This is the definition of the "default" vector space $R^n$

## $R^n$ Subspaces
A $V \subset \mathbb{R}^n$ has to satisfy the following properties to be considered a **subspace** of $\mathbb{R}^n$:
![[Math_1_LinAlg_VL06_print_EN.pdf#page=13&rect=206,54,286,373&color=red|Math_1_LinAlg_VL06_print_EN, p.13]]
![[Math_1_LinAlg_VL06_print_EN.pdf#page=13&rect=354,39,482,800&color=red|Math_1_LinAlg_VL06_print_EN, p.13]]

# Linear (in-)dependence
If we want to prove linear independence of a family $F$, it's best to form a matrix $A$ from its member vectors and then proving that $Ker(A) = {o}$, which is equivalent to proving that $rank(A) = n$, which again is equivalent to showing that $A$ has only dependent variables.
### Family
a *family* is a finite subset of a set. Seems to be the standard notation for linear independence analysis.

![[Math_1_LinAlg_VL06_print_EN.pdf#page=15&rect=109,40,325,798&color=red|Math_1_LinAlg_VL06_print_EN, p.15]]
Basically, linear dependence is given by whether or not some of the family's member vectors are linearly dependent on each other, i.e. scalar multiplications of each other.

![[Math_1_LinAlg_VL06_print_EN.pdf#page=17&rect=111,39,306,802&color=red|Math_1_LinAlg_VL06_print_EN, p.17]]
Blablabla, some more properties to maybe memorize.
It's sufficient to just disprove dependence in order to prove independence. Look at the slides if you need it listed out again.

# Basis
![[Math_1_LinAlg_VL06_print_EN.pdf#page=19&rect=210,42,370,799&color=red|Math_1_LinAlg_VL06_print_EN, p.19]]
A basis is basically just the smallest linearly independent family whose span maps out its full subspace. Removing a member from the family will therefore remove this property.

> [!INFO] Generating Set vs Basis
> A Generating Set is defined as **any** set of vectors that map out a vector space, whereas a *Basis* is a special kind of Generating Set, with the added constraint of having minimal elements and therefore having the size of $dim(Subspace)$ (see below).

![[Math_1_LinAlg_VL06_print_EN.pdf#page=20&rect=112,41,227,801&color=red|Math_1_LinAlg_VL06_print_EN, p.20]]
**Read the proof**!

Haven't looked through these yet, so some info on the proofs might follow:
![[Math_1_LinAlg_VL06_print_EN.pdf#page=21&rect=108,41,235,802&color=red|Math_1_LinAlg_VL06_print_EN, p.21]]

## Dimension of a subspace
![[Math_1_LinAlg_VL06_print_EN.pdf#page=23&rect=109,43,231,803&color=red|Math_1_LinAlg_VL06_print_EN, p.23]]
Remember the $dim()$ operator! (Size of smallest possible family spanning the whole subspace)
![[Math_1_LinAlg_VL06_print_EN.pdf#page=24&rect=195,36,386,801|Math_1_LinAlg_VL06_print_EN, p.24]]
# Matrix computations
## Matrix addition
Matrix addition is a **component-wise** operation. To add two matrices, they **must have the same dimensions** (e.g., both must be m×n). You simply add the corresponding elements from each matrix.
- **Rule:** $A+B=C$, where $c_{ij​}=a_{ij​}+b_{ij}$​.
- **Properties:** It is both commutative ($A+B=B+A$) and associative.
## Matrix factor multiplication
Should be self explanatory, just multiply every matrix cell with a factor.
## Matrix Matrix multiplication
To multiply matrix A by matrix B, the number of **columns in A** must equal the number of **rows in B**. The resulting matrix has the rows of the first and the columns of the second.
- **The Dot Product Rule:** The element at row i and column j in the resulting matrix is the dot product of the $i$th row of A and the $j$th column of B.
- **Crucial Note:** Unlike regular numbers, matrix multiplication is **not commutative** ($AB \neq BA$ in most cases).
The result of $C = AB$ can be seen as the resulting vectors from applying every column of $B$ to $A$ being written as the columns of $C$.
## Square Matrix Powers
Matrix exponentiation is only defined for **square matrices** (n×n). If a matrix A is square, you can multiply it by itself multiple times.
- **Notation:** $Ak=A⋅A⋅⋯⋅A$ ($k$ times).
- **Identity:** $A^0=I$, where I is the identity matrix (the matrix equivalent of the number 1).
# The inverse matrix
The inverse of a square matrix A is denoted as $A^{−1}$. It is the matrix that "undoes" the transformation of A.
- **The Identity Property:** $A⋅A^{−1}=I$ and $A^{−1}⋅A=I$.
- **Invertibility:** Not all matrices have an inverse. A matrix must be square and its **determinant must not be zero** ($det(A) \neq 0$) to be "invertible" or "non-singular."
- **Solving Equations:** Inverses are used to solve matrix equations like $Ax=b$ by calculating $x=A^{−1}b$.
For invertible **orthogonal** Matrices, the inverse is identical to the transpose. This will come up later in [[Linear Algebra Maths 1#Orthogonal Matrices\|Linear Algebra Maths 1#Orthogonal Matrices]].
### What's the transpose?
You basically just switch the rows and columns when transposing a matrix, so for 
$$
A = 
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
$$
$$
A^T = 
\begin{bmatrix}
1 & 3 \\
2 & 4
\end{bmatrix}
$$
#### Some Computation Rules:
![[Math_1_LinAlg_VL08_print_EN.pdf#page=4&rect=107,39,315,804|Math_1_LinAlg_VL08_print_EN, p.4]]
![[Math_1_LinAlg_VL08_print_EN.pdf#page=5&rect=127,38,379,808|Math_1_LinAlg_VL08_print_EN, p.5]]
# LU Decomposition
The LU Decomposition is an approach to simplify the solution of an LES $Ax = b$, by basically "recording" the steps needed to reach row echelon form in a separate matrix. This allows faster computations when solving the same LES for different inputs, since our transformation is now independent from the augmented column.

## Separating A into Lower and Upper
To reach $LU = A$, we form so called *lower* and *upper* *triangular matrices*. This is best demonstrated through intuition.
E.g.:
$$
L = 
\begin{bmatrix}
1 & 0 & 0 \\
1 & 1 & 0 \\
1 & 1 & 1
\end{bmatrix}
$$
$$
U = 
\begin {bmatrix}
1 & 1 & 1 \\
0 & 1 & 1 \\
0 & 0 & 1
\end{bmatrix}
$$

### My explanation™
Now how do we do this decomposition on an actual matrix? First, it may be important to understand what exactly the transformation $L$ on $U$ actually means. We should already be aware of the fact, that if $L = I \Rightarrow LU = U$. 

You can spend some time rotating and computing matrices in your head to get an intuition on why this is, but simply speaking, $IU$ can just be seen as *"for every row $ur_m$ of $U$, add that row **once** to the equivalent row of the resulting matrix"*. 

Can you see where this is going? I'm going to make it easy for you: our left hand matrix in the multiplication can be used to fully represent the transformation steps we have taken to get our right hand matrix to its current form. Specifically, the row modifications are recorded in it in the following form - where any $l_{mn}$ represents how often we add row $ur_n$ of $U$ to row $ar_m$ of the resulting matrix $A$ (just pretend this table is a matrix, can't use $\LaTeX$ packages in obsidian):

|        | $ur_1$ | $ur_2$ | $ur_3$ | $ur_4$ |
| ------ | ------ | ------ | ------ | ------ |
| $ur_1$ | 1      | 0      | 0      | 0      |
| $ur_2$ | 1      | 1      | 0      | 0      |
| $ur_3$ | 0      | 2      | 1      | 0      |
| $ur_4$ | 0      | 0      | 0      | 1      |
When applying this $L$ to $U$ as in $LU = A$, read it as: 
- use $1 \times$row 1 of $U$ for row $1$ of $A$
- use $1\times$row 1 $+$ $1\times$row 2 for row $2$
- use ($0\times$row 1 $+$) $2\times$row 2 $+$ $1\times$row 3 for row $3$
- use $1\times$row 4 for row 4

### The Algorithm by Hand
Now that we've gotten this out of the way, let's see how we would use this fact to compute our $LU = A$:
- Instead of $A$, write $I \times A$
- Transform A into row echelon form (while only modifying rows using rows above it!)
- While transforming, note every operation you make into the associated cell of your left matrix as seen above,  **times $-1$**! (this is important because our left-hand matrix shows how to **revert** the transformation we executed, not how to turn the original matrix into row echelon form)
	- e.g. we add row $1$ $\times 3$ to row $2$: write $-3$ to $l_{21}$

There you go! You've successfully performed this ungodly procedure by hand, something that will **definitely** be extremely important in your MS Teams centric Desk-Job 5 years from now!
## Computing $Ax = b$ using LU Decomposition
This is the moment we've all been waiting for:
![[Math_1_LinAlg_VL08_print_EN.pdf#page=7&rect=408,53,486,739|Math_1_LinAlg_VL08_print_EN, p.7]]
Basically, for $LUx = b$ (remember, matrix multiplications are read right to left!), we:
- compute $Ux (=y)$
- then solve $Uy = b$, oh wait, $U$ is already in row echelon form, yippee!
Do you see why the LU Decomposition approach is actually pretty cool?
## Some more yapping
Actually, this approach is already somewhat optimized, which is why even with the background knowledge of "recording", it might seem un-intuitive. 

The first instinct upon discovering this relation would probably be to just keep the transformation of $A$ to row echelon form, and then just apply it to any augmentation of $A$, right? As in keeping $A$ as is, then applying our transformation matrix $T$ to $[A | b]$ for every single system. The thing is that this still requires us to think about individual entries of $b$, adding them together through our transformation and so on...

This is why the LU Decomposition is actually so smart:
- We keep our $A$ in row echelon form ($U$), but don't just ignore away the operations we made on i (remember, we can't just write $Tx = b$ without transforming $b$ as well!). instead we keep their reverse in $L$, allowing us to write $LU$ as an actual complete stand in for $A$.
- At that point we *do* have to solve two different LES, but due to sticking to triangular matrices, these are already in row echelon form and only require us two write out the actual result vector calculations!

> [!INFO] What about the matrix's columns/vectors?
> I haven't given this a lot of thought, but from what we can see later down the line with QR decomposition, it seems pretty obvious that the analogous "operation recording" pattern holds for columns when we switch the order of the matrix multiplication operation.
>

# The Determinant
Unrelated to the definition the lecture gives for the determinant $det(A)$ of some matrix $A \in \mathbb{R}^{m \times n}$ (or rather lack thereof), here's a pretty good intuitive definition:
> The determinant $det(A)$ describes the oriented factor by which $A \in \mathbb{R}^{m \times n}$ stretches any input vector $x$ when applied as $A \times x$. 

(Remember: Oriented means it can be negative).

 This also applies to stretching a whole coordinate system or a family of vectors. Specifically, when applied to a shape, it will give the stretch factor of its area in 2D, or of its volume in 3D.

The lectures vaguely define it as the area of a Parallelogram spanned by two vectors making up the columns of $A$ in 2D, or the volume of the Parallelepiped spanned by three vectors making up the columns in 3D. This is a very un intuitive definition in my opinion, since intuitively you'd probably just look at the distances spanned by the vectors to approach these questions.
## The case $det(A) = 0$
The determinant being equal to 0, that means that the linear transformation using $A$ will squish the system onto a single line, or point. It intuitively also means that the spanned shapes will have $area = 0$.

This also means that the transformation using $A$ reduces the input vectors by at least one dimension!

$det(A) = 0$ can be inferred by:
- at least two columns being identical
- the family of columns being linearly dependent
## Negative determinants
A negative determinant means that the transformation will invert the input space. 
![[Math_1_LinAlg_VL09_print_EN.pdf#page=9&rect=73,10,516,809|Math_1_LinAlg_VL09_print_EN, p.9]]

## Computing the Determinant in 2D
This is a pretty good illustration if you want to understand the formula in depth. It is the general formula on 2D matrices:
![Pasted image 20251216181209.png](/img/user/Attachments/Pasted%20image%2020251216181209.png)

Here is a formal proof, I don't think it's important:
![[Math_1_LinAlg_VL09_print_EN.pdf#page=8&rect=274,45,518,796|Math_1_LinAlg_VL09_print_EN, p.8]]

If we (for 2D spaces) define $det(A) = area(A_{m1},A_{m2})$, we get the following set of rules that this area formula should adhere to:
![[Math_1_LinAlg_VL09_print_EN.pdf#page=5&rect=111,42,526,800|Math_1_LinAlg_VL09_print_EN, p.5]]

Note: (3) essentially means that switching the columns' order in the input will reverse the sign on the output.

## Computing the Determinant in 3D
![[Math_1_LinAlg_VL09_print_EN.pdf#page=10&rect=112,40,500,800|Math_1_LinAlg_VL09_print_EN, p.10]]

We build our initial definition of $volume(u,v,w)$ from these rules:
![[Math_1_LinAlg_VL09_print_EN.pdf#page=12&rect=76,15,491,790|Math_1_LinAlg_VL09_print_EN, p.12]]
Then we leverage the rule of homogeneity for the volume we established earlier in order to move our actual vector members out of the the volume itself, which will then be either $1$ or $-1$ by usage of the system unit vectors. In case these $e$s are unclear for a 3D space:
$$
e_1 = 
\begin{pmatrix}
1 \\
0 \\
0 
\end{pmatrix}
$$
$$
e_2 = 
\begin{pmatrix}
0 \\
1 \\
0 
\end{pmatrix}
$$
$$
e_3 = 
\begin{pmatrix}
0 \\
0 \\
1 
\end{pmatrix}
$$
The first definition can then be written as the sum of all possible ordered combinations of $[1,3]$ onto $i,j,k$ without replacement, as applied in the term above. Since we only need to compute the sign for the actual volume function, we can leverage rule (3) from above, turning it into a comparably easy formula (as seen in the last step).

Abstracting back to our matrix $A \in \mathbb{R}^{3 \times 3}$, we can now say that $det(A) = area(u,v,w)$, for columns of $A$ mapped to $u, v, w$ (as in $\{A_mc | m \in n\} = \{u,v,w\}$).
## The General Case
This is very it gets fucky.![[Math_1_LinAlg_VL09_print_EN.pdf#page=13&rect=109,42,528,801|Math_1_LinAlg_VL09_print_EN, p.13]]This slide is ass to understand, because it rolls back the concreteness of "area" and "volume" used in the 2D and 3D examples. Since we can't really see beyond the third dimension, we're suddenly back to actual matrices and the very under defined notion of whatever a "determinant" actually is. We actually kind of know the answer to this, having read [[Linear Algebra Maths 1#The Determinant\|Linear Algebra Maths 1#The Determinant]], but since this lecture is based on very different intuition, we will have to bear with the following:

This syntax is horribly confusing when coming from the last two examples. So just continue thinking in columns (vectors 🤓☝️) and imagine some area/volume-analogous property we could compute on this "thing's" columns/vectors in $(>3)D$ space, which is again equal to $det$.

### Formula No.1: The Permutation Formula by Leibnitz
We then treat this case as analogous to the summation we established in 3D, giving us this beautifully stupid term that you will hopefully never have to solve by hand:
![[Math_1_LinAlg_VL09_print_EN.pdf#page=16&rect=76,12,509,778|Math_1_LinAlg_VL09_print_EN, p.16]]
This is an additional helper for computing the sign of the system unit vectors determinant for a given:
![[Math_1_LinAlg_VL09_print_EN.pdf#page=17&rect=76,14,503,784|Math_1_LinAlg_VL09_print_EN, p.17]]

> [!NOTE] The $\#$ operator
> The $\#$ operator is very badly explained here if it weren't for the examples. It just describes the minimum number of times you have to switch two elements of a tuple until it becomes ordered (ordered without gaps in this case).

In this case it means the "distance" of switches your current tuple of system identity vectors is away from its ordered "base" form.

![[Math_1_LinAlg_VL09_print_EN.pdf#page=18&rect=78,12,522,805|Math_1_LinAlg_VL09_print_EN, p.18]]

### Formula No.2: Determinant using Gauss
![[Math_1_LinAlg_VL09_print_EN.pdf#page=19&rect=72,11,461,812|Math_1_LinAlg_VL09_print_EN, p.19]]
"Upper triangular form" is better known as "row echelon form".
Note how the $b$'s used here are the main diagonal.

Here's a proof if you really care:
![[Math_1_LinAlg_VL09_print_EN.pdf#page=22&rect=71,7,506,809|Math_1_LinAlg_VL09_print_EN, p.22]]
![[Math_1_LinAlg_VL09_print_EN.pdf#page=23&rect=368,54,519,823|Math_1_LinAlg_VL09_print_EN, p.23]]
![[Math_1_LinAlg_VL09_print_EN.pdf#page=24&rect=283,58,467,797|Math_1_LinAlg_VL09_print_EN, p.24]]

### Formula No.3: Laplace Expansion
First, consider the following Theorem:
![[Math_1_LinAlg_VL09_print_EN.pdf#page=25&rect=207,39,370,803|Math_1_LinAlg_VL09_print_EN, p.25]]
![[Math_1_LinAlg_VL09_print_EN.pdf#page=26&rect=114,41,513,803|Math_1_LinAlg_VL09_print_EN, p.26]]
![[Math_1_LinAlg_VL09_print_EN.pdf#page=27&rect=106,32,518,808|Math_1_LinAlg_VL09_print_EN, p.27]]
![[Math_1_LinAlg_VL09_print_EN.pdf#page=28&rect=217,45,483,800|Math_1_LinAlg_VL09_print_EN, p.28]]

## Cramer's Rule
This guy named Cramer had a rule or some shit. Basically for an LES $Ax = b$ and $det(A) \neq 0$ (meaning an injective mapping), we can get the solution to $x$ using this rule.
The rule states, that for $Ax = b$, we can determine the solution of $x_k$ by $x_k = \frac{det(A_k)}{det(A)}$, with $A_k$ being the determinant of $A$ with the $k$'th column replaces by $b$. The lecture says this is unnecessary though, so we can just forget about it.
# Affine Subspaces
![[Math_1_LinAlg_VL10_print_EN.pdf#page=2&rect=133,41,275,803|Math_1_LinAlg_VL10_print_EN, p.2]]
![[Math_1_LinAlg_VL10_print_EN.pdf#page=3&rect=150,19,455,814|Math_1_LinAlg_VL10_print_EN, p.3]]
Basically an Affine Subspace is a subspace $\subseteq R^n$ that is closed in regards to being moved by a $p \in R^n$.

An alternative (and more computationally relevant) way to define this:
1. An *affine combination* for a given set of vectors $A$ is defined as: $$
\{x_1,...,x_k\} \in A | A \in \mathbb{R}^n 
\Rightarrow
\sum_{i=1}^k \lambda_i = 1 |
\{\lambda_1,...,\lambda_k\} \in \mathbb{F} 
\text{ (normally $F \subseteq \mathbb{R}$)}
$$ Read: An affine combination is a linear combination whose coefficients sum up to $1$.
2. *"closed with regards to affine combinations"* ($\Rightarrow$ **and therefore $A$ being an affine subspace**) is further defined as: $$
\sum_{i=1}^k \lambda_i x_i \text{ is also} \in A
$$Read: An affine subspace contains all affine combinations of its member vectors.
This is essentially a generalization and expansion on [[Linear Algebra Maths 1#Affine and Convex Combinations\|Linear Algebra Maths 1#Affine and Convex Combinations]].
# Properties of Scalar Products
![[Math_1_LinAlg_VL10_print_EN.pdf#page=4&rect=133,32,491,813|Math_1_LinAlg_VL10_print_EN, p.4]]
# Distances/The Norm
This again is High School level stuff. The length/distance/norm of a vector $v \in R^n$ is just $||v|| = \sqrt{v_1^2 + v_2^2 + ... + v_n^2}$
of course, this also means that $v \cdot v = ||v||^2$
![[Math_1_LinAlg_VL10_print_EN.pdf#page=5&rect=107,39,344,803|Math_1_LinAlg_VL10_print_EN, p.5]]
![[Math_1_LinAlg_VL10_print_EN.pdf#page=6&rect=107,39,240,806|Math_1_LinAlg_VL10_print_EN, p.6]]

## Parameter and Normal Forms
![[Math_1_LinAlg_VL10_print_EN.pdf#page=7&rect=108,41,268,802|Math_1_LinAlg_VL10_print_EN, p.7]]
![[Math_1_LinAlg_VL10_print_EN.pdf#page=8&rect=109,40,394,804|Math_1_LinAlg_VL10_print_EN, p.8]]
![[Math_1_LinAlg_VL10_print_EN.pdf#page=9&rect=132,42,491,805|Math_1_LinAlg_VL10_print_EN, p.9]]

## Calculating Distances Between stuff
![[Math_1_LinAlg_VL10_print_EN.pdf#page=15&rect=108,41,519,802|Math_1_LinAlg_VL10_print_EN, p.15]]
![[Math_1_LinAlg_VL10_print_EN.pdf#page=16&rect=108,40,538,801|Math_1_LinAlg_VL10_print_EN, p.16]]
![[Math_1_LinAlg_VL10_print_EN.pdf#page=17&rect=168,40,327,801|Math_1_LinAlg_VL10_print_EN, p.17]]
# Orthogonal Projections onto Subspaces
## The Simplest case: Projecting points onto lines
there are certainly easier ways to do this (I would define a vector from $p$ to the line - including the factor - and then solve its $\times$ product for 0).

However, this is how the lecture does it, so we can approach the general case for projecting any $v \in \mathbb{R}^n$ onto any subspace $s \subset \mathbb{R}^n$. 

![[Math_1_LinAlg_VL11_print_EN.pdf#page=2&rect=72,13,537,807|Math_1_LinAlg_VL11_print_EN, p.2]]
![[Math_1_LinAlg_VL11_print_EN.pdf#page=3&rect=292,47,490,757|Math_1_LinAlg_VL11_print_EN, p.3]]

## The General Case

### Orthogonal Subspaces
An orthogonal subspace $M^\perp$ of $M \subset \mathbb{R}^n$ contains are vectors orthogonal to all vectors in $M$.
![[Math_1_LinAlg_VL11_print_EN.pdf#page=5&rect=202,41,367,802|Math_1_LinAlg_VL11_print_EN, p.5]]
![[Math_1_LinAlg_VL11_print_EN.pdf#page=6&rect=214,41,337,802|Math_1_LinAlg_VL11_print_EN, p.6]]
![[Math_1_LinAlg_VL11_print_EN.pdf#page=7&rect=112,41,253,801|Math_1_LinAlg_VL11_print_EN, p.7]]
Probably most importantly:
![[Math_1_LinAlg_VL11_print_EN.pdf#page=8&rect=109,40,280,802|Math_1_LinAlg_VL11_print_EN, p.8]]

### Setting up the Projection
![[Math_1_LinAlg_VL11_print_EN.pdf#page=10&rect=111,39,518,803|Math_1_LinAlg_VL11_print_EN, p.10]]
Note that $U^\perp$ is just the span of the normal vector of the plane in this case.

![[Math_1_LinAlg_VL11_print_EN.pdf#page=11&rect=71,10,529,785|Math_1_LinAlg_VL11_print_EN, p.11]]

### Gram Matrices
A Gram Matrix is essentially a way to layout all (not automatically normalized, as they would need to be to represent the cosine of the angle!) orientations of vectors from a family to each other.
![[Math_1_LinAlg_VL11_print_EN.pdf#page=12&rect=123,39,500,803|Math_1_LinAlg_VL11_print_EN, p.12]]
	It can be seen as $<A,A^T>$ of its relating subspace $A$. 
If you want to see the proof of invertibility, look at the [[Math_1_LinAlg_VL11_print_EN.pdf#page=13|Next Slide]]. 
### Relation to the Approximation Theorem
![[Math_1_LinAlg_VL11_print_EN.pdf#page=14&rect=156,40,402,801|Math_1_LinAlg_VL11_print_EN, p.14]]

I'm not sure if any of this is particularly relevant for now:![[Math_1_LinAlg_VL11_print_EN.pdf#page=15&rect=147,40,505,803|Math_1_LinAlg_VL11_print_EN, p.15]]![[Math_1_LinAlg_VL11_print_EN.pdf#page=16&rect=109,41,535,801|Math_1_LinAlg_VL11_print_EN, p.16]]
# Orthogonal Systems and Bases
![[Math_1_LinAlg_VL12_13_print_EN-1.pdf#page=2&rect=161,38,481,805|Math_1_LinAlg_VL12_13_print_EN-1, p.2]]
## Linear Independence of OGS
![[Math_1_LinAlg_VL12_13_print_EN-1.pdf#page=4&rect=116,37,220,803|Math_1_LinAlg_VL12_13_print_EN-1, p.4]]
(This should be self evident, as any given vector cannot be linearly dependent on any arbitrary orthogonal vector or vectors).

![[Math_1_LinAlg_VL12_13_print_EN-1.pdf#page=5&rect=59,36,520,803|Math_1_LinAlg_VL12_13_print_EN-1, p.5]]

> [!DANGER] Fuck this Fuckass Slide
> Note that the $G(B) \times \alpha = ...$ relates to an OGB, **NOT** an ONB, as the ordering of the text above would suggest.

## Fourier Expansions
![[Math_1_LinAlg_VL12_13_print_EN-1.pdf#page=6&rect=129,39,413,801|Math_1_LinAlg_VL12_13_print_EN-1, p.6]]
## Gram-Schmidt Normalization (obtaining ONBs)
![[Math_1_LinAlg_VL12_13_print_EN-1.pdf#page=8&rect=74,11,557,781|Math_1_LinAlg_VL12_13_print_EN-1, p.8]]
And so on for the following vectors, using all previously obtained $w$ components...
> [!ATTENTION] Simplifications
> This slide already heavily simplifies the projection given in [[Linear Algebra Maths 1#The Simplest case Projecting points onto lines\|Linear Algebra Maths 1#The Simplest case Projecting points onto lines]] for the case of $r$ being normalized. I.e.: $p = \frac{u_2 \circ w_1}{w_1 \circ w_1} \times w_1 = u_2 \circ w_1 \times w_1$, since $||w_1|| = 1$ and $w_1 = w_1 \Rightarrow w_1 \circ w_1 = 1$ 

Here's the complete breakdown:
![[Math_1_LinAlg_VL12_13_print_EN-1.pdf#page=10&rect=65,39,538,807|Math_1_LinAlg_VL12_13_print_EN-1, p.10]]
## QR Decomposition
QR Decomposition is essentially a matrix decomposed into the product of its range's orthonormal basis Q (LHS) and the inverse of the manipulations performed to transform the original matrix into the basis matrix, recorded as a right upper triangular matrix R (RHS).

This relies on the same basic concept as LU Decomposition, but instead of tracking row manipulations (or rather their inverse) using the LHS matrix, we track column manipulations using the RHS matrix here. This makes sense, since transforming the range of a matrix (remember, that's just the subspace spanned by its columns) into an ONB is basically just a linear transformation between its columns.

The Process:
- Take the columns of matrix $A$ and treat them as a Generating Family $F$ of $Ran(A)$. Note that we can safely throw out any free column vectors, as they are bound to be linearly dependent on some other member(s) of the family.
- Apply the Gram-Schmidt Normalization to $F$, turning it into an ONB of $Ran(A)$.
	- The resulting vectors form your $Q$ matrix.
- During this process, keep track of the coefficients generated for the previously orthonormalized $w$ vectors, as well as the normalization divisors used.
	- These will be arranged in $R$ as we will see in a second
There we go:
![[Math_1_LinAlg_VL12_13_print_EN-1.pdf#page=14&rect=323,122,488,709|Math_1_LinAlg_VL12_13_print_EN-1, p.14]]

**This Detail might also be interesting to note**:
![[Math_1_LinAlg_VL12_13_print_EN-1.pdf#page=16&rect=281,56,403,792|Math_1_LinAlg_VL12_13_print_EN-1, p.16]]

## Orthogonal Matrices
This definition is kind of a continuation of [[Linear Algebra Maths 1#What's the transpose?\|Linear Algebra Maths 1#What's the transpose?]].
These are some things we've touched on before:
![[Math_1_LinAlg_VL12_13_print_EN-1.pdf#page=17&rect=107,40,520,801|Math_1_LinAlg_VL12_13_print_EN-1, p.17]]
These are basically the implications that we didn't look at in the previous coverage:
![[Math_1_LinAlg_VL12_13_print_EN-1.pdf#page=18&rect=133,37,387,804|Math_1_LinAlg_VL12_13_print_EN-1, p.18]]
![[Math_1_LinAlg_VL12_13_print_EN-1.pdf#page=19&rect=131,39,330,803|Math_1_LinAlg_VL12_13_print_EN-1, p.19]]
## Rotations and Reflections
![[Math_1_LinAlg_VL12_13_print_EN-1.pdf#page=20&rect=112,40,517,802|Math_1_LinAlg_VL12_13_print_EN-1, p.20]]
![[Math_1_LinAlg_VL12_13_print_EN-1.pdf#page=21&rect=130,38,492,803|Math_1_LinAlg_VL12_13_print_EN-1, p.21]]
![[Math_1_LinAlg_VL12_13_print_EN-1.pdf#page=23&rect=73,10,522,806|Math_1_LinAlg_VL12_13_print_EN-1, p.23]]
Note that $D$ and $S$ signify rotation and reflection respectively (probably taken from the German names **D**rehung and **S**piegelung). 
![[Math_1_LinAlg_VL12_13_print_EN-1.pdf#page=25&rect=111,42,534,802|Math_1_LinAlg_VL12_13_print_EN-1, p.25]]
Note that this theorem is in relation to $\mathbb{R}^{3 \times 3}$. These properties **do not** hold for matrices $\in \mathbb{R}^{2 \times 2}$:
![[Math_1_LinAlg_VL12_13_print_EN-1.pdf#page=26&rect=153,39,278,803|Math_1_LinAlg_VL12_13_print_EN-1, p.26]]
Some additional theorems:
![[Math_1_LinAlg_VL12_13_print_EN-1.pdf#page=27&rect=110,42,335,803|Math_1_LinAlg_VL12_13_print_EN-1, p.27]]
I am unsure to what extent these last few theorems are really relevant for the exam. Probably treat these as a bit of an afterthought when studying this module.
