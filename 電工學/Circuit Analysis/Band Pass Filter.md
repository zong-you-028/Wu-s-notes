標籤: #電工學 

---

# Series

![[band pass filter series.png]]

We need a unit gain buffer to isolate two filters

![[band pass filter series with unit gain buffer.png]]

# Parallel

![[band pass filter parallel.png]]

[[#Low Pass Filter]] 和 [[#High Pass Filter]] 並聯

$$\omega_r = \frac{ 1 }{ \sqrt{ LC } }$$

$$G(\omega) = \frac{ v_o(\omega) }{ v_i(\omega) } = \frac{ -j\omega L }{ R(1 - \omega^2LC) - j\omega L } = \frac{ K\cdot j \frac{ \omega }{ \omega_l } }{ (1 + j\frac{ \omega }{ \omega_l })(1 + j\frac{ \omega }{ \omega_u }) }$$

![[band pass filter parallel diagram.png]]

# [[RLC Circuit#Operational Amplifier Filter|Operational Amplifier Filter]]

![[op amp filter.png]]

Op amp filter 是一種 "Active Filter"，也就是輸出的電流源和輸入的電流源不同

$$Z_1 = R_1 + \frac{ 1 }{ j\omega C_1 }$$

$$Z_f = R_2 \vert\vert \frac{ 1 }{ j\omega C_2 } = 
\frac{ R_2 \cdot \frac{ 1 }{ j\omega C_2 } }
{ R_2 + \frac{ 1 }{ j\omega C_2 } } = 
\frac{ R_2 }{ 1 + j\omega R_2 C_2 }$$

![[band pass filter using operational amplifier filter.png]]

$$\implies \frac { v_o }{ v_i } = 
-\frac{ j\omega R_2C_1 }
{(j\omega R_1C_1 + 1)(j\omega R_2C_2 + 1)}$$

$$ = -\frac{ 
	K\cdot j\frac{ \omega }{ \omega_l } 
}{ 
	(1 + j\frac{ \omega }{ \omega_l })
	(1 + j\frac{ \omega }{ \omega_u })
}$$

$$\implies
\left\{
	\begin{array}{}
		\omega_l = \frac{ 1 }{ R_1 C_1 } \\
		\omega_u = \frac{ 1 }{ R_2 C_2 }
	\end{array}
\right.$$

---

參考資料:

電工學上課

---

link:

