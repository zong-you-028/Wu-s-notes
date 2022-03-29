標籤: #電工學 

---

# Resistor

## [[Laplace Transform]]

$$v_R = i\cdot R$$

$$\mathcal{ L }[v_R] = R \mathcal{ L }[i(t)]$$

![[Resistor Laplace Transform.png]]

# Capacitor

## [[Laplace Transform]]

$$i_c = C\frac{ dv_c }{ dt }$$

$$\mathcal{ L }[i_c] = C\cdot \mathcal{ L }[\frac{ dv_c }{ dt }]$$

$$\mathcal{ L }[\frac{ dv_c }{ dt }] = sV_c(s) - v_c(0)$$

![[Capacitor Laplace Transform.png]]

# Inductor

## [[Laplace Transform]]

![[Inductor Laplace Transform.png]]

$$\mathcal{ L }[v_L] = L\mathcal{ L }\left[\frac{ di_L }{ 
dt }\right]$$

$$v_L = sLI_L - Li_L(0)$$

# RL Circuit

## [[Differential Equation]]

![[RL Circuit.png]]

$$\text{ KVL: } \qquad v_L - i_L R = 0$$

$$v_L = -L\frac{ di_L }{ dt }$$

$$\implies L\frac{ di_L }{ dt } + R i_L = 0$$

$$i_L = i_L(0) e^{ -\frac{ t }{ T } } \qquad \text{ where } T = \frac{ L }{ R }$$

## [[Laplace Transform]]

![[RL Circuit Laplace.png]]

$$I_R = \frac{ I_{ L0 } }{ s } \cdot \frac{ sL }{ sL + R }$$

$$ = I_{ L0 } \cdot \frac{ 1 }{ s + \frac{ 1 }{ T } } \qquad , T = \frac{ L }{ R }$$

# RC Circuit

## [[Differential Equation]]

![[Differential Equations in RLC circuit.png|400]]

$$i_c = i_R \qquad t \geq t_0$$

$$i_c = \underbrace{ - }_{ \text{ direction } }C \frac{ dv_c }{ dt }$$

$$\underbrace{ C \frac{ dv_c }{ dt } }_{ -i_c } + \underbrace{ \frac{ 
v_c }{ R } }_{ i_R } = 0$$

---

$$v_c = v_c(0) e^{ -\frac{ t }{ RC } } \qquad \text{ Let } T = RC \quad \text{ time constant }$$

## [[Laplace Transform]]

![[Laplace RC Circuit.png]]

$$v_c(s) = \frac{ v_{ c0 } }{ s }\frac{ R }{ \frac{ 1 }{sC} + R } = \frac{ RC }{ RCs + 1 }v_{ c0 }$$

$$ = \frac{ v_{ c0 } }{ s + \frac{ 1 }{ T } }$$

$$v_c(t) = \mathcal{ L }^{ -1 }\left[ \frac{ 1 }{ s + \frac{ 1 }{ T } } \right] \cdot v_{ c0 }$$

$$ = v_{ c0 }e^{ -\frac{ t }{ T } }$$

## Impedance

$$Z(s) = \frac{ V(s) }{ I(s) }$$

$$I(s) = scV(s) - \underbrace{ cv(0) }_{ \text{ source } }$$

$$V(s) = \frac{ 1 }{ sc }I(s) + \underbrace{ \frac{ 1 }{ 
s }v(0) }_{ \text{ source } }$$

# RLC Circuit (串連)

![[RLC Circuit Impedance.png]]

$$\frac{ V(s) }{ I(s) }
= \underbrace{ Z(s) }_{ \text{ 阻抗 (Impedance) } } = 
R + sL + \frac{ 1 }{ sC }$$

$$\implies Z(s) = \frac{ RCs + LCs^2 + 1 }{ sC }$$

求 $s$ when $Z(s) = 0$

$$\implies LCs^2 + RCs + 1 = 0$$

$s$ 稱為 zeroes

---

求 $s$ when $sC = 0$

$$sC = 0$$

$s$ 稱為 poles

## 虛數與實數

若 $s$ 以 $j\omega$ 代入

$$Z(j\omega) = \left.Z(s)\right\vert_{ s = j\omega } = \frac{ 1 - LC\omega^2 + j\omega RC }{ j\omega C }$$

[[Fourier Transform]]
$$\mathcal{ F }(\omega) = 
\int_0^\infty f(t)\cdot e^{ -j\omega t }dt$$
.
$$Z(j\omega) = 
R(\omega) + jX(\omega)$$

| $$R(\omega)$$   | $$jX(\omega)$$ |
| --------------- | -------------- |
| 實數部份        | 虛數部份       |
| 電阻 Resistance | 電抗 Reactance |

這兩個合起來叫做阻抗

# RLC Circuit (並聯)

![[RLC circuit(並聯).png]]

## 推導過程

Impedance $Z(s)$
(Resistance in $S$-domain)

$$Z(s) = \frac{ 1 }{ \frac{ 1 }{ 1 / sc } + \frac{ 1 }{ R } + \frac{ 1 }{ sL } }$$

Solve $V(s)$

$$V(s) = Z(s) \cdot \frac{ I_{ dc } }{ s }$$

Solve $I_L(s)$

$$I_L(s) = \frac{ V(s) }{ sL }$$

$$ = \frac{ 1 }{ sL } \cdot \frac{ I_{ dc } }{ s } \cdot \frac{ s/c }{ s^2 + \frac{ 1 }{ Rc }s + \frac{ 1 }{ Lc } }$$

$$ = I_{ dc }\underbrace{ \left( \frac{ 1 }{ s } \cdot \frac{ \omega_n^2 }{ s^2 + 2\xi \omega_n s + \omega_n^2 } \right) }_{ G(s) }$$

where $\xi = \frac{ 1 }{ 2R }\sqrt{ \frac{ L }{ c } }$

$$\omega_n = \sqrt{ \frac{ 1 }{ Lc } }$$

by Partial Fraction: 

$$G(s) = \underbrace{ \frac{ A_1 }{ s } }_{ u_s(t) } + \underbrace{ \frac{ A_2 (s + \sigma) }{ (s + \sigma)^2 + \omega_d^2 } }_{ \cos } + \underbrace{ \frac{ A_3 \cdot \omega_d }{ (s + \sigma)^2 + \omega_d } }_{ \sin }$$

where $\sigma = \xi \cdot \omega_n\; ,\;\omega_d = \sqrt{ 1 - \xi^2 }\cdot \omega_n$

$$A_1 = (G(s)\cdot s)\vert_{s = 0}$$

$$ = 1$$

移項

$$G(s) - \frac{ 1 }{ s } = \frac{ 1 }{ s }\left( \frac{s(s + 2\xi\omega_d)}{ s^2 + 2\xi\omega_n s + \omega_n^2 } \right)$$

$$ = \frac{(s + \sigma)}{ (s + \sigma)^2 + \omega_d^2 } + \frac{ \xi\omega_n }{ (s + \sigma)^2 + \omega_d }$$
.
$$A_2 = -1$$
.
$$A_3 = \frac{ -\xi }{ \sqrt{ 1 - \xi^2 } }$$
.
$$i_L(t) = I_{ dc }( \underbrace{ 1 }_{ \mathcal{ L }^{ -1 }\{ \frac{ 1 }{ s } \} \quad \text{ steady state } } - \underbrace{ e^{ -\sigma t }\cos\omega t - A_3 e^{ -\sigma t }\sin \omega dt }_{ \text{ transient Response } })$$

$$i_L = I_{ dc }\left(1 - \underbrace{ \sqrt{ 1 + A_3^2 } }_{  = \frac{ 1 }{ \sqrt{ 1 - \xi^2 } }  } \cdot e^{ -\sigma t }\sin(\omega dt + \beta)\right)$$
.
$$\beta = \tan^{ -1 }\frac{ \sqrt{ 1 - \xi^2 } }{ \xi } = \tan^{ -1 }\frac{ 1 }{ A_3 }$$

## 代值進去

$$\left\{
\begin{array}{}
	R = 625 \Omega \\
	c = 25nF \\
	L = 25 mH
\end{array}
\right.$$

$$\xi = \frac{ 1 }{ 2R }\sqrt{ \frac{ L }{ c } }$$

$$ = \frac{ 1 }{ 2 \cdot 625 }\cdot \sqrt{ \frac{ 25m }{ 25n } }$$

$$ = 0.8$$
.
$$\omega_n = \sqrt{ \frac{ 1 }{ Lc } } = \frac{ 1 }{ 25m \cdot 25n }$$

$$ = 40krad/s$$

$$ = 6kHz$$
.
$$\sigma = \xi \omega_n = 32krad/s$$
.
$$\omega_d = \sqrt{ 1 - \xi^2 }\omega_n = 24krad/s$$
.
$$i_L = 24\left(1 - \frac{ 1 }{ 0.6 }e^{ -32kt }\sin(24kt + \beta)\right)$$
.
$$\beta = \tan^{ -1 }\frac{ 0.6 }{ 0.8 } = 37\degree$$

## 交流電的情況

![[RLC circuit (並聯AC).png]]

$$i_s(t) = I_{ max }\cdot\sin(\omega t)$$
.
$$I_s(t) = \mathcal{ L }\{I_{ max }\sin\omega t\} = I_{ max }\cdot \frac{ \omega }{ s^2 + \omega^2 }$$
.
$$I_L(s) = \frac{ I_{ max }\cdot \omega }{ s^2 + \omega^2 }\cdot \left( \frac{ \omega_n^2 }{ s^2 + 2\xi\omega_n s + \omega_n^2 } \right)$$

Partial Function yields that

$$I_L(s) = \underbrace{ \frac{ A_1 }{ s - j\omega } + \frac{ \bar{ A }_1 }{ s + j\omega } }_{ \text{ steady state } } + \underbrace{ \frac{ A_2 }{ (s + \sigma) + j\omega_d } + \frac{ \bar{ A }_2 }{ (s + \sigma) - j\omega_d } }_{ \text{ trasient Response } }$$

1. $A_2$, $\bar{ A }_2$ are associated with the transient response which can die away fast
2. $A_1 = G(s) \cdot (s - j\omega)\vert_{ s = j\omega }$
$= \frac{ 1 }{ 2j }G(j\omega)$
3. Steady state Response

$$I_L(t) = \mathcal{ L }^{ -1 }\left\{ \frac{ Ae^{ j\theta } }{ 2j } \cdot \frac{ 1 }{ s - j\omega } + \frac{ Ae^{ -j\theta } }{ 2j } \cdot \frac{ 1 }{ s + j\omega } \right\}$$

$$A = \vert G(j\omega) \vert$$

$$\theta = \angle G(j\omega)$$

$$I_L(t) = I_{ max }A\frac{ e^{ j(\omega t + \theta) } - e^{ -j(\omega t + \theta) } }{ 2j }$$

[[Euler Formula]]
$$ = I_{ max } A \cdot \sin(\omega t + \theta)$$



---

參考資料:

電工學上課

---

link:

[[Inverse Laplace Transform#方法二 Decomposition of Fractions]]