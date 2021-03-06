---
title: Abstract Algebra - Assignment 2
author: Jaan Tollander de Balsch
date: \today
header-includes: \usepackage{unicode-math}
---
## Problem 1
### a)
For a group \(G\), show by induction, that \[(a_1·a_2·…·a_n)^{-1}=a_n^{-1}·…·a_2^{-1}·a_1^{-1}\] for arbitrary \(a_i∈G\), \(i=1,…,n\) and \(n∈ℕ\).

---

**Trivial case** \(n=1\): From *inverse element* axiom
\[
a_1·a_1^{-1}=e.
\]

**Base case** \(n=2\): From *closure* axiom \(x=a_1·a_2∈G\) then

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

**General case** \(n\): Using *closure* and *transitivity* axioms
\[
x=a_1·a_2·…·a_{n-1}·a_n =a_1·(a_2·…·(a_{n-1}·a_n))∈G.
\]
Then using the same process as in the base case
\[
(a_1·a_2·…·a_{n-1}·a_n)^{-1}=a_n^{-1}·a_{n-1}^{-1}·…·a_2^{-1}·a_1^{-1}.
\]

[@contemporary_abstract_algebra, pg. 52]


### b)
Write down the Caley table for the group \(ℤ_7^×:=\{1,2,3,4,5,6\}\) with multiplication modulo \(7\).

---

|\(×\)   |1   |2   |3   |4   |5   |6   |
|----|----|----|----|----|----|----|
|**1**   |1   |2   |3   |4   |5   |6   |
|**2**   |2   |4   |6   |1   |3   |5   |
|**3**   |3   |6   |2   |5   |1   |4   |
|**4**   |4   |1   |5   |2   |6   |3   |
|**5**   |5   |3   |1   |6   |4   |2   |
|**6**   |6   |5   |4   |3   |2   |1   |

Julia code:
```julia
print(reshape([mod(i*j, 7) for i in 1:6 for j in 1:6],(6,6)))
```


## Problem 2
Let \(G\) be a group, and let \(H\) and \(K\) be subgroups of \(G\). Show that \(H∪K\) is a subgroup of \(G\) if and only if \(H⊆K\) or \(K⊆H\).

---

Subgroup axioms for \(H\).

a) \(H≠∅\)
b) \(h_1,h_2∈H\) implies \(h_1·h_2∈H\)
c) If \(h∈H\) then \(h^{-1}∈H\)

Subgroup axioms for \(K\).

a) \(K≠∅\)
b) \(k_1,k_2∈K\) implies \(k_1·k_2∈K\)
c) If \(k∈K\) then \(k^{-1}∈K\)

Lets test subgroup axioms for \(H∪K\). There are three cases in which the group \(H∪K\) **is a subgroup** of \(G\). In all of these, the subgroup axioms of \(H∪K\) reduce to either subgroup axioms of \(H\) or \(K\).

1) If \(H=K\) then \(H∪K=H=K\). Reduces to the subgroup axioms of \(H\) or \(K\).
2) If \(K⊆H\) then \(H∪K=H\). Reduced to the subgroup axioms of \(H\).
3) If \(H⊆K\) then \(H∪K=K\). Reduces to the subgroup axioms of \(K\).

In the fourth case, \(H⊊K\) and \(K⊊H\), \(H∪K\) **is not a subgroup** of \(G\).

**Proof**: This proof provides a counterexample that \(H∪K\) is not **closed under operation** if \(H⊊K\) and \(K⊊H\) which implies that \(H∪K\) **is not a subgroup** of \(G\).

1) Let \(a,b∈H∪K\) such that \(a∈H\), \(a∉K\), \(b∈K\), and \(b∉H\)
2) Implies that \(a·b∈H∪K\)
3) Implies that \(a·b∈H\) or \(a·b∈K\)
4) If \(a·b∈H\) then \(a,b∈H\) or if \(a·b∈K\) then \(a,b∈K\)
5) These are in conflict with the assumptions and therefore \(a·b∉H∪K\) and \(H∪K\) is not a subgroup of \(G\).

<!--
a
\(H≠∅\) and \(K≠∅\) implies \(H∪K≠∅\)

c

1) If \(a∈H∪K\) then \(a∈H\) or \(a∈K\).
2) If \(a∈H\) then \(a^{-1}∈H\)
3) If \(a∈K\) then \(a^{-1}∈K\)
4) Since \(H⊂H∪K\) and \(K⊂H∪K\) then \(a^{-1}∈H∪K\) -->


## Problem 3
Let \(G\) be a group and let \(H\) be a subset of \(G\).

---

### a
If \(H\) is finite and non-empty, then \(H\) is a subgroup of \(G\) if and only if \(H\) is closed under the operation on \(G\).

---

The axiom for being non-empty \(H≠∅\) is already satisfied. In order to prove that \(H\) is a subgroup, we **need to prove the existence** of the identity element in \(H\). [@contemporary_abstract_algebra, pg. 64: Finite Subgroup Test]

Lets assume that \(H\) is **closed under operation**. Because \(H\) is non-empty it contains element \(a∈H\). If \(a=e\) there is nothing more to prove. If \(a≠e\), we consider a sequence of elements \(a, a^2, …\) which are all included in \(H\) by closure. Because the set is finite all the elements in the sequence cannot be distinct. Therefore there exists \(i>j\) such that \(a^i=a^j\) which implied \(a^{i-j}=e\). Because \(i-j>0\) then \(a^{i-j}∈H\) and therefore \(e∈H\).

<!-- Cayley table, finite, For all \(a∈H\) there exists \(b∈H\) such that \[a·b=e \\a^{-1}=b.\] -->


### b
Let the group \(G\) be \((ℤ,+,0)\). Then infinite subset \(H=(ℕ,+,0)\) of \(G\) is closed under the operation \(+\) on \(G\), but **not a subgroup** of \(G\) because its not **closed under inverse**, i.e. \(a∈H\) does not imply \(a^{-1}∈H\).


## Problem 4
Let \(G\) be a group. For \(g∈G\) define the *centralizer* \(C_G(g):=\{x∈G∣x·g=g·x\}\) of \(g\) in \(G\), and prove that \(C_G(g)\) is a subgroup for every \(g\).

---

**Nonempty**: For all \(g\), \[C_G(g)≠∅.\]

**Proof**: For every \(g\) if \(x=g\) then \[x⋅g=g·g=g·x\] therefore the centralizer always contains atleast the element \(g\).

**Closure under operation**: For all \(a,b∈C_G(g)\) \[a⋅b∈C_G(g)\]

**Proof**: Let \(a,b∈C_G(g)\) then \(a·g=g·a\) and \(b·g=g·b\). It can be shown that \(a·b\) belongs to \(C_G(g)\) if it satisfies the property \(x·g=g·x\).
\[
\begin{aligned}
(a·b)·g&=a·(b·g) \\
&=a·(g·b) \\
&=(a·g)·b \\
&=(g·a)·b \\
&=g·(a·b).
\end{aligned}
\]

**Closure under inverse**: For all \(a∈C_G(g)\) there exists \(a^{-1}∈C_G(g)\)

**Proof**: Let \(a∈C_G(g)\) then \(a·g=g·a\). It can shown that \(a^{-1}\) belongs to \(C_G(g)\) if it satisfies the property \(x·g=g·x\).
\[
\begin{aligned}
a^{-1}·g&=g·a^{-1} \\
a^{-1}·g·a&=g \\
g·a&=a·g \\
a·g&=g·a. \\
\end{aligned}
\]


## References
