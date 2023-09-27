Let $X$ and $Y$ be sets, and let $\mathcal{X}:=(X,d_X)$ and $\mathcal{Y}:=(Y,d_Y)$ be metric spaces, respectively.
Suppose $\mathcal{P}(X)$ and $\mathcal{P}(Y)$ be sets of all discrete distributions with finite support such that

$$\begin{aligned}
\mathcal{P}(X)&:= \left\{
    \alpha:=\sum_{i\in [n]}a_{x_i} \delta_{x_i}
    \left| \space \sum_{i \in [n]}a_{x_i}=1, x_i \in X {\rm \space and \space} a_{x_i}(\neq 0)\in \mathbb{R}_+ \space \forall i \in [n], n\in \mathbb{N}
\right. \right\}  \\
\mathcal{P}(Y)&:= \left\{
    \beta:=\sum_{i\in [n]}b_{y_i} \delta_{y_i}
    \left| \space \sum_{i \in [n]}b_{y_i}=1, y_i \in Y {\rm \space and \space} b_{y_i}(\neq 0)\in \mathbb{R}_+ \space \forall i \in [n], n\in \mathbb{N}
\right. \right\}.
\end{aligned}$$

For $\alpha \in \mathcal{P}(X)$ and $\beta \in \mathcal{P}(Y)$, if there exists a bijection $f:X\rightarrow Y$ such that

$$
a_{x_i} = b_{f(x_i)}
$$

and

$$
d_X(x_i, x_j) = d_Y\left(f(x_i), f(y_j)\right),
$$

then we call $\alpha$ and $\beta$ are isormophic.

と解釈しました。つまり、教科書の
$$
f:\{x_1,\cdots ,x_n\} \rightarrow \{y_1,\cdots ,y_m\}
$$

は本当は

$$
f:X\rightarrow Y
$$

と書くのが正しいんだけど、分布に寄与する有限個の$\{x_i\}_{i\in[n]}$と$\{y_i\}_{i\in[m]}$以外のところはどういう対応関係でも良い（$f$が全単射であることさえ満たされていれば）から、良かれと思ってこういう書き方になっちゃったんじゃないかと。あれ？そうなると$X$と$Y$の濃度は一致することになるけど、９章の冒頭で出てきた$\mathcal{X}=\{猫、犬、島\}$とかの例を見ると要素の数は一致してなくない？と思うかもだけど、その場合も例えば$\mathcal{X}$に適当に元を追加してその確率を0として要素の数を揃えて考えちゃえば本質は外れないということではないでしょうか（←表現自信ない）。もっというと、引数が異なれば$f$は違うところに飛んでほしいという単射の部分が重要なのであって、全射であることは実はそんなに本質ではない気がする。一方で、別の文脈で、全単射にしないと逆写像を考えられなくなってそうすると将来的に不都合が出てくる？から全単射を要請しているとかかな。