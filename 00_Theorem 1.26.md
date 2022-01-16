```
Theorem 1.26
```

Let $\mu$ be a measure on a $\sigma$-algebra $\mathfrak{A}$ of subsetes of a set $X$ and let $(E_n: n \in \mathbb{N})$ be a monotone sequence in $\mathfrak{A}.$

`1.`

If $E_n \uparrow$, then
$$
\lim_{n\rightarrow \infty} \mu (E_n)
=
\mu (\lim_{n\rightarrow \infty} E_n)
$$

`2`.

If $E_n \downarrow$, then
$$
\lim_{n\rightarrow \infty} \mu (E_n)
=
\mu (\lim_{n\rightarrow \infty} E_n),
$$

provided that there exists a set $X \in \mathfrak{A}$ with $\mu(A)<\infty$ such that $E_1\subset A.$


```
proof
```

`1.`

First,
consider there exists $n_0$ such that

$$
\mu(E_{n_0})=\infty.
$$

By the increasing monotonicity of

$$
\{ \ \mu(E_n): n \in \mathbb{N} \ \},
$$

we have

$$
\lim_{n\rightarrow \infty}
\mu(E_n)=\infty.
$$

Since
<!-- increasing monotonicity of -->
<!-- 
$$
\{
    \ E_n: n\in \mathbb{N} \   
\},
$$

we have -->

$$
E_{n_0}
\subset
\bigcup_{n \in \mathbb{N}}
E_n,
$$

<!-- and by the monotonicity of $\mu$, -->
we have


$$
\begin{aligned}
\infty
&= \mu(E_{n_0}) \\
&\leq
\mu( 
    \bigcup_{n \in \mathbb{N}} E_n
) \\
&=
\mu (\lim_{n\rightarrow \infty} E_n).
\end{aligned}
$$

Thus

$$
\lim_{n\rightarrow \infty} \mu (E_n)
=
\mu (\lim_{n\rightarrow \infty} E_n).
$$

Second, consider the case for any $n\in\mathbb{N}$

$$
\mu(
    E_n
)
<
\infty.
$$

We define for any $n \in \mathbb{N}$

<!-- $$
\{ \ 
    F_n: n \in \mathbb{N}
\ \}
$$

such that -->

$$
F_n
:=
E_n \backslash E_{n-1}
$$

with

$$
E_0 = \emptyset,
$$

then

$$
\bigcup_{n\in \mathbb{N}}
E_n
=
\bigsqcup_{n\in \mathbb{N}}
F_n.
$$

Thus

$$
\begin{aligned}
\mu(
    \bigcup_{n \in \mathbb{N}}
    E_n
)
&=
\mu(
    \bigsqcup_{n \in \mathbb{N}}
    F_n
) \\
&=
\sum_{n \in \mathbb{N}}
\mu(
    F_n
) \\
&=
\sum_{n \in \mathbb{N}}
\mu(
    E_n \backslash E_{n-1} 
)
\cdots \ 
(*).
\end{aligned}
$$

By the fact that for any $n\in \mathbb{N}$

$$
\mu(E_n) < \infty,
$$

and `Lemma 1.25`,

<!-- $$
\mu(
    E_n \backslash E_{n-1} 
)
=
\mu(E_n)
-
\mu(E_{n-1})
,
$$

which is shown in , -->

we have

$$
\begin{aligned}
(*)
&=
\sum_{n \in \mathbb{N}}
\mu(E_n)
-
\mu(E_{n-1}) \\
&=
\lim_{n\rightarrow \infty}
\mu(E_n)
-
\mu(E_0) \\
&=
\lim_{n\rightarrow \infty}
\mu(E_n).
\end{aligned}
$$

Thus we proved.

`2.`

We define for any $n \in \mathbb{N}$

$$
F_n
:=
E_n \backslash E_{n+1},
$$

then

$$
\bigcap_{n \in \mathbb{N}}
E_n
=
E_1
\backslash
(
    \bigsqcup_{n \in \mathbb{N}}
    F_n
).
$$

Thus

$$
\begin{aligned}
\mu(
    \lim_{n \rightarrow \infty}
    E_n
)
&=
\mu(
    \bigcap_{n \in \mathbb{N}}
    E_n
) \\
&=
\mu(
    E_1
    \backslash
    (
        \bigsqcup_{n \in \mathbb{N}}
        F_n
    )
)\cdots (*).
\end{aligned}
$$

By the fact that

$$
\mu(
    \bigsqcup_{n\in\mathbb{N}}
    F_n
)
<
\infty
$$

and `Lemma 1.25`, same as `1.`,
<!-- $$
\mu(
    E_1
    \backslash
    (
        \bigsqcup_{n \in \mathbb{N}}
        F_n
    )
) 
=
\mu(
    E_1
)
-
\mu(
    \bigsqcup_{n \in \mathbb{N}}
    F_n
),
$$ -->

we have

$$
\begin{aligned}
(*)
&=
\mu(
    E_1
)
-
\mu(
    \bigsqcup_{n \in \mathbb{N}}
    F_n
) \\
&=
\mu(
    E_1
)
-
\sum_{n \in \mathbb{N}}
\mu(F_n) \\
&=
\mu(
    E_1
)
-
\sum_{n \in \mathbb{N}}
\mu(E_n\backslash E_{n-1})\cdots (*).
\end{aligned}
$$

Also by the fact that for any $n \in \mathbb{N}$

$$
\mu(E_n) < \infty
$$

and `Lemma 1.25`, same as `1.`,
<!-- $$
\mu(
    E_n
    \backslash
    E_{n-1}
) 
=
\mu(
    E_n
)
-
\mu(
    E_{n-1}
),
$$ -->

we have

$$
\begin{aligned}
(*)
&=
\mu(
    E_1
)
-
\sum_{n \in \mathbb{N}}
\mu(E_n)
-
\mu(E_{n-1}) \\
&=
\mu(
    E_1
)
-
\lim_{n \rightarrow \infty}
\sum_{k =1}^{n}
\mu(E_k)
-
\mu(E_{k-1}) \\
&=
\mu(
    E_1
)
-
\lim_{n \rightarrow \infty}(
    \mu(E_1)
    -
    \mu(E_n)
) \cdots (*).
\end{aligned}
$$

Since

$$
\mu(E_1) < \infty,
$$

we have

$$
\begin{aligned}
(*)
&=
\mu(
    E_1
)
-
(
    \mu(E_1)
    -
    \lim_{n \rightarrow \infty}
    \mu(E_n)
) \\
&=
\lim_{n \rightarrow \infty}
    \mu(E_n).
\end{aligned}
$$

Thus we proved.