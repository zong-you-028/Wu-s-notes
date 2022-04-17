標籤: #電工學 

---

# Power Calculations for a General Load

對於任何 [[RLC Circuit]] ，我們有以下三條式子

$$
\begin{array}{}
	v(t) & = & V_m \cos(\omega t) \\
	i(t) & = & I_m \cos(\omega t - \theta) \\
	p(t) & = & 
	V_m I_m \cos(\omega t) \cos(\omega t - \theta)
\end{array}
$$

> [[Trigonometric Identity]]:
> $$\cos(\alpha \pm \beta) = \cos\alpha\cos\beta\mp\sin\alpha\sin\beta$$
> $$\implies \cos(\omega t - \theta) = \cos(\theta) \cos(\omega t) + \sin(\theta)\sin(\omega t)$$

$$\implies p(t) = 
V_mI_m\cos(\theta)\cos^2(\omega t) + 
V_m I_m \sin (\theta)\cos(\omega t)\sin(\omega t)$$

> [[Trigonometric Identity]]:
> $$\cos^2(\omega t) = \frac 1 2 + \frac 1 2 \cos(2\omega t)$$
> $$\cos(\omega t)\sin(\omega t) = \frac 1 2 \sin(2\omega t)$$

$$p(t) = \frac{ V_m I_m }{ 2 }\cos(\theta)[1 + \cos(2\omega t)] + \frac{ V_m I_m }{ 2 }\sin(\theta)\sin(2\omega t)$$

$$P = \frac{ V_m I_m }{ 2 } \cos (\theta)$$

$$P = \underline{ V_{ rms } I_{ rms }\cos(\theta) }_{ \# }$$

$P$: average power

## Power Factor

$${ \bf PF } = \cos(\theta)$$

$$\theta = \theta_v - \theta_i$$

$\theta_v$: phase of voltage
$\theta_i$: phase of current

---

參考資料:

課本

---

link:

[[AC Circuit]]
[[RLC Circuit]]