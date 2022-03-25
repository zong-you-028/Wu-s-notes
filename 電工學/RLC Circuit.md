標籤: #電工學 

---

# [[Differential Equation]]

## RC Circuit

![[Differential Equations in RLC circuit.png|400]]

$$i_c = i_R \qquad t \geq t_0$$

$$i_c = \underbrace{ - }_{ \text{ direction } }C \frac{ dv_c }{ dt }$$

$$\underbrace{ C \frac{ dv_c }{ dt } }_{ -i_c } + \underbrace{ \frac{ 
v_c }{ R } }_{ i_R } = 0$$

---

$$v_c = v_c(0) e^{ -\frac{ t }{ RC } } \qquad \text{ Let } T = RC \quad \text{ time constant }$$

## RL Circuit

![[RL Circuit.png]]

$$\text{ KVL: } \qquad v_L - i_L R = 0$$

$$v_L = -L\frac{ di_L }{ dt }$$

$$\implies L\frac{ di_L }{ dt } + R i_L = 0$$

$$i_L = i_L(0) e^{ -\frac{ t }{ T } } \qquad \text{ where } T = \frac{ L }{ R }$$

# [[Laplace Transform]]

$$F(s) = \int_0^\infty f(t) \cdot e^{ -st }dt$$

## Resistor

$$v_R = i\cdot R$$

$$\mathcal{ L }[v_R] = R \mathcal{ L }[i(t)]$$

![[Resistor Laplace Transform.png]]

## Capacitor

$$i_c = C\frac{ dv_c }{ dt }$$

$$\mathcal{ L }[i_c] = C\cdot \mathcal{ L }[\frac{ dv_c }{ dt }]$$

$$\mathcal{ L }[\frac{ dv_c }{ dt }] = sV_c(s) - v_c(0)$$

![[Capacitor Laplace Transform.png]]

## RC Circuit

![[Laplace RC Circuit.png]]

$$v_c(s) = \frac{ v_{ c0 } }{ s }\frac{ R }{ \frac{ 1 }{sC} + R } = \frac{ RC }{ RCs + 1 }v_{ c0 }$$

$$ = \frac{ v_{ c0 } }{ s + \frac{ 1 }{ T } }$$

$$v_c(t) = \mathcal{ L }^{ -1 }\left[ \frac{ 1 }{ s + \frac{ 1 }{ T } } \right] \cdot v_{ c0 }$$

$$ = v_{ c0 }e^{ -\frac{ t }{ T } }$$

## Inductor

![[Inductor Laplace Transform.png]]

$$\mathcal{ L }[v_L] = L\mathcal{ L }\left[\frac{ di_L }{ 
dt }\right]$$

$$v_L = sLI_L - Li_L(0)$$

## RL Circuit

![[RL Circuit Laplace.png]]

$$I_R = \frac{ I_{ L0 } }{ s } \cdot \frac{ sL }{ sL + R }$$

$$ = I_{ L0 } \cdot \frac{ 1 }{ s + \frac{ 1 }{ T } } \qquad , T = \frac{ L }{ R }$$

# Impedance

## RC Circuit

$$Z(s) = \frac{ V(s) }{ I(s) }$$

$$I(s) = scV(s) - \underbrace{ cv(0) }_{ \text{ source } }$$

$$V(s) = \frac{ 1 }{ sc }I(s) + \underbrace{ \frac{ 1 }{ 
s }v(0) }_{ \text{ source } }$$

## RLC Circuit

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

### 虛數與實數

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

---

參考資料:

電工學上課

---

link:

