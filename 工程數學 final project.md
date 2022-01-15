標籤: #工程數學 

---

# Section 1: Observing ODE in Real Life

## 1.

$$\sum{ F } = -ky - c\frac{ dy }{ dt } + F_{ external } = m \frac{ d^2 y }{ dt^2 }$$

## 3. i.

![[Mass spring damper.png]]

Above is a tuned mass damper for a building. The mass damper system on the building structure will protect the building from disastrous earthquake.

## 3. ii.

Newton's second law:
$$F = ma$$
$F$: force
$m$: mass
$a$: acceleration

---

Hooke's law for linear springs:
$$F_s = kx$$
$F_s$: force of spring
$k$: spring constant
$x$: displacement of the free end of the spring

---



## 3. iii.

In [this paper](https://s3.us-east-2.amazonaws.com/elasticbeanstalk-us-east-2-856193192518/files/me321/me321project3.pdf), it mentioned the parameters of Taipei 101.

$$
\left\{
	\begin{array}{l}
		m & = & 660000kg \\
		k & = & 111880kN/m \\
		c & = & 2000kNs/m \\
	\end{array}
\right.
$$

Assume $\theta$ is very small, and the height $H$ remain constant, so the damper and springs have horizontal movement only. We can use the ODE we write at [[#1]].

$$\sum{ F } = -ky - c\frac{ dy }{ dt } + F_{ external } = m \frac{ d^2 y }{ dt^2 }$$

In our case, $F_{ external }$ is the tension of the string, which has small influence that we will neglect.

$$-ky - c\frac{ dy }{ dt } = m \frac{ d^2 y }{ dt^2 }$$

Use the parameters above and substitude into our ODE.

$$-111880000y - 2000000\frac{ dy }{ dt } = 660000 \cdot \frac{ d^2y }{ dt^2 }$$

## 3. iv.

With [the paper](https://s3.us-east-2.amazonaws.com/elasticbeanstalk-us-east-2-856193192518/files/me321/me321project3.pdf)

## 3. v.

In most case, the tuned mass damper stays at $y = 0$. Also, we assume the oscillation is a sine wave with a frequency of $10Hz$:

$$
\begin{array}{}
y = 0 \text{ at } t = 0 \\
y' = \frac{ 1 }{ 20\pi } \text{ at } t = 0
\end{array}
$$

# Section 2: Solving the ODE using "Traditional Technique"

## 1. 

Assume the building encounters a forcing with $250gal\;(250m/s^2)$

$$F_{ forcing } = m \cdot 2.5 \times \sin\frac{ 1 }{ 20\pi }t$$
$$\implies F_{ forcing } = 6.6\times 10^5 \cdot 2.5 \times \sin\frac{ 1 }{ 20\pi }t$$

## 2.

$$6.6\times 10^5 y'' + 2 \times 10^6 y' + 1.1188 \times 10^8 y = 6.6 \times 10^5 \times 2.5 \times \sin\frac{ 1 }{ 20\pi }t$$

## 3.

$y_h$ part
$$6.6 \times 10^5 y'' + 2 \times 10^6 y' + 1.1188 \times 10^8 y = 0$$
$$\implies y'' + 3.03y' + 1.7 \times 10^2y = 0$$
$$
\text{ let } \quad
\begin{array}{l}
	y & = & e^{ \lambda x } \\
	y' & = & \lambda e^{ \lambda x } \\
	y'' & = & \lambda^2 e^{ \lambda x }
\end{array}
\text{ (characteristic equation) }
$$
$$\overset{ \text{ into ODE } }{ \implies } \lambda^2 + 3.03\lambda + 1.7 \times 10^2 = 0$$

$$
\begin{array}{}
	\lambda_1 = -7.435 \\
	\lambda_2 = -22.865
\end{array}
$$

$$\implies y_h = c_1e^{ -7.435t } + c_2e^{ -22.865t }$$

$y_p$ part

$$\overset{ \text{ ODE } }{ \implies } y'' + 3.03y' + 1.7 \times 10^2 y = 2.5 \times \sin\frac{ t }{ 20\pi }$$
$$y_p \text{ form: } K\cos\frac{ 1 }{ 20\pi } + M\sin\frac{ 1 }{ 20\pi }t \qquad \text{ (Undertermined Coefficients) }$$
$$\implies 
\begin{array}{}
y_p & = & K\cos\frac{ 1 }{ 20\pi }t + M\sin\frac{ 1 }{ 20\pi }t \\
y_p' & = & -\frac{ 1 }{ 20\pi }K\sin\frac{ 1 }{ 20\pi } + \frac{ 1 }{ 20\pi }\cos\frac{ 1 }{ 20\pi }t \\
y_p'' & = & -\frac{ 1 }{ 400 \pi^2 }K\cos\frac{ 1 }{ 20\pi }t - \frac{ 1 }{ 400\pi^2 }M\sin\frac{ 1 }{ 20\pi }t
\end{array}{}
$$

$$
\begin{array}{}
	(-\frac{ 1 }{ 400\pi^2 } + 3.03\times \frac{ 1 }{ 20\pi } + 170)K\cos\frac{ 1 }{ 20\pi }t + (-\frac{ 1 }{ 400\pi^2 } - 3.03 \times \frac{ 1 }{ 20\pi } + 170)M\sin\frac{ 1 }{ 20\pi }t \\
	\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad = 2.5\sin\frac{ 1 }{ 20\pi }t
\end{array}
$$

$$
\implies
\left\{
	\begin{array}{l}
		K = 0 \\
		M = 0.0147
	\end{array}
\right.
$$

$$y_p = 0.0147\sin\frac{ 1 }{ 20\pi }t$$

$$y(t) = y_h + y_p = c_1e^{ -7.435t } + c_2e^{ -22.865t } + 0.0147\sin\frac{ 1 }{ 20\pi }t$$

## 4.

$$\text{ IVP } \qquad y(0) = 0 \quad y'(0) = \frac{ 1 }{ 20\pi }$$

$$
\implies 
\left\{
	\begin{array}{}
		c_1 & + & c_2 & = & 0 \\
		-7.435c_1 & - & 22.865c_2 & = & -\frac{ 1 }{ 20\pi } \times 0.0147
	\end{array}
\right.
$$

$$
\implies 
\left\{
	\begin{array}{}
		c_1 & = & -1.516 \times 10^{ -5 } \\
		c_2 & = & 1.516 \times 10^{ -5 }
	\end{array}
\right.
$$

$$\implies y(t) = -1.516\times 10^{ -5 } \times e^{ -7.435t } + 1.516 \times 10^{ -5 } \times e^{ -22.865t } + 0.0147 \sin\frac{ 1 }{ 20\pi }t$$

## 5.

![[earthquake diagram.png]]