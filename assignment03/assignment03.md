---
title: Abstract Algebra - Assignment 3
author: Jaan Tollander de Balsch, 452056
date: \today
header-includes: \usepackage{unicode-math}
---
pg. 60

- order of a Group
- oder of an Element

pg. 66

- center of a group

## Problem 3
- centralizer?


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

TODO: contractition proof that \(n\) is the smallest positive integer and therefore the order.

TODO: \((a·b)^{-1}=b^{-1}·a^{-1}\) implies that \((a^n)^{-1}=(a^{-1})^n\)


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
