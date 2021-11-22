標籤: #工程數學 

---

利用 [[Eigenvalue]]，求出 [[ODE & PDE|ODE]] 的解

# 解法

## 列出兩行式子的情況

### Step 1 列式

$$
\begin{array}{}
y_1' & = & -0.02y_1 & + & 0.02y_2 \\
y_2' & = & 0.02y_1 & - & 0.02y_2
\end{array}
$$

$y$ 向量如下

$$
y = 
\left[
\begin{array}{}
y_1 \\
y_2
\end{array}
\right]
$$

利用 $y$ 向量重新列式

$$
y' = Ay \qquad A = 
\left[
\begin{array}{}
-0.02 & 0.02 \\
0.02 & -0.02
\end{array}
\right]
$$

### Step 2 求 general solution

假設解為 exponential function

$$y = xe^{ \lambda t }$$

則解 $y$ 的微分

$$y' = \lambda x e^{ \lambda t }$$

根據 [[#Step 1 列式|Step 1]] 的列式整理 $y'$

$$y' = \lambda x e^{ \lambda t } = Axe^{ \lambda t }$$

同時除以 $e^{ \lambda t }$

$$\lambda x = Ax$$

使用 [[Eigenvalue]] 的解法，得出 $\lambda$

$$\det (A - \lambda I) = 
\left\vert
\begin{array}{}
-0.02 - \lambda & 0.02 \\
0.02 & -0.02 - \lambda
\end{array}
\right\vert = 
(-0.02 - \lambda)^2 - 0.02^2 = \lambda(\lambda + 0.04) = 0$$

$$
\left\{
\begin{array}{l}
\lambda_1 = 0 \\
\lambda_2 = -0.04
\end{array}
\right.
$$

將 $\lambda$ 代入下式，求出 [[Eigenvector]]

$$
\left[
\begin{array}{}
a_{ 11 } - \lambda & a_{ 12 } \\
a_{ 21 } & a_{ 22 } - \lambda
\end{array}
\right]
\left[
\begin{array}{}
x_1 \\
x_2
\end{array}
\right] = 
\left[
\begin{array}{}
0 \\
0
\end{array}
\right]
\quad , \quad
\left\{
\begin{array}{l}
\lambda_1 = 0 \\
\lambda_2 = -0.04
\end{array}
\right.
$$
.
$$
\implies
\left[
\begin{array}{}
-0.02 - \lambda & 0.02 \\
0.02 & -0.02 - \lambda
\end{array}
\right]
\left[
\begin{array}{}
x_1 \\
x_2
\end{array}
\right] = 
\left[
\begin{array}{}
0 \\
0
\end{array}
\right]
$$
.
$$
\implies
\left\{
\begin{array}{}
	\left[
	\begin{array}{}
		-0.02 - 0 & 0.02 \\
		0.02 & -0.02 - 0
	\end{array}
	\right]
	\left[
	\begin{array}{}
		x_1 \\
		x_2
	\end{array}
	\right] = 
	\left[
	\begin{array}{}
		0 \\
		0
	\end{array}
	\right]
	
	\\
	
	\left[
	\begin{array}{}
		-0.02 - (-0.04) & 0.02 \\
		0.02 & -0.02 - (-0.04)
	\end{array}
	\right]
	\left[
	\begin{array}{}
		x_1 \\
		x_2
	\end{array}
	\right] = 
	\left[
	\begin{array}{}
		0 \\
		0
	\end{array}
	\right]
\end{array}
\right.
$$
.
$$
\implies 
\left\{
\begin{array}{l}
-0.02x_1 + 0.02x_2 = 0 \\
(-0.02 + 0.04)x_1 + 0.02x_2 = 0
\end{array}
\right.
\qquad
\text{ 最後只會得出兩個，因為另外兩個無效 }
$$
.
$$
\implies
\left\{
\begin{array}{l}
	x_1 = x_2 \\
	x_1 = -x_2
\end{array}
\right.
$$

可以得出兩個 [[Eigenvector]]

$$x^{(1)} = 
\left[
\begin{array}{}
	1 \\
	1
\end{array}
\right]
\quad \text{ and } \quad
x^{ (2) } = 
\left[
\begin{array}{r}
	1 \\
	-1
\end{array}
\right]$$

將 [[Eigenvalue]] 和 [[Eigenvector]] 代入

$$
\left\{
\begin{array}{}
	\lambda_1 = 0 \\
	\lambda_2 = -0.04 \\
	x^{ (1) } = 
	\left[
	\begin{array}{}
		1 \\
		1
	\end{array}
	\right] \\
	x^{ (2) } = 
	\left[
	\begin{array}{r}
		1 \\
		-1
	\end{array}
	\right]
\end{array}
\right.
\quad , \quad 
y = c_1x^{ (1) }e^{ \lambda_1 t } + c_2x^{ (2) }e^{ \lambda_2 t }
$$
.
$$
\implies y = c_1
\left[
\begin{array}{}
	1 \\
	1
\end{array}
\right] + c_2
\left[
\begin{array}{r}
	1 \\
	-1
\end{array}
\right] e^{ -0.04t }
$$

### Step 3 initial condition

$$
t = 0 \quad , \quad y(0) = 
\left[ 
\begin{array}{}
	0 \\
	150
\end{array}
\right]
$$

$$
\implies y(0) = c_1
\left[
\begin{array}{}
	1 \\
	1
\end{array}
\right] + c_2
\left[
\begin{array}{}
	1 \\
	-1
\end{array}
\right] = 
\left[
\begin{array}{}
	0 \\
	150
\end{array}
\right]
$$

$$
\implies 
\left\{
\begin{array}{}
	c_1 = 75 \\
	c_2 = -75
\end{array}
\right.
$$

$$\implies y = 75
\left[
\begin{array}{}
	1 \\
	1
\end{array}
\right] - 75
\left[
\begin{array}{}
	1 \\
	-1
\end{array}
\right] e^{ -0.04 t }$$

$$
\implies 
\left\{
\begin{array}{}
	y_1 = 75 - 75 e^{ -0.04t } \\
	y_2 = 75 + 75 e^{ -0.04t }
\end{array}
\right.
$$

## 解一般 [[ODE & PDE|ODE]] 的情況

有一個 ODE

$$y^{ (n) } = F(t, y, y', \dots , y^{ (n - 1) })$$

將所有微分換成 $y_{component}$

$$y_1 = y, \quad y_2 = y' , \quad y_3 = y'' , \quad \dots , \quad y_n = y^{ (n - 1) }$$

整理成矩陣

$$
\left\{
\begin{array}{}
y_1'       & =      & y_2 \\
y_2'       & =      &     & y_3 \\
           & \vdots &     &     & \ddots\\
y_{n - 1}' & =      &     &     &        & y_n \\
y_n'       & =      &     &     &        & F(t, y_1, y_2, \dots , y_n)
\end{array}
\right.
$$

$$
y' = Ay = 
\left[
\begin{array}{}
0 & 1      & 0 & \dots  & 0 \\
0 & 0      & 1 & \dots  & 0 \\
0 & \vdots &   & \ddots & 0 \\
0 & 0      & 0 & \dots  & 1 \\
a_1 & a_2  & a_3 & \dots & a_n
\end{array}
\right]
\left[
\begin{array}{}
y_1 \\
y_2 \\
\vdots \\
y_{ n - 1 } \\
y_n
\end{array}
\right]
$$

利用 $\det (A - \lambda I) = 0$ 求出 [[Eigenvalue]] (如果不重根會有 $n$ 個)，帶入 $(A - \lambda I)x = 0$ 求 [[Eigenvector]] $x$

$$y = c_1x^{ (1) }e^{ \lambda_1 t } + c_2x^{ (2) }e^{ \lambda_2 t } + \dots + c_nx^{ (n) }e^{ \lambda_n t }$$

### 重根

直接看例子

> Example:
> $$
> \vec{ y' } = A \vec{ y } = 
> \left[
> \begin{array}{}
>     4 & 1 \\
>     -1 & 2
> \end{array}
> \right]
> $$

---

參考資料:

工數課本P131
工數PPT 4.0~4.1 P51

---

link:

