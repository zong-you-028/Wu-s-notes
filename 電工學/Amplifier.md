標籤: #電工學 

---

# Concept

$$\underbrace{ y(t) }_{ \text{ Output } } = \underbrace{ A }_{ \text{ Gain (fixed) } } \underbrace{ x(t) }_{ \text{ Input } }$$

## Voltage Gain

$$v_o(t) = A_v v_i(t)$$

$A_v$: Voltage Gain

## Current Gain

$$A_i = \frac{ i_o }{ i_i } = \frac{ v_o / R_L }{ v_i / R_i } = A_v \frac{ R_i }{ R_L }$$

## Power Gain

$$G = \frac{ P_o }{ P_i } = \frac{ V_o I_o }{ V_i I_i } = A_v A_i = (A_v)^2 \frac{ R_i }{ R_L }$$

## Cascaded Amplifiers

當多個 Amplifier 串接在一起

$$A_v = A_{ v1 } A_{ v2 }$$

## Practical and Ideal Amplifiers

### Practical Amplifier

![[Practical Amplifier.png]]

$$y(t) = \underbrace{ A(x, t, T) }_{ \text{ Nonlinear } } \cdot (x(t) + x_{ \text{ offset } }(t, T))$$

$t$: time
$T$: temperature

### Ideal Voltage Amplifier

![[Ideal Voltage Amplifier.png]]

$A$: Voltage Gain

### Ideal Current Amplifier

![[Ideal Current Amplifier.png]]

### Practical Current Amplifier

![[Practical Current Amp.png]]

### Voltage Controlled Current Source

![[Voltage Controlled Current Source.png]]

# Operational Amplifier

![[Operational Amplifier.png]]

上面的原理圖簡化後變成下面的表示方式

![[Operational Amplifier Simplified.png]]

$p$: positive (non-Inverting terminal)
$n$: negative (Inverting terminal)

## Ideal OP amp & Practical OP amp comparison

|                  | $$r_i$$      | $$r_0$$        | $$A$$              | $$v_{ ps }$$ |
| ---------------- | ------------ | -------------- | ------------------ | ------------ |
| Ideal OP amp     | $$\infty$$   | $$0$$          |                    |              |
| Practical OP amp | $$1M\Omega$$ | $$100 \Omega$$ | $$10^5 \sim 10^6$$ | $$15V$$      | 

# Amplifier Usages

## Non-inverting Amplifier

![[Non-inverting Amplifier.png]]

Assuming that $r_i = \infty$ and $r_0 = 0$ ,

$$1. \quad i_p = i_n = 0$$
.
$$2. \quad v_n = \underbrace{ v_{ in } }_{ v_p } - v_d$$
.
$$3. \quad v_n = Bv_{ out } = B(Av_d)$$
$$B = \frac{ R_1 }{ R_F + R_1 } \qquad \text{ voltage divider }$$
.
$$2. = 3. \implies v_{ in } - v_d = BAv_d$$
$$\frac{ v_d }{ v_{ in } } = \frac{ 1 }{ 1 + AB }$$
$$\frac{ v_0 }{ v_{ in } } = \frac{ A }{ 1 + AB }$$

## Voltage Follower (Unit Gain Buffer)

![[Voltage Follower (Unit Gain Buffer).png]]

## Inverting Amplifier

![[Inverting Amplifier.png]]

Assuming $v_d \simeq 0$, 

$$i_i = \frac{ v_{ in } }{ R_1 }$$

$$v_0 = -i_1 \cdot R_F$$

$$\implies \frac{ v_0 }{ v_{ in } } = \frac{ -R_F }{ R_1 }$$

## Summing Amplifier

![[Summing Amplifier.png]]

$R_F$: Feedback 回授

Assuming 
$$v_d \simeq 0$$
$$i_n = 0$$
.
$$v_0 = -\left(\frac{ R_F }{ R_1 }v_1 + \frac{ R_F }{ R_2 }v_2\right)$$

## Difference Amplifier

![[Difference Amplifier.png]]

$$1. \quad v_p = v_2 \times \frac{ R_F }{ R_2 + R_F }$$

$$2. \quad \frac{ v_1 - v_n }{ R_1 } = i_1$$

$$\vdots$$

---

參考資料:

電工學 2022-03-07

---

link:

