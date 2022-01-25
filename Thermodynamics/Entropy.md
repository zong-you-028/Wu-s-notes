標籤: #Thermodynamics 

---

> content:
> - [[#Definition]]
> - [[#Entropy of a Pure Substance]]
> - [[#Entropy Change in Reversible Process]]
>     - [[#Carnot Cycle T-s diagram]]
>     - [[#Reversed Carnot Cycle]]
> - [[#Entropy of a Solid or Liquid]]
> - [[#Entropy Change of an Ideal gas]]

- A thermodynamic property
- $T = 0K$, $s = 0$
- molecular disorder or randomness

# Definition

$$ds = (\frac{ \delta Q }{ T })_{ rev }$$

$s$: Entropy

or

$$\delta Q = Tds$$

$$\Delta s = \underbrace{ s_2 - s_1 }_{ \text{ check table } } = \int_1^2\frac{ \delta Q }{ T }$$

# Entropy of a [[Pure Substance]]

Saturated:

$$s = (1 - x)s_f + xs_g$$
$$s = s_f + xs_{ fg }$$

# Entropy Change in Reversible Process

## [[Carnot Cycle]] (T-s diagram)

1. Isothermal Expansion (Heating)
2. Adiabatic Expansion
3. Isothermal Compression (Cooling)
4. Adiabatic Compression

![[Carnot Cycle T-s Diagram.png]]

$$s_2 - s_1 = \int_1^2(\frac{ \delta Q }{ T })_{ rev } = \frac{ _1Q_2 }{ T_H }$$

$$s_4 - s_3 = \int_3^4(\frac{ \delta Q }{ T })_{ rev } = \frac{_3Q_4}{ T_L }$$

$(2 \rightarrow 3), (4 \rightarrow 1)$ is reversible, adiabatic $\implies$ entropy remains constant (isentropic process)

## Reversed [[Carnot Cycle]]

Refrigerator or Heat Pump

![[Reversed Carnot Cycle T-s Diagram.png]]

$$Q_H = W + Q_L$$

- consider a reversible heat transfer process

![[Reversible Heat Transfer Process.png]]

$$s_2 - s_1 = s_{ fg }$$

$$ = \frac{ 1 }{ m }\int_1^2(\frac{ \delta Q }{ T })$$

$$ = \frac{ 1 }{ mT }\int_1^2\delta Q$$

$$ = \frac{ _1q_2 }{ T } = s_2 - s_1$$

$$ = \frac{ h_{ fg } }{ T }$$

.

$$_2q_3 = \frac{ 1 }{ m }\int_2^3\delta Q = \frac{ 1 }{ m }\int_2^3 Tds$$

- Area under T-s diagram represents the quantity of heat transfer in reversible process

# Entropy of a Solid or Liquid

for solid or liquid

$$dh = du + d(P\underbrace{ \nu }_{ \text{ const } })$$

$$\approx du + \underbrace{ \nu }_{ \text{ very small (neglect) } } dP$$

$$\approx du$$

$$\approx \underbrace{ c }_{ \text{ specific heat } }dT$$

$$\therefore dh \approx du = cdT$$

From [[Gibbs Function]]:
$$Tds = du + P\underbrace{ d\nu }_{ \approx 0 }$$

$$\therefore ds \approx \frac{ du }{ T } = \frac{ c }{ T }dT$$

$$\implies \int_1^2 ds = \int_1^2\frac{ c }{ T }dT$$

$$\implies \underline{ s_2 - s_1 = c\ln(\frac{ T_2 }{ T_1 }) }_{ \# } \qquad \text{ for solid or liquid only }$$

# Entropy Change of an Ideal gas

1. From [[Gibbs Function]]:
$$Tds = du + Pd\nu$$

$$\implies ds = \frac{ du }{ T } + \frac{ P }{ T }d\nu$$

$$
\text{ From }
\left\{
	\begin{array}{l}
		du = c_vdT \\
		\text{ ideal gas } \frac{ P }{ T } = \frac{ R }{ \nu }
	\end{array}
\right.
$$

$$\implies ds = c_v\frac{ dT }{ T } + \frac{ P }{ \nu }d\nu$$

integrate each side

$$\underline{ s_2 - s_1 = \int_1^2 c_v\frac{ dT }{ T } + R\ln\frac{ \nu_2 }{ \nu_1 } }_{ \# }$$

---

參考資料:

[劉耀先熱力學OCW](https://youtube.com/playlist?list=PLj6E8qlqmkFt83RMhWiOggy669xF9Z3aA)

---

link:

[[Saturated liquid-vapor mixture]]