---
title: Abstract Algebra - Assignment 3
author: Jaan Tollander de Balsch
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
