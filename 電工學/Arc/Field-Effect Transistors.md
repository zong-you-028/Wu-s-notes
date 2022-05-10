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

---

參考資料:

課本

---

link:

