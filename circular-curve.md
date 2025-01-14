
---
title: 圆曲线
taxon: definition
author: kokic
date: 2024-12-30
---

$\gdef\quads#1{\quad #1 \quad}$
$\gdef\eqq{\quads=}$
$\gdef\d{\operatorname{d}}$
$\gdef\E{\operatorname{E}}$
$\gdef\arc{\text{arc}}$
$\gdef\R{\mathbf{R}}$
$\gdef\Q{\mathbf{Q}}$

考虑半径为 $r$ 的实圆周 $x^2+y^2=r^2$，其在上半平面的轨迹可表为函数 $y=\sqrt{r^2-x^2},x\in[-r,r]$，[长度](/arc-length) 为 

$$
L 
\eqq \int_{-r}^r\dfrac{r}{\sqrt{r^2-x^2}}\d x
\eqq r\arcsin\dfrac{x}{r}\bigg|_{-r}^r
\eqq\pi r
$$ 

因而圆的弧长定义了反正弦函数，即 

$$
\arcsin x \eqq \int_0^x\dfrac{1}{\sqrt{1-t^2}}\d t
$$ 

其反函数被称为正弦函数，统称圆函数或者三角函数. 

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

现在取 $C(\Q): y=x^2+1$ 上一定点 $(0, 1)$, 固定斜率 $t$ 从而有直线 $\ell(\Q): y=tx+1$, 类似地求曲线 $\ell(\Q) \cdot C(\Q) = 0$ 的交点, 得到 $(t, t^2+1)$.  

如果我们对抛物线 $C(\R)$ 求弧长, 所得到的将是 $\log$ 或 $\sinh^{-1}$ 的代数函数. 当然, $\sinh^{-1}$ 实际上也是 $\log$ 的代数函数. 
$$
\begin{aligned} 
s
&\eqq \int\sqrt{1+(2x)^2}\d x \\
&\eqq \frac12 \sqrt{1+4x^2} + \frac14\sinh^{-1}(2x)
\end{aligned}
$$

现在重新回顾 

$$
\int\dfrac{\d x}{y}, \quad y = \sqrt{r^2-x^2}
$$ 

积分号内的项是 $x,y$ 的有理函数, $y$ 是 $x$ 的代数函数, 同时我们已经知道 $x,y$ 满足的代数方程有一个 [有理参数化](/circular-parameterization), 也就是说

$$
\begin{aligned}
\int\dfrac{\d x}{y} 
&\eqq \int \frac{\d{(\frac{1-t^2}{1+t^2})}}{\frac{2t}{1+t^2}} \\
&\eqq \int -\frac{4t}{(1+t^2)^2} \cdot \frac{1+t^2}{2t} \d t \\
&\eqq \int -\frac{2}{1+t^2} \d t \\
&\eqq -2\tan^{-1} t
\end{aligned}
$$

另一方面, 我们知道 $t = \pm\frac{\sqrt{1-x}}{\sqrt{1+x}}$. 这就意味着 $\arcsin x$ 和 $-2\tan^{-1} t$ 之间最多只相差一个常数, 容易计算这个常数正是 $\frac{\pi}2$, 则有

$$
\arcsin x \eqq \frac{\pi}2-2\arctan\frac{\sqrt{1-x}}{\sqrt{1+x}}
$$

双曲线时的情况略有不同. 考虑 $C(\R):x^2-y^2=1$, 如果朴素地计算平面直角坐标系上的积分, 将得到一个会被归类为椭圆积分的表达式

$$ 
\int \sqrt{\frac{2x^2-1}{x^2-1}} \d x 
\eqq \int \frac{4x^4-1}{\sqrt{x^2-1}\sqrt{2x^2+1}} \d x
$$

由于分子部分的 $4x^4-1$ 是多项式函数, 因此整个积分的核心就在于下面这一项 

$$
\int \frac1{\sqrt{(x^2-1)(2x^2+1)}} \d x
\tag{1}
$$

[椭圆积分的经验](/elliptic-integral) 很容易让我们认为最后的结果当中势必会出现 [椭圆函数](/elliptic-functions). 事实正是如此, 注意这个时候 $y^2 = (x^2-1)(2x^2+1)$ 的 $g$ 是 $1$, 而且实际上在引入椭圆函数后, $(1)$ 的表达式要远比弧长的表达式复杂. 

现在考虑双曲线 $C(\R)$ 的一个参数化 
$$ (x,y) \quads\mapsto (\cosh t, \sinh t) $$ 

相应的, 关于 $x \in [a,b]$ 弧长积分变为 $t \in [\cosh^{-1}a, \cosh^{-1}b]$ 的积分 

$$
\begin{aligned}
\int \sqrt{\sinh^2 t + \cosh^2 t} \d t
&\eqq \int \sqrt{\cosh 2t} \d t \\
&\eqq -i \E(it \mid 2) \\
&\eqq -i \E(i \cosh^{-1}x \mid 2) \\
&\eqq \E(\sin^{-1}x \mid 2) \\
\end{aligned}
$$ 
