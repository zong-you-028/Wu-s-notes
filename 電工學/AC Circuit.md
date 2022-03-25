標籤: #電工學 

---

# Angles

## Transient Response

![[Transient Responce.png]]

$$\overset{ \mathcal{ L } }{ \implies } \frac{ I_{ dc } }{ s } = \frac{ V }{ 1/sC } + \frac{ V }{ R } + \frac{ V }{ sL }$$

> $$V(s) = (sC + \frac{ 1 }{ R } + \frac{ 1 }{ sL })^{ -1 } \cdot \frac{ I_{ dc } }{ s }$$

$$\implies I_L = \frac{ V(s) }{ sL } = \frac{ I_{dc} / s }{ s^2LC + \frac{ L }{ R }s + 1 }$$

使用 [[Inverse Laplace Transform]] 中的 [[Inverse Laplace Transform#方法二 Decomposition of Fractions|Decomposition of Fractions]]

$$I_L = \frac{ A_1 \cdot 1 }{ s } + \frac{ A_2 (s + \sigma) }{ (s + \sigma)^2 + \omega^2 } + \frac{ A_3 \omega }{ (s + \sigma)^2 + \omega^2 }$$

計算後發現後面兩項太小，因此只需要第一項

$$A_1 = 24\text{mA}$$

---

參考資料:

電工學上課

---

link:

