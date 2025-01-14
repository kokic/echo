
---
title: Schanuel–Lavendhomme 构造
author: kokic
taxon: definition
date: 2024-11-18
---

$\gdef\quads#1{\quad #1 \quad}$
$\gdef\eqq{\quads=}$

Schanuel 和 Lavendhomme 给出了一个例子, 用于说明 [Kock--Lawvere 公理](/data-structure/kock-lawvere) 实际上与排中律矛盾. 定义一个 $D \to R$ 的函数如下

$$ 
g(d) = \begin{cases}
1 & \text{if} ~ d \neq 0 \\
0 & \text{if} ~ d = 0
\end{cases}
$$

如果 [Kock--Lawvere 公理](/data-structure/kock-lawvere) 成立, 则不可能有 $D = \{0\}$ [^impossible]. 因此我们可以 [使用排中律] 假设存在非零的 $d_0 \in D$, 由 [Kock--Lawvere 公理](/data-structure/kock-lawvere) 得

$$ 1 \eqq g(d_0) \eqq b d_0 + g(0) \eqq b d_0 $$

再两边平方, 有 $1 = 0$, 矛盾. 

[^impossible]: 尽管这个陈述是比较显然的, 不过我们还是说明一下, 这里在表达的是 $|D\smallsetminus\{0\}| > 0$ 这样的意思. 
