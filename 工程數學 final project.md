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

# Section 3: Solving the ODE using Laplace Transform

## 1.

$$6.6\times 10^5 y'' + 2 \times 10^6 y' + 1.1188 \times 10^8y = 1.65 \times 10^7 \times \sin(\frac{ t }{ 20\pi })$$

$$y(0) = 0, \qquad y'(0) = \frac{ 1 }{ 2\pi }$$

$$\implies 6.6\times 10^5 \mathscr{ L }\{ y'' \} + 2 \times 10^6 \mathscr{ L }\{ y' \} + 1.1188 \times 10^8 \mathscr{ L }\{ y \} = 1.65 \times 10^7 \mathscr{ L }\left\{ \sin\frac{ t }{ 20\pi } \right\}$$

$$\implies Y( 6.6 \times 10^5 s^2 + 2 \times 10^6s + 1.1188 \times 10^8 ) = \frac{ \frac{ 8.25 }{ \pi } \times 10^5 }{ s^2 + \frac{ 1 }{ 400\pi^2 } } + \frac{ 6.6 \times 10^5 }{ 20\pi }$$

$$\implies Y = \frac{ 2.62606 \times 10^5 + \frac{ 6.6 \times 10^5 }{  20 \pi} ( s^2 + \frac{ 1 }{ 400\pi^2 } ) }{ s^2 + \frac{ 1 }{ 400\pi^2 } } \times \frac{ 1 }{ 6.6 \times 10^5s^2 + 2 \times 10^6s + 1.1188 \times 10^8 }$$

$$\implies Y = \frac{ 262606.0007 + 2.66075s^2 }{ ( s^2 + \frac{ 1 }{ 400 \pi^2 } )( 6.6\times 10^5s^2 + 2\times 10^6s + 1.1188 \times 10^8 ) }$$

$$= \frac{ As + B }{ s^2 + \frac{ 1 }{ 400\pi^2 } } + \frac{ Cs + D }{ 6.6 \times 10^5s^2 + 2 \times 10^6s + 1.1188 \times 10^8 }$$

$$
\implies
\left\{
	\begin{array}{rcc}
		(6.6 \times 10^5A + C)s^3 & = & 0 \\
		(2 \times 10^6 + 6.6 \times 10^5B + D)s^2 & = & 2.66075s^2 \\
		(1.1188 \times 10^8 A + 2 \times 10^6B + \frac{ C }{ 400\pi^2 })s & = & 0 \\
		(1.1188 \times 10^8B + \frac{ D }{ 400\pi^2 }) & = & 262606.0007
	\end{array}
\right.
$$

$$
\implies 
\left\{
	\begin{array}{}
		A & = & -0.00040 \\
		B & = & 0.02211 \\
		C & = & 260.80512 \\
		D & = & -13796.43713
	\end{array}
\right.
$$

$$
\implies
Y = 
\frac{ -0.0004s }{ s^2 + \frac{ 1 }{ 400\pi^2 } } +
1.38921 \times \frac{ \frac{ 1 }{ 20\pi } }{ s^2 + \frac{ 1 }{ 400\pi^2 } } + 
\frac{ 260.80512s - 13796.43713 }{ 6.6 \times 10^5s^2 + 2 \times 10^6 + 1.1188 \times 10^8 }
$$

$$ = -0.0004\mathscr{ L }\left\{ \cos\frac{ t }{ 20\pi } \right\} + 1.38921 \mathscr{ L }\left\{ \sin\frac{ t }{ 20\pi } \right\} + \frac{ 3.95159 \times 10^{ -4 }s - 0.02090 }{ s^2 + \frac{ 100s }{ 33 } + \frac{ 5594 }{ 33 } }$$

$$
\begin{array}{}
= -0.0004\mathscr{ L }\left\{ \cos\frac{ t }{ 20\pi } \right\} + 1.38921 \mathscr{ L }\left\{ \sin\frac{ t }{ 20\pi } \right\} + \frac{ 3.95159 \times 10^{ -4 } ( s + \frac{ 50 }{ 33 } ) }{ ( s + \frac{ 50 }{ 33 } )^2 + 167.21947 } \\
\qquad\qquad\qquad\qquad\qquad\qquad\qquad - 1.28566 \times 10^{ -4 } \times \frac{ 167.21947 }{ ( s + \frac{ 50 }{ 33 } ) + 167.21947 }
\end{array}
$$

$$
\begin{array}{}
= -0.0004 \mathscr{ L }\left\{ \cos\frac{ t }{ 20\pi } \right\} + 1.38921 \mathscr{ L }\left\{ \sin\frac{ t }{ 20\pi } \right\} + 3.95159\times 10^{ -4 }\mathscr{ L }\left\{ e^{ -\frac{ 50 }{ 33 }t }\cos(167.21947t) \right\} \\
\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad - 1.28566 \times 10^{ -4 }\mathscr{ L }\left\{ e^{ -\frac{ 50 }{ 33 }t }\sin(167.21947t) \right\}
\end{array}
$$

$$
\begin{array}{}
\implies y(t) = \underline{ -0.0004\cos\frac{ t }{ 20\pi } + 1.38921\sin\frac{ t }{ 20\pi } + 3.95159\times 10^4 e^{ -\frac{ 50 }{ 33 }t }\cos(167.21947t) } \\ 
\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\underline{ - 1.28566\times 10^{ -4 } e^{ -\frac{ 50 }{ 33 }t }\sin( 167.21947t ) }_{ \# }
\end{array}
$$