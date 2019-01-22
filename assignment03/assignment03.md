---
title: Abstract Algebra - Assignment 3
author: Jaan Tollander de Balsch, 452056
date: \today
header-includes: \usepackage{unicode-math}
---
TODO: references

* pg. 60, terminology and notation
* pg. 63, subgroup tests
* [@contemporary_abstract_algebra]


## Problem 3
Let \(G\) be a group and let \(H\) and \(K\) be subgroups of \(G\). Show that the set \(HK:=\{h·k∣h∈H,k∈K\}\) is a subgroup of \(G\) if and only if \(HK=KH.\)

---

In order to prove that \(HK\) is a subgroup of \(G\) if only only if \(HK=KH\) it needs to satisfy the subgroup test. In this case we will be using the **Two-Step Subgroup Test**. The subset \(HK\) is **nonempty** because subsets \(H\) and \(K\) are non-empty.

**Closure under operation**: For all \(a,b∈HK\) implies \(a·b∈HK\).

1) Let \(a=h_1·k_1\) and \(b=h_2·k_2\) where \(h_1,h_2∈H\) and \(k_1,k_2∈K\).
2) The definition of \(HK\) implies that \(h_1·k_1∈H\) and \(h_2·k_2∈K\).
3) A further implication is that
\(h_1,k_1∈H\) and \(h_2,k_2∈K\).
4) Therefore all \(h∈H\) must be in \(K\) and all \(k∈K\) must be in \(H\) for \(HK\) to be a subgroup of \(G\).

**Closure under inverse**: For all \(a∈HK\) implies \(a^{-1}∈HK\).

1) Let \(a=h·k\) where \(h∈H\) and \(k∈K\).
2) Then \((h·k)^{-1}∈HK\).
3) Equivalently \(k^{-1}·h^{-1}∈HK\).
4) Definition of \(HK\) implies \(k^{-1}∈H\) and \(h^{-1}∈K\).
5) Therefore all inverses of \(h∈H\) must be in \(K\) and all inverses of \(k∈K\) must be in \(H\) for \(HK\) to be a subgroup of \(G\).

For \(HK\) to be a subgroup of \(G\), subgroups \(H\) and \(K\) must be equivalent, and therefore \(HK=KH\).


## Problem 4
Let \(GL_2(ℝ)\) denote the group of all invertible \(2×2\)-matrices with real entries. Let
\[
A:=\left[\begin{matrix}1 & 1\\0 & 1\end{matrix}\right]
\text{   and   }
B:=\left[\begin{matrix}0 & -1\\1 & 0\end{matrix}\right]
\]

### (a)
Show that \(A\) and \(B\) are indeed invertible, and determine their order.

---

The inverses of \(A\) and \(B\) are
\[
A^{-1}=\left[\begin{matrix}1 & -1\\0 & 1\end{matrix}\right]
\]
and
\[
B^{-1}=\left[\begin{matrix}0 & 1\\-1 & 0\end{matrix}\right].
\]

The order of \(A\) is infinite because there does not exist \(n∈ℕ\) such that \(A^n=I\)
\[
A^{n}=\left[\begin{matrix}1 & n\\0 & 1\end{matrix}\right].
\]

The sequence \(B^1,B^2,B^3,B^4,B^5,...\)
\[
\left ( \left[\begin{matrix}0 & -1\\1 & 0\end{matrix}\right], \quad \left[\begin{matrix}-1 & 0\\0 & -1\end{matrix}\right], \quad \left[\begin{matrix}0 & 1\\-1 & 0\end{matrix}\right], \quad \left[\begin{matrix}1 & 0\\0 & 1\end{matrix}\right], \quad \left[\begin{matrix}0 & -1\\1 & 0\end{matrix}\right], ...\right )
\]

The order of \(B\) is \(4\) because
\[
B^4=I.
\]


### (b)
Compute the product \(A⋅B\) and determine its order. What is your conclusion?

---

The product \(A⋅B\)
\[
A⋅B=\left[\begin{matrix}1 & -1\\1 & 0\end{matrix}\right]
\]

The sequence \((A⋅B)^1,(A⋅B)^2…,(A⋅B)^7,…\)
\[
\left ( \left[\begin{matrix}1 & -1\\1 & 0\end{matrix}\right], \quad \left[\begin{matrix}0 & -1\\1 & -1\end{matrix}\right], \quad \left[\begin{matrix}-1 & 0\\0 & -1\end{matrix}\right], \quad \left[\begin{matrix}-1 & 1\\-1 & 0\end{matrix}\right], \quad \left[\begin{matrix}0 & 1\\-1 & 1\end{matrix}\right], \quad \left[\begin{matrix}1 & 0\\0 & 1\end{matrix}\right], \quad \left[\begin{matrix}1 & -1\\1 & 0\end{matrix}\right],…\right )
\]

The order of \(A⋅B\) is \(6\)
\[
(A⋅B)^6=I
\]


## Problem 5
Let \(a,b,\) and \(c\) be elements in a group \(G\).

### (a)
Show that \(a\) and \(a^{-1}\) have the same order.

---

Let the order of the element \(a\) be the smallest positive integer \(n\) such that
\[
\begin{aligned}
a^n &= e \\
(a^n)^{-1} &= e \\
(a^{-1})^{n} &= e.
\end{aligned}
\]

This implies that the order of \(a^{-1}\) is also \(n\).

* TODO: infinite order case
* TODO: contractition proof that \(n\) is the smallest positive integer and therefore the order.
* TODO: \((a·b)^{-1}=b^{-1}·a^{-1}\) implies that \((a^n)^{-1}=(a^{-1})^n\)


### (b)
Show that \(b^{-1}·a·b\) and \(a\) have the same order.

---

Let the order of the element \(b^{-1}·a·b\) be the smallest positive integer \(n\) such that
\[
\begin{aligned}
(b^{-1}·a·b)^n&=e \\
(b^{-1}·a·b)·(b^{-1}·a·b)·...·(b^{-1}·a·b)&=e \\
b^{-1}·a·(b·b^{-1})·a·(b·b^{-1})·...·(b·b^{-1})·a·b&=e \\
b^{-1}·a^n·b&=e \\
a^n&=b·e·b^{-1} \\
a^n&=e.
\end{aligned}
\]
This implies that the order of element \(a\) is also \(n\).


### (c)
Using (b), show that \(a·b\) and \(b·a\) have the same order. Deduce from this, that \(a·b·c\) and \(b·c·a\) have the same order.

---

Let the order of the element \(a·b\) be the smallest positive integer \(n\) such that
\[
\begin{aligned}
(a·b)^n&=e \\
a·(b·a)^{n-1}·b&=e \\
a·(b·a)^{n-1}&=e·b^{-1} \\
a·(b·a)^{n-1}&=b^{-1}·e \\
(b·a)·(b·a)^{n-1}&=e \\
(b·a)^n&=e
\end{aligned}
\]
This implies that the order of element \(b·a\) is also \(n\). Using this property, we can also prove that the order of element \(a·b·c\) is the same as the order of element \(b·c·a\)
\[
\begin{aligned}
(a·b·c)^n&=e \\
(a·b')^n&=e, b'=b·c \\
(b'·a)^n&=e \\
(b·c·a)^{n}&=e.
\end{aligned}
\]


## References
