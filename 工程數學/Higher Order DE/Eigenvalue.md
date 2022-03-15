標籤: #工程數學 

---

$$Ax = \lambda x$$
$A$: $n \times n$ matrix
$\lambda$: scalar
$x$: any vector

在上面式子的 $\lambda$ 就是 $A$ 的 eigenvalue，$x$ 就是 [[Eigenvector]]

# 求解 eigenvalue

$$A\vec{ v }_{ eig } = \lambda \vec{ v }_{ eig }$$

$$\implies A \vec{ v }_{ eig } - \lambda \vec{ v }_{ eig } = [A - \lambda I]\vec{ v }_{ eig } = 0$$

$$\implies [A - \lambda I]^{ -1 }[A - \lambda I]\vec{ v }_{ eig } = [A - \lambda I]^{ -1 } \cdot 0$$

$$\implies \vec{ v }_{ eig } = 0$$

$$[A - \lambda I] \text{ has to be singular to prevent } \vec{ v }_{ eig } = 0$$

Singular matrix:

$$\det(A - \lambda I) = 0$$

$$\implies \text{ we have solve for } \lambda (\lambda_1, \lambda_2, \dots, \lambda_n)$$

$$\implies \text{ Solve for } \vec{ v }_{ eig (1) }, \vec{ v }_{ eig (2) }, \dots, \vec{ v }_{ eig (n) } \text{ for } \lambda_1, \lambda_2, \dots, \lambda_n$$

(use [[Gauss Elimination]])

## 結論

$$\det \vert A - \lambda I\vert = 0$$

用上面式子即可解 eigenvalue $\lambda$

再接著用求出的 eigenvalue 求 [[Eigenvector]]

# Application of Eigenvalues Problems

## Simple Strain

> $$x_1^2 + x_2^2 = 1$$
> $$P: (x_1, x_2) \overset{ [A] }{ \rightarrow } Q: (y_1, y_2)$$
> $$[A] = \left[ \begin{array}{} 5 & 3 \\ 3 & 5 \end{array} \right]$$
> find "Principal directions" (eigenvectors)

eigenvalue

$$
\det
\left(
	\begin{array}{}
		5 - \lambda & 3 \\
		3 & 5 - \lambda
	\end{array}
\right) = 0 = (5 - \lambda)^2 = 9
$$

$$\lambda_1 = 8, \quad \lambda_2 = 2$$

$\lambda > 1$ means stretching

eigenvector

for $\lambda = 8$

$$
\left[
	\begin{array}{}
		5 - 8 & 3 \\
		3 & 5 - 8
	\end{array}
\right\vert
\left.
	\begin{array}{}
		0 \\
		0
	\end{array}
\right] = 
\left[
	\begin{array}{}
		-1 & 1 \\
		0 & 0
	\end{array}
\right\vert
\left.
	\begin{array}{}
		0 \\
		0
	\end{array}
\right]
$$

$$\implies -x_1 + x_2 = 0$$

$$
\vec{ x }^{ (1) } = 
\left[
	\begin{array}{}
		1 \\
		1
	\end{array}
\right]
$$

for $\lambda = 2$

$$
\left[
	\begin{array}{}
		5 - 2 & 3 \\
		3 & 5 - 2
	\end{array}
\right\vert
\left.
	\begin{array}{}
		0 \\
		0
	\end{array}
\right] = 
\left[
	\begin{array}{}
		1 & 1 \\
		0 & 0
	\end{array}
\right\vert
\left.
	\begin{array}{}
		0 \\
		0
	\end{array}
\right]
$$

$$\implies x_1 + x_2 = 0$$

$$
\vec{ x }^{ (2) } = 
\left[
	\begin{array}{}
		1 \\
		-1
	\end{array}
\right]
$$

## Traction / Principal Stresses

> Is there a cut, where $\vec{ t }_{ i }^{ (n) }$ align with $\vec{ n }_i$
> ![[Traction Principal Stresses.jpg]]

$$\vec{ t }_{ i } = \sigma \cdot \vec{ n }_{ i }$$

$$\vec{ t }_{ i }^{ (n) } = [\sigma_{ ij }]^T \vec{ n }_{ i } = [\sigma_{ ij }]\vec{ n }_{ i }$$

$$\vec{ t }_{ i }^{ (n) } = [\sigma_{ ij }]\vec{ n } = \sigma \vec{ n }$$

$$(\sigma_{ ij } - \sigma I) \vec{ n } = 0$$

$$
\left[
	\begin{array}{}
		\sigma_{ 11 } - \sigma & \sigma_{ 12 } & \sigma_{ 13 } \\
		\sigma_{ 21 } & \sigma_{ 22 } - \sigma & \sigma_{ 23 } \\
		\sigma_{ 31 } & \sigma_{ 32 } & \sigma_{ 33 } - \sigma
	\end{array}
\right]
\left[
	\begin{array}{}
		n_1 \\
		n_2 \\
		n_3
	\end{array}
\right] = 
\left[
	\begin{array}{}
		0 \\
		0 \\
		0
	\end{array}
\right]
$$

$$\implies \det(\sigma_{ ij } - \sigma I) = 0$$

find $\sigma_1, \sigma_2, \sigma_3$

find [[Eigenvector]]s $\vec{ n }$ (principal stresses)

## Markov Process

> $$\vec{ x }(t_i + 1) = [A]\vec{ x }(t_i)$$
> $$
> \left[
> \begin{array}{}
> & & & & \text{ (To:) } \\
> & 0.7 & 0.1 & 0 & (x_1) \\
> & 0.2 & 0.9 & 0.2 & (x_2) \\
> & 0.1 & 0 & 0.8 & (x_3) \\
> \text{ (From:) } & (x_1) & (x_2) & (x_3)
> \end{array}
> \right] \vec{ x }(t_i)
> $$
> Is there equilibrium

Using eigenvectors to find equilibrium (limit state)



---

參考資料:

工數課本P129
工程數學上課

---

link:

[[Matrices]]
[[Normal Stress]]