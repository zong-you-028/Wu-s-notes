標籤: #電工學 

---

Dielectric Constant $\epsilon$

$$\epsilon = \underbrace{ \epsilon_0 }_{ \text{ air } } \cdot \underbrace{ \epsilon_r }_{ \text{ relativity } }$$

$C$: 電容 Capacitance (Unit: Faraday)

$$C = \epsilon\frac{ A }{ d }$$

# Properties

## Stored Charge in Terms of Voltage

In an ideal capacitor, the stored charge $q$ is proportional to the voltage berween the plates:

$$q = Cv$$


## Current in Terms of Voltage

Current is the time rate of flow of charge

$$i = \frac{ dq }{ dt } = \frac d { dt }(Cv)$$

$$\implies \underline{ 
	i = C\frac{ dv }{ dt } 
}_{ \# }$$

## Voltage in Terms of Current

$$q(t) = \int_{ t_0 }^t i(t)dt + q(t_0)$$

$$\implies Cv(t) = 
\int_{ t_0 }^t i(t)dt + q(t_0)$$

$$\implies v(t) = 
\frac 1 C \int_{ t_0 }^t i(t)dt + 
\frac{ q(t_0) }{ C }$$

$$\implies 
\underline{
	v(t) = 
	\frac 1 C \int_{ t_0 }^t i(t)dt + 
	v(t_0)
}_{ \# }$$

## Stored Energy

$$p(t) = v(t)i(t)$$

> use [[#Current in Terms of Voltage]]
> $$i = C \frac{ dv }{ dt }$$

$$\implies p(t) = Cv \frac{ dv }{ dt }$$

$$w(t) = \int_{ t_0 }^t p(t)dt$$

$$\implies w(t) = 
\int_{ t_0 }^t Cv \frac{ dv }{ dt }dt$$

$$\implies w(t) = \int_0^{ v(t) } Cvdv$$

$$\implies \underline{ 
	w(t) = \frac 1 2 C v^2(t)
}_{ \# }$$

> [[#Stored Charge in Terms of Voltage]]:
> $$q = Cv$$

$$\implies \underline{ 
	w(t) = \frac 1 2 v(t)q(t)
}_{ \# }$$

$$\implies \underline{ 
	w(t) = \frac{ q^2(t) }{ 2C } 
}_{ \# }$$

## Parallel

![[Parallel.png]]

$$
i = C_{ eq }(\frac{ dv }{ dt }) = 
\underbrace{ C_1 (\frac{ dv }{ dt }) }_{ i_1 } + \underbrace{ C_2(\frac{ dv }{ dt }) }_{ i_2 }
$$

$$C_{ eq } = C_1 + C_2$$

## Series

![[Series.png]]

$$\frac{ \int idt }{ C_{ eq } } = \frac{ \int idt }{ C_1 } + \frac{ \int idt }{ C_2 }$$

$$C_{ eq } = \frac{ C_1C_2 }{ C_1 + C_2 }$$

# Scenario

## Energy Conservation After Charge Redistribution

![[energy conservation after charge redistribution.png]]

$$E_{ before } = \frac{ 1 }{ 2 }C_1v_1^2$$

$$Q = C_1v_1$$

![[energy conservation after charge redistribution 2.png]]

$$v_{ after } = \frac{ Q_1 }{ C_1 } = \frac{ Q_2 }{ C_2 }$$

$$\frac{ c_1q }{ C_1 } = \frac{ c_2q }{ C_2 }$$

$$c_1q + c_2q = Q = C_1 v_1$$

$$q = \frac{ C_1 }{ c_1 + c_2 }v_1$$

$$v_{ after } = \frac{ Q_1 }{ C_1 } = \frac{ c_1 }{ c_1 + c_2 }v_1$$

$$E_{ after } = \frac{ 1 }{ 2 }(c_1 + c_2)\left( \frac{ c_1 }{ c_1 + c_2 }v_1 \right)^2 = \frac{ 1 }{ 2 }\frac{ c_1^2 }{ c_1 + c_2 }v_1^2$$

## OpAmp Circuit

![[OpAmp Circuit.png]]

$$v_{ out } = \frac{ 1 }{ C }\int(\frac{ v_{ in } }{ R })dt$$

$$v_{ out } = \frac{ 1 }{ RC }\int v_{ in }dt$$

---

參考資料:

電工學上課

---

link:

[[Amplifier]]