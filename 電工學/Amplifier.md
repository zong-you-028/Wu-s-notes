標籤: #電工學 

---

# Concept

$$\underbrace{ y(t) }_{ \text{ Output } } = \underbrace{ A }_{ \text{ Gain (fixed) } } \underbrace{ x(t) }_{ \text{ Input } }$$

## Practical Amplifier

![[Practical Amplifier.png]]

$$y(t) = \underbrace{ A(x, t, T) }_{ \text{ Nonlinear } } \cdot (x(t) + x_{ \text{ offset } }(t, T))$$

$t$: time
$T$: temperature

## Ideal Voltage Amplifier

![[Ideal Voltage Amplifier.png]]

$A$: Voltage Gain

## Ideal Current Amplifier

![[Ideal Current Amplifier.png]]

## Practical Current Amplifier

![[Practical Current Amp.png]]

## Voltage Controlled Current Source

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

---

參考資料:

電工學 2022-03-07

---

link:

