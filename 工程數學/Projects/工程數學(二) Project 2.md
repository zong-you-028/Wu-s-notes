# 4. What You Need To Do:

## 1. Defining your scalar field:

- Come up with an equation that describes the 3D temperature-field (i.e. a scalar field 𝑇(𝑥, 𝑦, 𝑧)), which satisfy the three constraints given above.

A two-dimentional Gaussian function:

$$f(x, y) = A e^{
	-\left(
		\frac{(x - x_0)^2}{2\sigma_x^2} +
		\frac{(y - y_0)^2}{2\sigma_y^2}
	\right)
}$$

where $A$ is amplitude, $x_0, y_0$ is the center, and $\sigma_x, \sigma_y$ are $x$ and $y$ spreads of the blob

in our case, $x_0, y_0 = 0$, $\sigma_x = \sigma_y$

$$\implies f(x, y) = A e^{
	-\left(
	\frac{x^2}{2\sigma^2} +
	\frac{y^2}{2\sigma^2}
	\right)
}$$

First condition: $f(0, 0) = 1000000$

$$\implies A = 10^6$$

Second condition: $f(1000, 0) = 10000$

$$\implies 10000 = 10^6 e^{
	-\left(
		\frac{10^6}{2\sigma^2}
	\right)
}$$

$$\implies -\frac{10^6}{2\sigma^2} = 
\ln\left(
	\frac{10000}{10^6}
\right)$$

$$\implies-\frac{10^6}{2\sigma^2} = -4.6052$$

$$\implies \frac{1}{2\sigma^2} = 4.6052 \times 10^{-6}$$

$$\implies 2\sigma^2 = 217147.241$$

$$\implies \sigma = 329.5051$$

$$\therefore \underline{
	f(x, y) = 10^6 e^{
		-\left(
			\frac{ x^2 }{ 217147.241 } +
			\frac{ y^2 }{ 217147.241 }
		\right)
	}
}_\#$$

---

# Reference

[Two-dimensional Gaussian function - wikipedia](https://en.wikipedia.org/wiki/Gaussian_function#Two-dimensional_Gaussian_function)