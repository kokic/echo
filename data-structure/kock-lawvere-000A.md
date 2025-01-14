---
title: 所有函数都光滑
author: kokic
taxon: corollary
date: 2024-5-13
---

$\gdef\quads#1{\quad #1 \quad}$
$\gdef\eqq{\quads=}$

对任意函数 $f:R \rightarrow R$, 存在唯一的函数 $f':R \rightarrow R$ 满足

$$
f(x + \varepsilon) \eqq f(x) + f'(x)\varepsilon,\quad \forall ~ x \in R, ~ \forall ~ \varepsilon \in D
$$

这个一般认为是 [Kock--Lawvere 公理](/data-structure/kock-lawvere) 的推论, 不过从 $\mathcal{E}$ 的定义来看, 这才是整套框架真正的目的之一. 或者说, 是为了恢复牛顿时期 "幂零无穷小量" 计算上的直观. 

[](/data-structure/kock-lawvere-0001.typ#:block)
