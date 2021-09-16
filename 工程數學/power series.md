標籤: #工程數學 

---

# 定義

## 1. Power Series

$$\sum_{n = 0}^{\infty}c_n(x - x_0)^n = c_0 +
										c_1(x - x_0) +
										c_2(x - x_0)^2 + ...$$
										
## 2. Convergence

$$\lim_{N \rightarrow \infty} \sum_{n = 0}^{N}c_n(x - x_0)^n \quad\text{exists}$$

### 測試方法: Ratio Test

test for convergence

$$\lim_{n \rightarrow \infty} \left\vert \frac{c_{n + 1}(x - x_0)^{n + 1}}{c_n(x - x_0)^n} \right\vert = L$$
$$L < 1: \text{converge} \quad L > 1 : \text{diverge} \quad L = 1 : \text{不一定}$$

## 3. Radius of Convergence

$x$ 在一定範圍內會是收斂，在這個範圍外發散
這個範圍就叫做收斂半徑（[[#3 Radius of Convergence | Radius of Convergence]]）

$$L < 1 \;\text{if}\;\vert x - x_0 \vert < R$$
$$L > 1 \;\text{if}\;\vert x - x_0 \vert > R$$

# [[Taylor Series]] 的收斂範圍

| [[Taylor Series]]                                                        | Interval of Convergence |
| ------------------------------------------------------------------------ | ----------------------- |
| $$e^x = 1 + \frac{x}{1!} + \frac{x^2}{2!} + \frac{x^3}{3!} + ...$$       | $$(-\infty , \infty)$$  |
| $$\sin x = x - \frac{x^3}{3!} + \frac{x^5}{5!} - ...$$                   | $$(-\infty , \infty)$$  |
| $$\cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!}...$$     | $$(-\infty , \infty)$$  |
| $$\ln(1 + x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + ...$$ | $$(-1, 1]$$             |
| $$\frac{1}{1 - x} = 1 + x + x^2 + x^3 + ...$$                            | $$(-1, 1)$$             | 



---

參考資料:

[Series Solutions of Linear Equations](https://youtu.be/2ARH7cnl2vk)