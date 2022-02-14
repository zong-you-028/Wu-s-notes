標籤: #工程數學 

---

> - [[#Fourier Integral]]
> - [[#Complex Form or Exponential Form of Fourier Integral]]
> - [[#Fourier Cosine Integral]]
> - [[#Fourier Sine Integral]]
> - [[#Others]]

# Fourier Integral

和 [[Fourier Series]] 不同，用來分析沒有週期的訊號

## 定義

$$f(x) = \frac{ 1 }{ \pi }\int_0^\infty [A(\alpha)\cos(\alpha x) + B( \alpha)\sin(\alpha x)]d\alpha$$

$$A(\alpha) = \int_{ -\infty }^{\infty} f(x)\cos( \alpha x )dx$$

$$B(\alpha) = \int_{ -\infty }^\infty f(x)\sin(\alpha x)dx$$

### 和 [[Fourier Series]] 不同

1. 因為 Fourier Integral 沒有週期(週期無限大)，因此 [[Fourier Series]] 的 $a_0, a_n, b_n$ 無限小，$\sum$ 變成了 $\int_0^\infty$
2. $\frac{ 1 }{ \pi }$
3. $A(\alpha), B(\alpha)$ 沒有乘 $\frac{ 1 }{ p }$
4. $a_0$ 為 $\alpha = 0$ 的情況，因為積分有包含到 $0$ 所以不見了

### [[Fourier Series]] to Fourier Integral

[[Fourier Series]]:

$$f(x) = \frac{ a_0 }{ 2 } + \sum_{ n = 1 }^{ \infty }\left( a_n\cos\frac{ n\pi }{ p }x + b_n\sin\frac{ n\pi }{ p }x \right)$$

$$a_0 = \frac{ 1 }{ p }\int_{ -p }^{ p }f(x)dx$$

$$a_n = \frac{ 1 }{ p }\int_{ -p }^{ p }f(x)\cos\frac{ n\pi }{ p }xdx$$

$$b_n = \frac{ 1 }{ p }\int_{ -p }^{ p }f(x)\sin\frac{ n\pi }{ p }xdx$$

$$\implies f(x) = \frac{ 1 }{ 2p }\int_{ -p }^{ p }f(t)dt + \frac{ 1 }{ 
p }\sum_{ n = 1 }^\infty\left( \int_{ -p }^p f(t)\cos\frac{ n\pi }{ p } 
tdt \right)\cos\frac{ n\pi }{ p }x + \frac{ 1 }{ p }\sum_{ n = 1 }^\infty\left( \int_{ -p }^pf(t)\sin\frac{ n\pi }{ p }tdt \right)\sin\frac{ n\pi }{ p }x$$

令 $\Delta \alpha = \frac{ \pi }{ p } \qquad \frac{ 1 }{ p } = \frac{ \Delta \alpha }{ \pi }$

$$f(x) = \frac{ \Delta \alpha }{ 2\pi }\int_{ -p }^{ p }f(t)dt + \frac{ 
\Delta \alpha }{ \pi }\sum_{ n = 1 }^\infty \left( \int_{-p}^{ p }f(t)\cos(n\Delta \alpha \cdot t)dt \right)\cos(n\Delta \alpha \cdot x) + \frac{ \Delta \alpha }{ \pi }\sum_{ n = 1 }^{ \infty }\left( \int_{ -p }^p f(t)\sin(n \Delta \alpha \cdot t)dt \right)\sin(n\Delta \alpha \cdot x)$$

$$ = \frac{ 1 }{ 2\pi }\int_{ -p }^pf(t)dt\cos(0\Delta \alpha \cdot x)\Delta \alpha + \frac{ 1 }{ \pi }\sum_{ n = 1 }^\infty\left( \int_{ -p }^pf(t)\cos(n \Delta \alpha \cdot t)dt \right)\cos(n \Delta \alpha \cdot x)\Delta \alpha + \frac{ 1 }{ 2\pi }\int_{ -p }^pf(t)dt\sin(0\Delta \alpha \cdot x)\Delta \alpha + \frac{ 1 }{ \pi }\sum_{ n = 1 }^\infty \left( \int_{ -p }^{ p }f(t)\sin(n\Delta \alpha \cdot t)dt \right)\sin(n\Delta \alpha \cdot x)\Delta \alpha$$

when $p \rightarrow \infty$ (週期 $\rightarrow \infty$)，$\Delta \alpha \rightarrow 0$

$$\lim_{ \Delta \alpha \rightarrow 0 }\left[ S(0)\frac{ \Delta \alpha }{ 
2 } + \sum_{ n = 1 }^\infty S(n\Delta \alpha)\Delta \alpha \right] = \int_0^\infty S(\alpha)d\alpha$$

$$f(x) = \frac{ 1 }{ \pi }\int_0^\infty \left( \int_{ -p }^p f(t)\cos(\alpha t)dt \right)\cos( \alpha x )d\alpha + \frac{ 1 }{ \pi }\int_0^\infty \left( \int_{ -p }^p f(t)\sin(\alpha t)dt \right)\sin(\alpha x)d\alpha$$

$$f(x) = \frac{ 1 }{ \pi } \int_0^\infty \left[ \left( \int_{ -\infty }^\infty f(t)\cos(\alpha t)dt \right)\cos( \alpha x )d\alpha + \left( \int_{ -\infty }^\infty f(t)\sin(\alpha t)dt \right)\sin(\alpha x)d\alpha \right]$$

# Complex Form or Exponential Form of Fourier Integral

$$f(x) = \frac{ 1 }{ 2\pi }\int_{ -\infty }^\infty C(\alpha)e^{ -j\alpha x }d\alpha$$

$$C(\alpha) = \int_{ -\infty }^\infty f(x)e^{ j\alpha x }d\alpha$$

# Fourier Cosine Integral

$$f(x) = \frac{ 2 }{ \pi }\int_0^\infty A(\alpha)\cos(\alpha x)d\alpha$$

$$A(\alpha) = \int_0^\infty f(x)\cos(\alpha x)dx$$

適用情形: even 或 interval: $[0, \infty)$

# Fourier Sine Integral

$$f(x) = \frac{ 2 }{ \pi }\int_0^\infty B(\alpha)\sin(\alpha x)d\alpha$$

$$B(\alpha) = \int_0^\infty f(x)\sin(\alpha x)dx$$

適用情形: odd 或 interval: $[0, \infty)$

# Others

---

參考資料:

[[微分方程]第26講、Section 11-3 Fourier Cosine and Sine Series](https://youtu.be/l3VGEy4CSms)

---

link:

[[Integral Transform]]
[[Laplace Transform 解法]]