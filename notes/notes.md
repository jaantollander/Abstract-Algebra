## Definitions
A **group** is a triple \((G,·,e)\) where \(G\) is a set, \(·\) is a binary operation on \(G\) and the indentity \(e\), such that the following hold

a) **Closure**: For all \(x,y∈G\) the result operation \[x·y∈G.\]
b) **Associativity**: For all  \(x,y,z∈G\), \[(x·y)·z=x·(y·z).\]
c) **Indentity element**: There exists an identity element \(e\) such that for all \(x∈G\) \[e·x=x·e=x.\]
d) **Inverse element**: For every \(x∈G\) there exists \(y∈G\) such that \[x·y=y·x=e.\]

**Semigroup**: Only (a), (b) holds.

**Monoid** Only (a), (b), and \c) hold.

\(G\) is called **Abelian group** if the following also holds

d) **Commutativity**: For all \(x,y∈G\) we have \(x·y=y·x\).

---

Let \(G\) be a group and \(∅=H⊆G\) a subset of \(G\). We say \(H\) is a **subgroup** of \(G\), formally \(H⊆G\), it is closed under the operation on \(G\) and satisfies all group axioms.

A subset \(H\) of a group \(G\) is a subgroup, if and only if the following hold

a) **Nonempty**: The subgroup is non-empty \(H≠∅\).
b) **Closed under operation**: For all \(a,b∈H\) \[a·b∈H.\]
c) **Closed under inverse**: For all \(a∈H\) \[a^{-1}∈H.\]

Alternatively

I) \(H≠∅\)
II) \(a,b∈H\) implies \(a·b^{-1}∈H\).

---

For a group \(G\) and a subset \(T⊆G\) define
\[
⟨T⟩:=⋂\{H⊆G∣T⊆H\},
\]
the intersection of all subgroups that contain \(T\).

---

- [Group](https://en.wikipedia.org/wiki/Group_(mathematics))
- [Subgroup](https://en.wikipedia.org/wiki/Subgroup)
- [Cayley table](https://en.wikipedia.org/wiki/Cayley_table)
