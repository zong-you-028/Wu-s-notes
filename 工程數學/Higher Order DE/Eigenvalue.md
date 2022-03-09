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

---

參考資料:

工數課本P129

---

link:

[[Matrices]]