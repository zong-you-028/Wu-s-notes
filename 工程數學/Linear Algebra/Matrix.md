標籤: #工程數學 

---

# Operation

## Addition

$$\left[ 
\begin{array}{}
a_{ 11 } & a_{ 12 } \\
a_{ 21 } & a_{ 22 }
\end{array}
\right] + 
\left[
\begin{array}{}
b_{ 11 } & b_{ 12 } \\
b_{ 21 } & b_{ 22 }
\end{array}
\right] = 
\left[
\begin{array}{}
a_{ 11 } + b_{ 11 } & a_{ 12 } + b_{ 12 } \\
a_{ 21 } + b_{ 21 } & a_{ 22 } + b_{ 22 }
\end{array}
\right]$$

## [[Matrix Multiplication|Multiplications]]

### Scalar Multiply

$$
b
\left[
\begin{array}{}
a_{ 11 } & a_{ 12 } \\
a_{ 21 } & a_{ 22 }
\end{array}
\right] = 
\left[
\begin{array}{}
ba_{ 11 } & ba_{ 12 } \\
ba_{ 21 } & ba_{ 22 }
\end{array}
\right]
$$

### Matrix Multiply

$$
\left[
\begin{array}{}
a_{ 11 } & a_{ 12 } \\
a_{ 21 } & a_{ 22 } \\
a_{ 31 } & a_{ 32 }
\end{array}
\right] *
\left[
\begin{array}{}
b_{ 11 } & b_{ 12 } & b_{ 13 } \\
b_{ 21 } & b_{ 22 } & b_{ 23 }
\end{array}
\right]
$$

上面的矩陣是 $3\times 2$ 和 $2\times 3$ 的，如果要可以乘起來 $a\times b \text{ and } c \times d$ 兩個陣列的 $b$ 和 $c$ 必須相等(在這個情況是 $2$ )，並且最後的結果會是 $a\times d$ (在這個情況是 $3\times 3$ )

法則: 橫的乘上直的加起來

#### Rules

- $AB \neq BA$
- $(kA)B = k(AB)$
- $(AB)C = A(BC)$
- $(A + B)C = AC + BC$
- $C(A + B) = CA + CB$

### Array Multiplication (Element-wise Multiplication)

$$A \ _.* B = 
\left[
\begin{array}{}
a_{ 11 } & a_{ 12 } \\
a_{ 21 } & a_{ 22 }
\end{array}
\right] \ _.*
\left[
\begin{array}{}
b_{ 11 } & b_{ 12 } \\
b_{ 21 } & b_{ 22 }
\end{array}
\right] = 
\left[
\begin{array}{}
a_{ 11 }b_{ 11 } & a_{ 12 }b_{ 12 } \\
a_{ 21 }b_{ 21 } & a_{ 22 }b_{ 22 }
\end{array}
\right]$$

## [[Matrix Transposition|Transpose]]

$$A = [a_{ ji }] \ \rightarrow \ A^T = [a_{ ij }]$$

- $(A^T)^T = A$
- $(A + B)^T = A^T + B^T$
- $(cA)^T = cA^T$
- $(AB)^T = B^T A^T$

# Others

- Symmetric

$$A^T = A$$

- Skew Symmetric 

$$A^T = -A$$

- Diagnol Matrix

$$\left[
\begin{array}{}
a & 0 & 0 \\
0 & b & 0 \\
0 & 0 & c
\end{array}
\right]$$

- Identity Matrix

$$
\left[
\begin{array}{}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{array}
\right]
$$

---

參考資料:

工程數學上課

---

link:

