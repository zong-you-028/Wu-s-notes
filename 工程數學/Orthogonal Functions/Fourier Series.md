標籤: #工程數學 

---

對於 [[Complete]] 且 [[Orthogonal]] 的 $\phi_n(x)$ ，我們可以用以下函數表達

> - [[#Trigonometric Functions]]
> - [[#Fourier Cosine and Sine Functions]]

# Trigonometric Functions

$$\{ 1,\  \cos\frac{ \pi }{ p }x,\  \cos \frac{ 2\pi }{ p }x,\  \cos\frac{ 3\pi }{ p }x,\  \dots,\  \sin\frac{ \pi }{ p }x,\  \sin\frac{ 2\pi }{ p }x,\  \sin\frac{ 3\pi }{ p }x,\  \dots \}$$

- [[Orthogonal Set]] on the interval of $[-p, \ p]$
- [[Complete]]
- 測量頻率的工具

## 證明

要證明是否是 [[Orthogonal Set]] ，需要將 $1$, $\cos$, $\sin$ 互相算出為 [[Orthogonal]]

(1) $1$ v.s. $\cos$

$$\int_{ -p }^{ p } 1\cdot \cos\frac{ \pi k }{ p }xdx$$

$$ = \left. \frac{ p }{ \pi k }\sin\frac{ \pi k }{ p }x \right\vert_{ -p }^{ p }$$

$$ = \frac{ p }{ \pi k }\sin\pi k - \frac{ p }{ \pi k }\sin(-\pi k)$$

$$ = 0$$

(2) $1$ v.s. $\sin$

$$\int_{ -p }^{ p } 1 \cdot \sin\frac{ \pi k }{ p }xdx$$

$$ = \left. -\frac{ p }{ \pi k }\cos\frac{ \pi k }{ p }x \right\vert_{ -p }^{ p }$$

$$ = -\frac{ p }{ \pi k }\cos \pi k + \frac{ p }{ \pi k } \cos (-\pi k)$$

$$ = 0$$

$1$ 是 even function, $\sin$ 是 odd function, 兩個一定 [[Orthogonal]]

(3) $\cos$ v.s. $\sin$

$$\int_{ -p }^{ p } \cos\frac{ \pi k }{ p }x\cdot \sin\frac{ \pi h }{ p }xdx$$

$$ = \int_{ -p }^{ p }\frac{ 1 }{ 2 }
\left[
\sin\frac{ \pi(h + k) }{ p }x - \sin\frac{ \pi (h - k) }{ p }x
\right]dx$$

$$
= \left. \frac{ p }{ 2\pi }
\left[
	-\frac{ 1 }{ h + k }
	\cos
	\left(
		\frac{ \pi(h + k)x }{ p }
	\right) + 
	\frac{ 1 }{ h - k }\cos
	\left(
		\frac{ \pi(h - k)x }{ p }
	\right)
\right] \right\vert_{ -p }^{ p }
$$

$$
= 
\frac{ p }{ 2\pi }
\left[
-\frac{ 1 }{ h + k }
\left[
\cos(\pi(h + k)) - \cos(-\pi(h + k))
\right] + \frac{ 1 }{ h - k }
\left[
\cos(\pi(h - k)) - \cos(-\pi(h - k))
\right]
\right]
$$

$$ = 0 \qquad (\text{ when } h \neq k)$$

$$\text{ when } h = k$$

$$\int_{ -p }^{ p }\cos\frac{ \pi k }{ p }x\cdot \sin\frac{ \pi h }{ p }xdx$$

$$ = \int_{ -p }^{ p }\frac{ 1 }{ 2 }\sin\frac{ 2\pi k }{ p }xdx$$

$$ = \left. -\frac{ p }{ 4\pi k }\cos\frac{ 2\pi k }{ p } \right\vert_{ -p }^{ p }$$

$$ = 0$$

$\cos$ 是 even function, $\sin$ 是 odd function, 兩者一定 [[Orthogonal]]

(4) $\cos$ v.s. $\cos$, $k \neq h$

$$\int_{ -p }^{ p }\cos\frac{ \pi k }{ p }x\cdot \cos\frac{ \pi h }{ p }xdx$$

$$ = \int_{ -p }^{ p }\frac{ 1 }{ 2 }\left[ \cos\frac{ \pi(h + k) }{ p }x + \cos\frac{ \pi(h - k) }{ p }x \right]dx$$

$$ = \left. \frac{ p }{ 2\pi }\left[ \frac{ 1 }{ h + k }\sin\left( \frac{ \pi(h + k)x }{ p } \right) + \frac{ 1 }{ h - k }\sin\left( \frac{ \pi(h - k)x }{ p } \right) \right] \right\vert_{ -p }^{ p }$$

$$ = \frac{ p }{ 2\pi }\left[ \frac{ 1 }{ h + k }[\sin(\pi(h + k)) - \sin(-\pi(h + k))] + \frac{ 1 }{ h + k }[\sin(\pi(h - k)) - \sin(-\pi(h - k))] \right]$$

$$ = 0 \qquad \text{ when } h \neq k $$

(5) $\sin$ v.s. $\sin$, $k \neq h$

$$\int_{ -p }^{ p }\sin\frac{ \pi k }{ p }x \cdot \sin\frac{ \pi h }{ p }xdx$$

$$ = \int_{ -p }^{ p }\frac{ 1 }{ 2 }\left[ \cos\frac{ \pi(h - k) }{ p }x - \cos\frac{ \pi(h + k) }{ p }x \right]dx$$

$$ = \left. \frac{ p }{ 2\pi }\left[ \frac{ 1 }{ h - k }\sin\left( \frac{ \pi(h - k)x }{ p } \right) - \frac{ 1 }{ h + k }\sin\left( \frac{ \pi(h + k)x }{ p } \right) \right] \right\vert_{ -p }^{ p }$$
  
$$ = 0 \qquad (\text{ when } h \neq k )$$

## Fourier Series

$$f(x) \cong \frac{ a_0 }{ 2 } + \sum_{ n = 1 }^{ \infty }\left( 
a_n\cos\frac{ n\pi }{ p }x + b_n\sin\frac{ n\pi }{ p }x \right)$$

$$a_0 = \frac{ 1 }{ p }\int_{ -p }^{ p }f(x)dx$$

$$a_n = \frac{ 1 }{ p }\int_{ -p }^{ p }f(x)\cos\frac{ n\pi }{ p }xdx$$

$$b_n = \frac{ 1 }{ p }\int_{ -p }^{ p }f(x)\sin\frac{ n\pi }{ p }xdx$$

上述的 $f(x)$ 是近似，原因是 [[#Condition for Converge]] , [[#Period Extension]]

## 頻率與週期

對於每個 $\cos\frac{ n\pi }{ p }x$
週期: $\frac{ 2p }{ n }$
頻率: $\frac{ n }{ 2p }$

## 例題

> $$f(x) = \left\{ \begin{array}{} 0 & \text{ for } & -\pi < x < 0 \\ \pi - x & \text{ for } & 0 \leq x < \pi \end{array} \right.$$

$p = \pi$ 帶入公式

$$a_0 = \frac{ 1 }{ \pi }\int_{ -\pi }^{ \pi }f(x)dx$$

$$ = \frac{ 1 }{ \pi }(\pi - x)dx = \frac{ \pi }{ 2 }$$

$$a_n = \frac{ 1 }{ \pi }\int_{ -\pi }^{ \pi }f(x)\cos nxdx$$

$$ = \frac{ 1 }{ \pi }\int_0^\pi (\pi - x)\cos nx dx$$

$$ = \left. \frac{ \pi - x }{ \pi }\frac{ 1 }{ n }\sin nx \right\vert_{ 
0 }^{ \pi } - \frac{ 1 }{ \pi }\int_0^\pi (-1)\frac{ 1 }{ n }\sin nx dx$$

$$ = \left.-\frac{ 1 }{ n^2\pi }\cos nx \right\vert_0^\pi$$

$$ = \frac{ 1 - \cos n\pi }{ n^2\pi } \qquad (\cos n\pi = (-1)^n)$$

$$ = \frac{ 1 - (-1)^n }{ n^2 \pi }$$

$$b_n = \frac{ 1 }{ \pi }\int_{ -\pi }^{ \pi }f(x)\sin nxdx$$

$$ = \frac{ 1 }{ \pi }\int_0^\pi (\pi - x)\sin nxdx$$

$$ = \left. \frac{ \pi - x }{ \pi }\frac{ 1 }{ n }\cos nx \right\vert_0^\pi - \frac{ 1 }{ \pi }\int_0^\pi(-1)(-\frac{ 1 }{ n }\cos nx)dx$$

$$ = \frac{ 1 }{ n } - \left. \frac{ 1 }{ n^2\pi }\sin nx \right\vert_0^\pi$$

$$ = \frac{ 1 }{ n }$$

$$f(x) = \frac{ \pi }{ 4 } + \sum_{ n = 1 }^{ \infty }\left( \frac{ 1 - (-1)^n }{ n^2\pi }\cos\frac{ n\pi }{ p }x + \frac{ 1 }{ n }\sin\frac{ n\pi }{ p }x \right)$$

## Condition for Converge

$$f(x) = \frac{ a_0 }{ 2 } + \sum_{ n = 1 }^{ \infty }\left( 
a_n\cos\frac{ n\pi }{ p }x + b_n\sin\frac{ n\pi }{ p }x \right) \qquad \text{ 其實未必成立 }$$

$$a_0 = \frac{ 1 }{ p }\int_{ -p }^{ p }f(x)dx$$

$$a_n = \frac{ 1 }{ p }\int_{ -p }^{ p }f(x)\cos\frac{ n\pi }{ p }xdx$$

$$b_n = \frac{ 1 }{ p }\int_{ -p }^{ p }f(x)\sin\frac{ n\pi }{ p }xdx$$

若 $f_1(x)$ 為依上述方法轉換結果
$f(x)$ 為原式

1. $f_1(x_0) = f(x_0) \qquad \text{ if } f(x) \text{ is continuous at } x_0$ 
2. $f_1(x_0) = \frac{ f(x_{ 0+ }) + f(x_{ 0- }) }{ 2 } \text{ if } f(x) \text{ is not continuous at } x_0$
$f(x_{ 0+ })$: 趨近 $x_0$ 但大於 $x_0$ 的 $f(x)$
$f(x_{ 0- })$: 趨近 $x_0$ 但小於 $x_0$ 的 $f(x)$

## Period Extension

若 $f_1(x)$ 是週期為 $2\pi$ 的函式

$$f_1(x + 2p) = f_1(x)$$

因此對一個非週期的函式， Fourier Series Expansion 的結果不適用於 $x \notin [-p, p]$ 的區域。但是週期函式則可以。

### 證明

$$f_1(x) = \frac{ a_0 }{ 2 } + \sum_{ n = 1 }^{ \infty }\left( a_n\cos\frac{ n\pi }{ p }x + b_n\sin\frac{ n\pi }{ p }x  \right) \qquad \text{ fundamental period: } 2p$$

在 interval $x \in [-p, p]$ 以外的地方

$$f_1(x + 2p) = \frac{ a_0 }{ 2 } + \sum_{ n = 1 }^{ \infty }\left( 
a_n\cos(\frac{ n\pi }{ p }x + 2n\pi) + b_n\sin( \frac{ n\pi }{ p }x + 2n\pi ) \right)$$

$$\underline{ f_1(x + 2p) = f(x) }_{ \# }$$

# Fourier Cosine and Sine Functions

與 [[#Trigonometric Functions]] 很像，只是限制更多
$f(x)$ 限制為 even 或 odd

## Fourier Cosine Series

$$f(x) = \frac{ a_0 }{ 2 } + \sum_{ n = 1 }^{ \infty }a_n\cos\frac{ n\pi }{ p }x$$

$$a_0 = \frac{ 2 }{ p }\int_0^p f(x)dx$$

$$a_n = \frac{ 2 }{ p }\int_0^p f(x)\cos\frac{ n\pi }{ p }xdx$$

### 差異

1. 少了 $\sin$
2. $\int_{ -p }^{ p } \rightarrow \int_0^p$
3. $\frac{ 1 }{ p } \rightarrow \frac{ 2 }{ p }$

因為是 even function ，因此可以縮小積分範圍，然後 $\times 2$

## Fourier Sine Series

$$f(x) = \sum_{ n = 1 }^{ \infty }b_n\sin\frac{ n\pi }{ p }x$$

$$b_n = \frac{ 2 }{ p }\int_0^p f(x)\sin\frac{ n\pi }{ p }xdx$$

### 差異

1. 少了 $1, \cos$
2. $\int_{ -p }^{ p } \rightarrow \int_0^p$
3. $\frac{ 1 }{ p } \rightarrow \frac{ 2 }{ p }$

因為 odd funciton 和 odd function 相乘是 even function ，因此可以縮小積分範圍，然後 $\times 2$

## 例題

> Expand $$f(x) = x, \quad -2 < x < 2$$ in a fourier series

$f(x)$ is odd
$\therefore$ expand $f(x)$ by a sine series

$$b_n = \frac{ 2 }{ 2 }\int_0^2 x\sin\frac{ nx }{ 2 }xdx$$

$$ = \left. -\frac{ 2 }{ n\pi }x\cos\frac{ n\pi }{ 2 }x \right\vert_0^2 + \frac{ 2 }{ n\pi }\int_0^2\cos\frac{ n\pi }{ 2 }xdx$$

$$ = -\frac{ 2 }{ n\pi }2\cos n\pi + 0 + \left. \frac{ 4 }{ n^2\pi^2 }\sin\frac{ n\pi }{ 2 }x \right\vert_0^2$$

$$ = -\frac{ 4 }{ n\pi }(-1)^n + 0 - 0$$

$$ = \frac{ 4 }{ n\pi }(-1)^{ n + 1 }$$

$$f(x) = \sum_{ n = 1 }^{ \infty } \frac{ 4(-1)^{ n + 1 } }{ n\pi }\sin\frac{ n \pi }{ 2 }x$$

---

參考資料:

[[微分方程]第25講、Sections 11-2 and 11-3 Fourier Series, Fourier Cosine and Sine Series](https://youtu.be/Yrg5hIHcbn4)

---

link:

[[Generalized Fourier Series]]