
---
title: 圆曲线
taxon: definition
author: kokic
date: 2024-12-30
---

$\gdef\d{\operatorname{d}}$
$\gdef\arc{\text{arc}}$
$\gdef\Q{\mathbf{Q}}$

<!-- 对于某个平面代数曲线 $F(x,y)$ 所确定的轨迹 $X$, $X$-函数定义为 $X$ 的弧长积分 $\arc_X(x) = \int_0^x f(t)\d t$ 的反函数 $\wp_X(x)$, 如果 $\wp_X(x)$ 和 $\wp_X^\prime(x)$ 满足某个微分方程 $D_X$, 且 $D_X$ 在所有满足的微分方程中最简, 则称 $D_X$ 为 $X$-曲线.  -->

考虑半径为 $r$ 的实圆周 $x^2+y^2=r^2$，其在上半平面的轨迹可表为函数 $y=\sqrt{r^2-x^2},x\in[-r,r]$，[长度](/arc-length) 为 $$L=\int_{-r}^r\dfrac{r}{\sqrt{r^2-x^2}}\d x=r\arcsin\dfrac{x}{r}\bigg|_{-r}^r=\pi r$$ 因而圆的弧长定义了反正弦函数，即 $$\arcsin x=\int_0^x\dfrac{1}{\sqrt{1-t^2}}\d t$$ 其反函数被称为正弦函数，统称圆函数或者三角函数. 

现在, 注意到 $\cot(x)$ 和 $\cot^\prime(x)$ 满足   $\cot^2(x) + \cot^\prime(x) = 1$, 令 $(\cot(x), \cot^\prime(x)) \mapsto (x,y)$, 即 $y=c-x^2$. 

其他三角函数及其导数也有类似的关系, 以下列出.

$$\def\arraystretch{1.5}\begin{array}{|c|c|c|} 
\hline
u & (u, u^\prime) \mapsto (x,y) & g \\
\hline
\cot & y = -x^2-1 & 0 \\ 
\hline
\tan & y = x^2 + 1 & 0 \\ 
\hline
\cos, \sin & y^2 = 1-x^2 & 0 \\
\hline
\sec, \csc & y^2 = x^4-x^2 & 0 \\
\hline
\end{array}$$

<!-- 对于 $y^2 = x^4-x^2$, 这是曲线 $y=x^2+x$ 与 $y=x^2-x$ 的乘积.  -->



<!-- 
我们取它的一个根 $\alpha$, 任取 $\beta \in \Q^\times$ 例如 $1$. 做变换

$$ x = \frac{\beta}{t-\alpha}, \quad y = \frac{\beta^2u}{(t-\alpha)^2} \quad (= ~ x^2u) $$

现在计算 

$$ f(x) = g'(\alpha)\beta x^3 + \frac{g''(\alpha)}{2!}\beta^2 x^2 + \frac{g'''(\alpha)}{3!}\beta^3 x + \frac{g''''(\alpha)}{4!}\beta^4 $$ -->

<!-- 故将此类抛物线称为圆曲线.  -->
