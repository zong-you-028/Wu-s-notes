標籤: #電工學 

---

# Concept

Amplifier 是一種將訊號放大的東西

$$\underbrace{ y(t) }_{ \text{ Output } } = \underbrace{ A }_{ \text{ Gain (fixed) } } \underbrace{ x(t) }_{ \text{ Input } }$$

一個 voltage amplifier 的 schematic diagram 會長這樣

![[schematic diagram of amplifier.png]]

$v_s$: voltage of source
$R_s$: resistance of source
$R_L$: load resistance

$v_i$: input voltage
$v_o$: output voltage
$i_o$: output current
$A_{ voc }$: 在 open circuit 的情況下，amplifier 放大 voltage 的倍數

Amplifier 包含了 3 個可分析的參數
1. [[#Voltage Gain]]
2. [[#Current Gain]]
3. [[#Power Gain]]

## Voltage Gain

Voltage 放大了幾倍

$$v_o(t) = A_v v_i(t)$$

$A_v$: Voltage Gain

## Current Gain

Current 放大了幾倍

$$A_i = \frac{ i_o }{ i_i } = \frac{ v_o / R_L }{ v_i / R_i } = A_v \frac{ R_i }{ R_L }$$

## Power Gain

$$G = \frac{ P_o }{ P_i } = \frac{ V_o I_o }{ V_i I_i } = A_v A_i = (A_v)^2 \frac{ R_i }{ R_L }$$

## Cascaded Amplifiers

可以將多個 Amplifier 串接在一起，將放大倍數乘起來

當多個 Amplifier 串接在一起

$$A_v = A_{ v1 } A_{ v2 }$$

## Power Supplies

amplifier 需要使用 power supply 協助運作，power 的流動如下圖

![[illustration of power flow in amplifier.png]]

可以看到有部份的 output signal 是 power supply 提供的

## Efficiency

這個 efficiency 是指 power supply 與輸出訊號的效率關係，可以用以下公式計算

$$\eta = \frac{ P_o }{ P_s } \times 100 \%$$

$P_o$: output power
$P_s$: supply power

# Other Amplifiers

除了上面提到的 voltage amplifier 以外，還有其他種類的 amplifier

1. [[#Current Amplifier]]

## Current Amplifier

以下是 current amplifier 的樣子

![[current amplifier.png]]

就和 [[Kirchhoff's Law#Thevenin Norton-Equivalent-Circuit Analysis|Thevenin Norton Circuit]] 一樣，current amplifier 和 voltage amplifier 也可以互相轉換，譬如以下例題

> Find the current-amplifier model of the voltage-amplifier model shown below.
> ![[example of converting a voltage amplifier to a current amplifier.png]]

為了找到 short-circuit current gain ，我們將 output terminal short ，找到以下關係

$$
\left\{
	\begin{array}{}
		i_i = \frac{ v_i }{ R_i } \\
		i_{ osc } = 
		\frac{ A_{ voc } v_i }{ R_o }
	\end{array}
\right.
$$

The short-circuit current gain is

$$A_{ isc } = \frac{ i_{ osc } }{ i_i } = 
A_{ voc } \frac{ R_i }{ R_o } = 10^3$$

## Transconductance Amplifier

類似 [[#Current Amplifier]] ，但是 dependent current source 依據的是 $v_{ in }$

![[transconductance-amplifier model.png]]

gain parameter 用 $G_{ msc }$ 表示，如下

$$G_{ msc } = \frac{ i_{ osc } }{ v_i }$$

## Transresistance Amplifier

類似 voltage amplifier ，與 [[#Transconductance Amplifier]] 相反。是一個 voltage amplifier 的接法和 current dependent voltage source

![[transresistance amplifier.png]]

$$R_{ moc } = \frac{ v_{ ooc } }{ i_i }$$

# Practical and Ideal Amplifiers

chart of ideal amplifiers:

| Amplifier Type                                          | Input Impedance | Output Impedance | Gain Parameter |
| ------------------------------------------------------- | --------------- | ---------------- | -------------- |
| [[#Ideal Voltage Amplifier\|Voltage]]                   | $$\infty$$      | $$0$$            | $$A_{ voc }$$  |
| [[#Ideal Current Amplifier\|Current]]                   | $$0$$           | $$\infty$$       | $$A_{ isc }$$  |
| [[#Ideal Transconductance Amplifier\|Transconductance]] | $$\infty$$      | $$\infty$$       | $$G_{ msc }$$  |
| [[#Ideal Transresisstance Amplifier\|Transresistance]]  | $$0$$           | $$0$$            | $$R_{ moc }$$  |

## Practical Amplifier

![[Practical Amplifier.png]]

$$y(t) = \underbrace{ A(x, t, T) }_{ \text{ Nonlinear } } \cdot (x(t) + x_{ \text{ offset } }(t, T))$$

$t$: time
$T$: temperature

## Ideal Voltage Amplifier

需要檢測 open-circuit voltage 並且產生放大後的 voltage ，因此具有無限大的 input impedance 與 0 output impedance

![[Ideal Voltage Amplifier.png]]

$A$: Voltage Gain

## Ideal Current Amplifier

需要檢測 short-circuit current 並產生放大後的 current ，因此有 0 input impedance 和無限大的 output impedance

![[Ideal Current Amplifier.png]]

## Ideal Transconductance Amplifier

[[#Transconductance Amplifier]]

檢測 $v_{ oc }$ 並產生正比於 $v_{ oc }$ 的電流，因此有無限大的 input impedance 和無限大的 output impedance

## Ideal Transresisstance Amplifier

檢測 $i_{ sc }$ 並產生正比於 $i_{ sc }$ 的電壓，因此有 0 input impedance 和 0 output impedance

## Practical Current Amplifier

![[Practical Current Amp.png]]

# Frequency Response

在交流電的情況下， gain parameter of amplifier 不會是常數，因此 gain parameter 有更廣義的定義

$$A_v = \frac{ {\bf V}_o }{ {\bf V}_i }$$

${\bf V}_o$: 輸出電壓 phasor
${\bf V}_i$: 輸入電壓 phasor
$A_v$: complex gain of amplifier

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

$$i_1 = \frac{ v_{ in } }{ R_1 }$$

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

if $r_1 = r_2$

$$v_o = \frac{ R_F }{ R_1 }(v_2 - v_1)$$

---

參考資料:

電工學 2022-03-07

---

link:

