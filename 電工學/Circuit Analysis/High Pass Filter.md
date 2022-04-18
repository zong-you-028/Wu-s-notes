標籤: #電工學 

---

# RL Filter

![[rl filter.png]]

$$G(\omega) = \frac{ v_o(\omega) }{ v_i(\omega) } = \frac{ j\omega T }{ 1 + j\omega T } \qquad T = \frac{ L }{ R }$$

$$G(\omega) = \frac{ \omega T }{ \sqrt{ 1 + (\omega T)^2 } } \angle90\degree - \tan^{ -1 }\omega T$$

![[high pass filter diagram.png]]

# CR Filter

![[cr filter.png]]

$$G(\omega) = \frac{ v_o(\omega) }{ v_i(\omega) } = \frac{ j\omega T }{ 1 + j\omega T } \qquad T = RC$$

# [[RLC Circuit#Operational Amplifier Filter|Operational Amplifier Filter]]

![[op amp filter.png]]

Op amp filter 是一種 "Active Filter"，也就是輸出的電流源和輸入的電流源不同，因此可以串接

$$Z_1 = R + \frac{ 1 }{ j\omega C }$$

$$Z_f = R$$

$$\implies \frac{ v_o }{ v_i } = 
-\frac{ j\omega RC }{ j\omega RC + 1 }$$

---

參考資料:

電工學上課

---

link:

