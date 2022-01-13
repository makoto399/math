```
Theorem 1.44.
```
Given two measurable spaces $(X, \mathfrak{A})$ and $(Y, \mathfrak{B})$.

Let $f$ be a $\mathfrak{A}/\mathfrak{B}$ - measurable mapping of $X$ into $Y$.

Let $\mu$ be a measure on $\mathfrak{A}$.

The set function defined by $v=\mu \circ f^{-1}$ on $\mathfrak{B}$, that is, $v(B)=\mu(f^{-1}(B))$ for $B \in \mathfrak{B}$, is a measure on $\mathfrak{B}$.

```
proof
```

First,
by the positiveness of $\mu$, so is $v$.

Second,

$$
\begin{aligned}
v(\emptyset)
&=
\mu(f^{-1}(\emptyset)) \\ 
&=
\mu(\emptyset) \\
&=
0.
\end{aligned}
$$

Third, let

$$
\{ \ 
    B_n \in \mathfrak{B}: n \in \mathbb{N}
\ \}
$$

be such that for any $m,n\in \mathbb{N}$

$$
B_n \cap B_m = \emptyset.
$$

Then

$$
\begin{aligned}
v(
    \bigsqcup_{n\in\mathbb{N}}
    B_n
)
&=
\mu(
    f^{-1}(
       \bigsqcup_{n\in\mathbb{N}}
       B_n 
    )
) \\
&=
\mu(
    \bigsqcup_{n\in\mathbb{N}}
        f^{-1}(
            B_n 
    )
) \\
&=
\sum_{n\in\mathbb{N}}
\mu(f^{-1}(B_n)) \\
&=
\sum_{n\in\mathbb{N}}
v(B_n).
\end{aligned}
$$

Thus $\mu$ is a measure.


