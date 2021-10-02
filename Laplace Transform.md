標籤: #工程數學 

---

Laplace Transform of $f(t)$

$$F(s) = L\{f(t)\} = \int_0^\infty e^{-st}f(t)dt$$

通常用大寫來代表 transform 的結果，也就是上式的 $F(s)$

$s$ 可以是任何複數 $s = \mu + j\omega$

Laplace Transform 是一種 [[Integral Transform]]

# 拉普拉斯轉換表

底下這個東西要背起來

| $$f(t)$$      | $$F(s)$$                 | 算法                            |
| ------------- | ------------------------ | ------------------------------- |
| $$1$$         | $$\frac{1}{s}$$          | [[#L 1 frac 1 s \| link (1)]]   |
| $$t^n$$       | $$\frac{n!}{s^{n + 1}}$$ | [[#L t frac 1 s 2 \| link (t)]] |
| $$\exp(at)$$  | $$\frac{1}{s - a}$$      |                                 |
| $$\sin(kt)$$  | $$\frac{k}{s^2 + k^2}$$  |                                 |
| $$\cos(kt)$$  | $$\frac{s}{s^2 + k^2}$$  |                                 |
| $$\sinh(kt)$$ | $$\frac{k}{s^2 - k^2}$$  |                                 |
| $$\cosh(kt)$$ | $$\frac{s}{s^2 - k^2}$$  |                                 |

## $L\{1\} = \frac{1}{s}$

$$L\{1\} = \int_0^\infty e^{-st}dt$$
.
$$= \left. -\frac{e^{-st}}{s} \right\vert_0^\infty$$
.
$$= -\frac{e^{-s\cdot\infty}}{s} - (-\frac{e^{-s\cdot 0}}{s})$$
.
$$= \frac{1}{s}$$

> 這裡假設 $s > 0$, 所以
> $$-\frac{e^{-s\cdot \infty}}{s} = 0$$

## $L\{t\} = \frac{1}{s^2}$

$$L\{t\} = \int_0^\infty te^{-st}dt \qquad 
\begin{array}{}
	u = t & dv = e^{-st}dt \\
	du = 0 & v = -\frac{e^{-st}}{s}
\end{array}$$
.
$$= \left. -\frac{te^{-st}}{s} \right\vert_0^\infty + \int_0^\infty\frac{e^{-st}}{s}dt$$
.
$$= -\frac{\infty\cdot e^{-s\cdot\infty}}{s} + 0 - \left.\frac{e^{-st}}{s^2}\right\vert_0^\infty$$
.
$$= -\frac{e^{-s\cdot \infty}}{s^2} + \frac{e^{-s\cdot 0}}{s^2}$$
.
$$= \frac{1}{s^2}$$

# 特性

## 1. 可以把微分變成乘法

$$\text{可以將}\; \frac{d^k}{dt^k}y(t) \; \text{變成} \; s^kY(s) \underbrace{- s^{k - 1}y(0) - s^{k - 2}y'(0) - ... - sy^{(y - 2)}(0) - y^{(k - 1)}(0)}_{\text{同時考慮 initial conditions}}$$

## 2. 具有 Linear Property (可以乘進括號裡)

拉普拉斯轉換可以直接乘進括號裡

$$\int_0^\infty e^{-st}[\alpha f(t) + \beta g(t)]dt = \alpha \int_0^\infty e^{-st}f(t)dt + \beta\int_0^\infty e^{-st}g(t)dt$$

也就是

$$L\{\alpha f(t) + \beta g(t)\} = \alpha L\{f(t)\} + \beta L\{g(t)\}$$

> 事實上，所有 [[Integral Transform]] 都有這個性質

## 3. 並不是所有情況都可以用 Laplace Transform

### constraint 1

對於 $f(t)$ ，必須存在常數 $c$, $M > 0$, $T > 0$ ，滿足下列式子

$$\vert f(t) \vert \leq Me^{ct} \quad \text{for all} \; t > T$$

也就是 $Me^{ct}\; (c > 0)$ 要增加的比 $f(t)$ 快

![[Laplace Transform 存在條件一.png]]

[[#拉普拉斯轉換表]] 裡面的式子全部滿足 [[#constraint 1]]

#### 不滿足 [[#constraint 1]] 的例子

$$f(t) = \exp(t^2) \quad \text{並不存在}\; c \; \text{使得} \; \vert f(t)\vert \leq Me^{ct} \quad \text{for all } t > T$$

---

參考資料:

[Class 20 - Chapter 7 The Laplace Transform - youtube](https://youtu.be/m60TiMLKzvQ)