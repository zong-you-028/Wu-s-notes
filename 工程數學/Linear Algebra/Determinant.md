標籤: #工程數學 

---

# Application

- ODE [[Wronskian]]
- cross product
- [[Eigenvalue]]
- ==solve system of equation== [[Cramer's Rule]]

# Calculate

Order $n = 3$

$$
\det\left(\left[
\begin{array}{}
a & b & c \\
d & e & f \\
g & h & i
\end{array}
\right]\right) = 
a\det\left(\left[
\begin{array}{}
e & f \\
h & i
\end{array}
\right]\right) - 
b\det\left(\left[
\begin{array}{}
d & f \\
g & i
\end{array}
\right]\right) + 
c\det\left(\left[
\begin{array}{}
d & e \\
g & h
\end{array}
\right]\right)$$

$$
= -b\det\left(\left[
\begin{array}{}
d & f \\
g & i
\end{array}
\right]\right) +
e\det\left(\left[
\begin{array}{}
a & c \\
g & i
\end{array}
\right]\right) - 
h\det\left(\left[
\begin{array}{}
a & c \\
d & f
\end{array}
\right]\right)
$$

> Pattern of signs:
> $$\left(\begin{array}{} + & - & + \\ - & + & - \\ + & - & + \end{array}\right) \qquad \left(\begin{array}{} + & - & + & - \\ - & + & - & + \\ + & - & + & - \\ - & + & - & + \end{array}\right)$$

## General Mathematical Formulation

$$\det(A) = a_{ j1 }c_{ j1 } + a_{ j2 }c_{ j2 } + \dots + a_{ jn }c_{ jn } \qquad (j = 1,\ 2,\ \dots,\ n)$$

$$c_{ ji } \equiv (-1)^{ j + 1 }M_{ ji }$$

$M_{ ji } \equiv$ a determinant of the matrix of order $n - 1$ , formed for $A$ by taking at the column and row of entry $a_{ ji }$

---

參考資料:

工程數學 2022-03-02

---

link:

[[Matrix]]