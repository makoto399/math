```
Theorem 3.16
```

The Lebesgue measure space $(\mathbb{R}, \mathfrak{M}_L, \mu_L)$ is translation invariant, that is, for every $E \in \mathfrak{M}_L$ and $x\in\mathbb{R}$ we have

`1.`

$$
E + x \in \mathfrak{M}_L
$$

and

$$
\mu_L(E+x)
=
\mu_L(E).
$$

`2.`

For every $x \in \mathbb{R}$, let

$$
\mathfrak{M}_L + x
:=
\{ \ 
    E + x : E\in \mathfrak{M}_L    
\ \},
$$

then

$$
\mathfrak{M}_L + x
=
\mathfrak{M}_L.
$$

```
proof
```

`1.`

Let $\mu^*_L$ be Lebesgue outer measure.

For every $E\in \mathfrak{M}_L$, $x \in \mathbb{R}$, and $A\in\mathfrak{P}(R)$,

$$
\begin{aligned}
\mu^*_L&(A \cap (E+x))
+
\mu^*_L(A \cap (E+x)^c) \\
&=
\mu^*_L(A \cap (E+x))
+
\mu^*_L(A \cap (E^c + x))
\end{aligned}
$$

by the talnslation invariant of the Lebesgue outer measure,

$$
\begin{aligned}
&=
\mu^*_L((A \cap (E+x))-x)
+
\mu^*_L((A \cap (E^c + x))-x) \\
&=
\mu^*_L((A - x)\cap E)
+
\mu^*_L((A - x) \cap E^c) \\
\end{aligned}
$$

since measurability of $E$

$$
\begin{aligned}
&=
\mu^*_L(A - x),
\end{aligned}
$$

by the talnslation invariant of the Lebesgue outer measure,

$$
\begin{aligned}
=
\mu^*_L(A),
\end{aligned}
$$

then

$$
E + x \in \mathfrak{M}_L.
$$

Also by the talnslation invariant of the Lebesgue outer measure,

$$
\begin{aligned}
\mu_L(E+x)
&=
\mu^*_L(E+x) \\
&=
\mu^*_L(E) \\
&=
\mu_L(E) 
\end{aligned}
$$

Thus, we proved.

`2.`

It's easy to show by the same argument of `1.`.

