標籤: #工程數學 

---

$$Ax = \lambda x$$
$A$: $n \times n$ matrix
$\lambda$: scalar
$x$: any vector

在上面式子的 $\lambda$ 就是 $A$ 的 [[Eigenvalue]]，$x$ 就是 Eigenvector

# 求解 eigenvector

將定義移向

$$Ax = \lambda x \implies (A - \lambda I)x = 0$$

以矩陣表示

$$
\left[
\begin{array}{}
a_{ 11 } - \lambda & a_{ 12 } \\
a_{ 21 }           & a_{ 22 } - \lambda
\end{array}
\right]
\left[
\begin{array}{}
x_1 \\
x_2
\end{array}
\right]
=
\left[
\begin{array}{}
0 \\
0
\end{array}
\right]
$$

先求出 [[Eigenvalue]]，帶入上式並使用 [[Augmented Matrix Method]] 就可以解出 eigenvector

---

參考資料:

工數課本P129

---

link:

[[Eigenvalue]]