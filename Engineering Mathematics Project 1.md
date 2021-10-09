# Engineering Mathematics Project 1

> Group: iTron
> Members: 
> 趙珈毅 109611010
> 陳柏文 109611030
> 張瀚元 109611004
> 吳典謀 109611066

## Section 1

> $$\text{Bernoulli: }\; y' + P(x)y = r(x)y^\alpha$$
> $$\text{Logistics equation: }\; y' = Ay - By^2$$

---

$$\text{1. }\; \frac{dy}{dt} = Ay - By^2$$
$$\implies \frac{1}{Ay - By^2}dy = dt$$
$$\implies \frac{1}{Ay(1 - \frac{B}{A}y)}dy = dt$$
$$\implies \frac{1}{A}\left[ \int\frac{1}{y}dy + \int \frac{\frac{B}{A}}{(1 - \frac{B}{A}y)}dy \right] = \int dt$$
$$\implies \frac{1}{A}\left[ \ln y - \ln(1 - \frac{B}{A}y) \right] = t + c_1$$
$$\implies\ln\frac{y}{1 - \frac{B}{A}y} = At + c_2$$
$$\implies\frac{y}{1 - \frac{B}{A}y} = c_3e^{At}$$
$$\implies y(1 + \frac{B}{A}ce^{At}) = c_3e^{At}$$
$$\implies y = \frac{c_3e^{At}}{1 + \frac{B}{A}c_3e^{At} } = \underline{\frac{1}{ce^{-At} + \frac{B}{A}}}_{\#}$$

---

$$\text{2. }\; B = 0$$
$$\implies y' = Ay$$
$$\implies \frac{dy}{dt} = Ay$$
$$\implies \frac{dy}{y} = Adt$$
$$\implies \ln y = At + c_1$$
$$\implies y = e^{At + c_1} = \underline{ce^{At}}_{\#}$$
$$\implies \text{They are the same.}$$

---

$$\text{3.}\; y(t) = \frac{1}{ce^{-At} + \frac{B}{A}}$$
$$\text{when }\; B = 0$$
$$\implies y(t) = \frac{1}{ce^{-At}} = ce^{At}$$
$$\implies \text{They are the same}$$

---

$$\text{4. }\; y = Ay - By^2$$
$$y(t) = \frac{1}{ce^{-At} + \frac{B}{A}}$$
$$\lim_{t\rightarrow\infty}y(t) = \frac{A}{B}$$
$$\text{so when }\; t \rightarrow \infty , \; y(t) \;\text{ will converge to }\frac{A}{B}$$
$$y(t) \text{ will brake to } \frac{A}{B}, \; \text{so }-By^2 \text{ is called braking term}$$



---

$$\text{5. }\; y(t_0) = y_0 = \frac{1}{ce^{-At_0}+\frac{B}{A}}$$
$$\implies \frac{1}{y_0} = ce^{-At_0} + \frac{B}{A}$$
$$\implies \frac{1}{y_0} - \frac{B}{A} = ce^{-At_0}$$
$$\implies (\frac{1}{y_0} - \frac{B}{A})e^{At_0} = \underline{c}_{\#}$$

---

$$\text{6. }y = 1000e^{0.5t}$$
![[y=1000e^{0.5x}.png]]

---

$$\text{7. }$$
![[compare chart 1.7.png]]

---

$$\text{8. }\lim_{t \rightarrow \infty}ce^{-At}=0$$
$$\lim_{t \rightarrow\infty}y(t) = \lim_{t \rightarrow \infty}\frac{1}{0 + \frac{1}{4}} = \underline{4}_{\#}$$
$$\text{when }\; t \; \text{ approach }\infty \text{ , }\;y\;\text{ converge to }\frac{A}{B}$$
![[1.8 compare.png]]

---

$$\text{9.\ \ \ (3).}$$
![[positive.png]]

---

$$\text{9.\ \ \ (4).}$$
![[model compare.png]]
$$\text{Verhulst Model is more appropriate.}$$
$$\text{Because the model converges when the cases reach 30 millions.}$$

---

$$\text{9.\ \ \ (5).}$$
$$y(t) = \frac{1}{ce^{-At} + \frac{B}{A}} \quad \text{---(1)}$$
$$y(t_f) \approx \frac{A}{B} = 2.9 \times 10^7$$
$$\implies y(0) = \frac{1}{c + \frac{B}{A}} = 1$$
$$\implies c = 1 - 2.9 \times 10^{-7} \doteqdot 1$$
$$c = 1 \;\text{代回 (1)}$$
$$\implies y(t) = \frac{1}{e^{-At} + \frac{B}{A}}$$
$$t = 347 \implies y(347) = 2 \times 10^7 = \frac{1}{e^{-A \times 347} + \frac{1}{2.9 \times 10^{-7}}}$$
$$\implies A = \underline{0.0518}_{\#}$$
$$\implies B = \underline{1.79 \times 10^{-9}}_{\#}$$

---