標籤: #工程數學 

---

對於 [[Complete]] 且 [[Orthogonal]] 的 $\phi_n(x)$ ，我們可以用以下函數表達

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

---

參考資料:

[[微分方程]第25講、Sections 11-2 and 11-3 Fourier Series, Fourier Cosine and Sine Series](https://youtu.be/Yrg5hIHcbn4)

---

link:

[[Generalized Fourier Series]]