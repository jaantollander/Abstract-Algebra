---
title: Abstract Algebra - Assignment 2
author: Jaan Tollander de Balsch
date: \today
header-includes: \usepackage{unicode-math}
---
## Definitions
A **group** is a triple \((G,·,e)\) where \(G\) is a set, \(·\) is a binary operation on \(G\) and the indentity \(e\), such that the following hold

a) **Closure**: \(x·y∈G\) for all \(x,y∈G\)
b) **Associativity**: \((x·y)·z=x·(y·z)\) for all  \(x,y,z∈G\)
c) **Indentity element**: \(e·x=x·e=x\) for all \(x∈G\)
d) **Inverse element**: For every \(x∈G\) there exists \(y∈G\) such that \(x·y=y·x=e\).

<!-- It's common to omit the symbol \(·\). -->

**Semigroup**: Only (a) holds.

**Monoid** Only (a) and (b) hold.

\(G\) is called **Abelian group** if the following also holds

d) **Commutativity**: For all \(x,y∈G\) we have \(x·y=y·x\).

---

Let \(G\) be a group and \(∅=H⊆G\) a subset of \(G\). We say \(H\) is a **subgroup** of \(G\), formally \(H⊆G\), it is closed under the operation on \(G\) and satisfies all group axioms.

A subset \(H\) of a group \(G\) is a subgroup, if and only if the following hold

a) \(H≠∅\)
b) \(a,b∈H\) implies \(a·b∈H\)
c) If \(a∈H\) then \(a^{-1}∈H\)

Alternatively

I) \(H≠∅\)
II) \(a,b∈H\) implies \(a·b^{-1}∈H\).

## Problem 1
### a)
**Trivial case** \(n=1\): Let \(a_1∈G\) then by *inverse element* axiom
\[
a_1·a_1^{-1}=e.
\]

**Base case** \(n=2\): Let \(a_1,a_2∈G\) then by *closure* axiom also \(x=a_1·a_2∈G\).

\[
\begin{aligned}
x·x^{-1}&=e \\
(a_1·a_2)·(a_1·a_2)^{-1}&=e \\
a_1·(a_2·(a_1·a_2)^{-1})&=e \\
a_2·(a_1·a_2)^{-1} &= a_1^{-1}·e \\
(a_1·a_2)^{-1} &= a_2^{-1}·a_1^{-1}·e \\
(a_1·a_2)^{-1} &= a_2^{-1}·a_1^{-1}. \\
\end{aligned}
\]

**General case** \(n\): Let \(a_1,a_2,…,a_n∈G\) then by the *closure* and *transitivity* axioms
\[
x=a_1·a_2·…·a_{n-1}·a_n =a_1·(a_2·…·(a_{n-1}·a_n))∈G.
\]
Then using the same process as in the base case
\[
(a_1·a_2·…·a_{n-1}·a_n)^{-1}=a_n^{-1}·a_{n-1}^{-1}·…·a_2^{-1}·a_1^{-1}.
\]


### b)
The Caley table for the group \(ℤ_7^×:=\{1,2,3,4,5,6\}\) with multiplication modulo \(7\).

```julia
print(reshape([mod(i*j, 7) for i in 1:6 for j in 1:6],(6,6)))
```

|\(×\)   |1   |2   |3   |4   |5   |6   |
|----|----|----|----|----|----|----|
|**1**   |1   |2   |3   |4   |5   |6   |
|**2**   |2   |4   |6   |1   |3   |5   |
|**3**   |3   |6   |2   |5   |1   |4   |
|**4**   |4   |1   |5   |2   |6   |3   |
|**5**   |5   |3   |1   |6   |4   |2   |
|**6**   |6   |5   |4   |3   |2   |1   |


## Problem 2
