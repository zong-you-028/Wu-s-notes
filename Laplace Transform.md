標籤: #工程數學 

---

Laplace Transform of $f(t)$

$$F(s) = L\{f(t)\} = \int_0^\infty e^{-st}f(t)dt$$

通常用大寫來代表 transform 的結果，也就是上式的 $F(s)$

Laplace Transform 是一種 [[Integral Transform]]

# 特性

laplace transform 有四個好用的特性

## 1. 可以把微分變成乘法

$$\text{可以將}\; \frac{d^k}{dt^k}y(t) \; \text{變成} \; s^kY(s) - s^{k - 1}y(0) - s^{k - 2}y'(0) - ... - sy^{(y - 2)}(0) - y^{(k - 1)}(0)$$

---

參考資料:

[Class 20 - Chapter 7 The Laplace Transform - youtube](https://youtu.be/m60TiMLKzvQ)