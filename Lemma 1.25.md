```
Lemma 1.25
```

A measure $\mu$ on a $\sigma$ - algebra of subsets of a set X has the following properties:

`1.`
Finite additivity:

If below is a set of mutually disjoint elements, 

$$
\{ \ E_n: E_n \in \mathfrak{A}, n \in \mathbb{N} \ \}
$$

we have

$$
\mu(
    \bigcup_{k=1}^n E_k
)
=
\sum_{k=1}^n
\mu(E_k).
$$


`2.`
Monotonicity:

For all $E_1$, $E_2 \in\mathfrak{A}$ such that

$$
E_1 \subset E_2,
$$

we have

$$
\mu(
    E_1
)
\leq
\mu(
    E_2
).
$$

`3.`

For all $E_1$, $E_2$ $\in \mathfrak{A}$ such that

$$
E_1 \subset E_2
$$

and

$$
\mu(E_1) < \infty,
$$

we have

$$
\mu(E_2 \backslash E_1)
=
\mu(E_2) - \mu(E_1).
$$

```
proof
```
`1.`
skip

`2.`
skip

`3.`

Since

$$
E_1 \subset E_2,
$$

we have

$$
E_2 = E_1 \bigcup (E_2 \backslash E_1).
$$

Thus

$$
\begin{aligned}
\mu(
    E_2
)
&=
\mu(E_1 \bigcup (E_2 \backslash E_1)) \\
&=
\mu(E_1) + \mu(E_2 \backslash E_1) \cdots (*).
\end{aligned}
$$

Since 

$$
\mu(E_1) < \infty,
$$

we substract $\mu(E_1)$ from both side of $(*)$,

then we have

$$
\mu(E_2 \backslash E_1)
=
\mu(E_2) - \mu(E_1).
$$

