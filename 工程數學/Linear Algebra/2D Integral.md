標籤: #工程數學 

---

2D Integral 主要是關於
1. 2D region in 2D space
2. 2D [[Surface]] in 3D space

# 面積求法

Evaluating integral across $R$:

$$\underset{ R }{ \int\int } fdydx = 
\int_a^b
\left[
	\int_{ g(x) }^{ h(x) }
	f(x, y) dy
\right] dx$$

![[2D integral evaluate area R.png|400]]

# Green's Theorem

將 [[Line Integral]] 與 2D Integral 結合

![[green's theorem.png]]

tank 1:

$$\oint_C \vec v \cdot d\vec r = 4vL$$

tank 2:

$$\oint_C \vec v \cdot d \vec r = 4vL$$

我們得到一個結論，不管一個 tank 分成幾個小漩渦，積分起來都一樣

Evaluate integral across $R$:

$$\implies 
\underbrace { 
	\oint_C \vec F(\vec r) \cdot d\vec r 
}_{ \text{ 1D integral } } = 
\underset{ R }{ \int\int }(\nabla \times \vec F) \cdot \hat k dx dy$$

$$ = \underbrace{ 
	\underset{ R }{ \int\int } \left(
		\frac{ \partial F_2 }{ \partial x } - 
		\frac{ \partial F_1 }{ \partial y }
	\right) dA
}_{ \text{ 2D integral } }$$

# [[Surface]] Integral

2D [[Surface]] $S$ within 3D space:

![[surface integral.png|300]]

$$
\vec r(u, v) = 
\left[
	\begin{array}{}
		x(u, v) \\
		y(u, v) \\
		z(u, v)
	\end{array}
\right]
$$

> e.g.
> $(u, v)$ parametric representation of a cylinder in 3D space.

$$\vec r = 
\left[
	\begin{array}{}
		a\cos u \\
		a\sin u \\
		v
	\end{array}
\right]$$

$$\text{ gives a cylinder with radius } a$$

---

cone:

$$\vec r = 
\left[
	\begin{array}{}
		v\cos u \\
		v\sin u \\
		v
	\end{array}
\right]$$

---

參考資料:

工程數學上課

---

link:

$\nabla f$: [[Field#Scalar Field]]