標籤: #電工學 

---

# NMOS and PMOS Transistors

## NMOS Transistors

![[n channel mosfet.png]]

$D$: drain
$G$: gate
$S$: source
$B$: body (substrate)

When a sufficiently large (positive) voltage is applied to the gate relative to the source, electrons are attracted to the region under the gate, and a channel of *n*-type material is induced between the drain and the source.

Drain current is controlled by the voltage applied to the gate.

### Circuit Symbol

![[circuit symbol of nmos transistor.png|250]]

### Operation

根據給 gate 與 drain 的電壓不同，通過 nmos 的電流可以分成以下三種情況

- cutoff region
- triode region
- saturation region

#### Cutoff Region

當給 gate 的電壓 $v_{ GS }$ 不夠大的時候會發生，這時 drain 和 source 會是斷路狀態

$$\text{ when } v_{ GS } \leq V_{ to } \qquad i_D = 0$$

我們稱 $V_{ to }$ 為 threshold voltage

![[mosfet operation in cutoff region.png]]

#### Triode Region

當給 gate 的電壓 $v_{ GS }$ 足夠大時 drain 和 source 就會導通，此時如果在 drain 和 source 之間給一個小的電壓 $v_{ DS }$ (必須足夠小)，會開始產生電流通過。

$$
\begin{array}{}
	\text{ when } & v_{ DS } < v_{ GS } - V_{ to }\\
	& v_{ GS } \geq V_{ to }
\end{array}
$$

$$i_D = K[\ 2(V_{ GS } - V_{ to })v_{ DS } - v^2_{ DS } \ ]$$

$$K = \left( \frac W L \right) \frac{ KP }{ 2 }$$

- $W$: width of channel
- $L$: length of channel
- $KP$: device parameter, depends on the thickness of the oxide layer and certain properties of the channel material. a typical value is $50\mu\text A / \text V^2$

![[mosfet operation in the triode region.png]]

#### Saturation Region

當進入了 triode region 並且逐漸加大 drain 與 source 間的電壓 $v_{ DS }$ 大過一定程度就會進入 saturaion region，此時的電流 $i_D$ 不論 $v_{ DS }$ 如何改變都是固定的

$$i_D = K(v_{ GS } - V_{ to })$$

![[mosfet operation in saturation region.png]]

![[characteristic curves of nmos.png]]

#### Boundary Between Triode and Saturation Regions

At this boundary, the channel thickness at the drain is zero, which occurs when $v_{ GD } = V_{ to }$

$$v_{ GD } = V_{ to }$$

$$\implies v_{ GS } - v_{ DS } = V_{ to }$$

$$\implies v_{ GS } - V_{ to } = v_{ DS }$$

substitude into equation of saturation region

> equation of saturation region
> $$i_D = K(v_{ GS } - V_{ to })$$

$$\implies \underline{ 
	i_D = Kv^2_{ DS }
}_\#$$

Notice that the boundary between the triode region and the saturation region is a parabola

#### Equivalent Resistance

$$R_D = 
\left.
	\frac{ \partial v_{ DS } }{ \partial i_D }
\right\vert_{ v_{ GS } \text{ const } }$$

$R_D$ is preferred to be very small ($100 \text m \Omega \sim 10\text m \Omega$)

我們會取 $v_{DS} = 0$ 附近的等效電阻

$$ = \left.
	\frac{ 1 }{ \frac{ \partial i_D }{ \partial v_{ DS } } }
\right\vert_{ v_{ DS } = 0 }$$

$$ = \underline{\frac{ 1 }{ 2K(v_{ GS } - v_{ to }) }}_\#$$

## PMOS Transistors

MOSFETs can also be constructed by interchanging the $n$ and $p$ regions of $n$-channel devices, resulting in $p$-channel devices.

![[circuit symbol for pmos transistor.png|300]]

As indicated in the figure, we usually orient the $p$-channel FETs with the source at the top and reference the current out of the drain.

## Summary

|                            | NMOS                                                                                                                                      | PMOS                                                                                                                                      |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| Circuit Symbol             | ![[circuit symbol of nmos transistor.png]]                                                                                                | ![[circuit symbol for pmos transistor.png]]                                                                                               |
| $KP$ (typical value)       | $$50 \mu \text A / \text V^2$$                                                                                                            | $$25 \mu \text A / \text V^2$$                                                                                                            |
| $K$                        | $$\left( \frac 1 2 \right)KP \left(\frac W L\right)$$                                                                                     | $$\left( \frac 1 2 \right)KP \left(\frac W L\right)$$                                                                                     |
| $V_{ to }$ (typical value) | $$+1 \text V$$                                                                                                                            | $$-1 \text V$$                                                                                                                            |
| Cutoff region              | $$v_{ GS } \leq V_{ to }$$ $$i_D = 0$$                                                                                                    | $$v_{ GS } \geq V_{ to }$$ $$i_D = 0$$                                                                                                    |
| Triode region              | $$v_{ GS } \geq V_{ to } \text{ and } 0 \leq v_{ DS } \leq v_{ GS } - V_{ to }$$ $$i_D = K[2(v_{ GS } - V_{ to })v_{ DS } - v_{ DS }^2]$$ | $$v_{ GS } \leq V_{ to } \text{ and } 0 \geq v_{ DS } \geq v_{ GS } - V_{ to }$$ $$i_D = K[2(v_{ GS } - V_{ to })v_{ DS } - v_{ DS }^2]$$ |
| Saturation region          | $$v_{ GS } \geq V_{ to } \text{ and } v_{ DS } \geq v_{ GS } - V_{ to }$$ $$i_D = K(v_{ GS } - V_{ to })^2$$                              | $$v_{ GS } \leq V_{ to } \text{ and } v_{ DS } \leq v_{ GS } - V_{ to }$$ $$i_D = K(v_{ GS } - V_{ to })^2$$                              |
| $v_{ DS }$ and $v_{ GS }$  | Normally assume positive values                                                                                                           | Normally assume negative values                                                                                                           | 

# Load-Line Analysis

![[load-line analysis.png]]

對於上圖的兩個 loop 分別列出 KVL

$$
\left\{
	\begin{array}{}
		v_{ GS }(t) = v_{ in }(t) + V_{ GG } \\
		\underline{V_{ DD } = R_D i_D(t) + v_{ DS }(t)}_\#
	\end{array}
\right.$$

我們將第二條式子畫出的線稱為 load-line ，並且我們會把他畫在圖上。

譬如上圖的情況，我們會將 $R_D = 1\text k\Omega, V_{DD} = 20 \text V$ 代入

$$\implies 20 = i_D(t) + v_{ DS }$$

注意 $i_D$ 的單位是 $\text{mA}$ ，並且我們可以根據這個方程式在圖表上畫出 load line

> ## Quiescent Operating Point
> 
> 我們把 $v_{ in } = 0$ 的點稱為 quiescent operating point ，或者 Q point
> 
> 譬如上圖中，如果 $v_{in}(t) = 0$ ，$v_{GS} = v_{DD} = 4\text V$ 。我們可以在圖表上看到 $v_{ GS } = 4 \text V$ 的線與 load line 就是 Q point

接著我們把 $v_{ in }(t) = \sin(2000\pi t)$ 加入，並且看看 $v_{ GS }$ 與 $v_{ DS }$ 的關係。我們可以使用 load line 來幫助我們看出來。結果如下：

![[inverting amplifier using mos.png]]

我們發現這是一個 inverting amplifier ，但是注意結果其實並不是 $\sin$ 波。從 field line 可以發現，高點、低點與中間點的電壓如下

| 點              | $$v_{ GS }$$  | $$v_{ DS }$$   |
| --------------- | ------------- | -------------- |
| $v_{ DS }$ 高點 | $$3 \text V$$ | $16 \text V$   |
| 中間點          | $$4 \text V$$ | $$11 \text V$$ |
| $v_{ DS }$ 低點 | $$5 \text V$$ | $$4 \text V$$  | 

對於 $v_{DS}$ ，高點與中間點相差 $5 \text V$ ，中間點與低點相差 $7 \text V$ ，因此這個 amplifier 做的是非線性的放大。

# Bias Circuits

上面提到的 Amplifier Circuit 有許多缺點，譬如需要兩個電池、 Q point 不會在中間等問題，並且選擇的元件（如電阻）必須要非常精準，因此有了改良的版本。 bias circuit 容許不是很精準的零件。

## The Fixed- plus Self-Bias Circuit

The fixed- plus self-bias circuit shown in Figure(a) is a good circuit for establishing Q points that are relatively independent of device parameters

![[fixed- plus self-bias circuit.png|400]]

為了分析，我們把 (a) 做 Thevenin Equivalent Circuit 變成 (b) ，其中

$$V_G = V_{ DD } \frac{ R_2 }{ R_1 + R_2 }$$

$$R_G = R_1 \vert \vert R_2$$

對於 (b) 的 loop 寫出 KVL

$$V_G = v_{ GS } + R_Si_D$$

並且使用 transistor 的 saturation region （我們通常會希望使用 saturation region）

$$i_D = K(v_{ GS } - V_{ to })^2$$

根據上面兩條式子，畫出 $i_D$ 對 $v_{GS}$ 的圖，可以得出 Q point

![[graphical solution of fixed plus self bias circuit.png|450]]

最後，還有 drain loop 的 equation 來求出 $v_{DS}$

$$v_{DS} = V_{DD} - (R_D + R_S) i_D$$

---

參考資料:

課本

---

link:

