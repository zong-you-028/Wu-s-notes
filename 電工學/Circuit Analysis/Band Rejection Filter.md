標籤: #電工學 

---

又稱為 Notch Filter，將已知的頻段部份去除

![[band rejection filter.png]]

$$\frac{ v_o }{ v_i } = 
G_{ BR }(j\omega) = 
\frac R 
{ j\omega L \vert\vert \frac 1 { j \omega C } + R }$$

$$G_{ BR }(\omega) = 1 - G_{ BP }(\omega)$$

$$ = 1 - \frac{ K j \frac{ \omega }{ \omega_l } }
{ (1 + j \frac \omega { \omega_l }) \cdot 
(1 + j\frac \omega { \omega_u }) }$$

![[diagram band rejection filter and band pass filter.jpg]]

$$B.W.\text{ (bandwidth) } = 
\frac{ \sqrt{ 1 -  4R^2 \frac{ C }{ L } } }
{ RC }$$

$$\omega_p \text{ (peak frequency) } = 
\frac 1 { \sqrt{ LC } }$$

$$\omega_u \text{ (upper frequency) } = 
\omega_p + \frac{ B.W. }{ 2 }$$

$$\omega_l \text{ (lower frequency) } = 
\omega_p - \frac{ B.W. }{ 2 }$$

---

參考資料:

電工學上課

---

link:

