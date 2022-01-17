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

$$6.6\times 10^5 y'' + 2 \times 10^6 y' + 1.1188 \times 10^8 y = 1.65 \times 10^7 \times \sin\frac{ t }{ 20\pi }$$

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
	\lambda_1 = -1.515 + 12.9501i \\
	\lambda_2 = -1.515 - 12.9501i
\end{array}
$$

$$\implies y_h = e^{ 1.515t }(A\cos 12.9501t + B\sin 12.9501t)$$

$y_p$ part

$$\overset{ \text{ ODE } }{ \implies } y'' + 3.03y' + 1.7 \times 10^2 y = 2.5 \times \sin\frac{ t }{ 20\pi }$$
$$y_p \text{ form: } K\cos\frac{ 1 }{ 20\pi } + M\sin\frac{ 1 }{ 20\pi }t \qquad \text{ (Undertermined Coefficients) }$$
$$\implies 
\begin{array}{}
y_p & = & K\cos\frac{ 1 }{ 20\pi }t + M\sin\frac{ 1 }{ 20\pi }t \\
y_p' & = & -\frac{ 1 }{ 20\pi }K\sin\frac{ 1 }{ 20\pi } + \frac{ 1 }{ 20\pi }M\cos\frac{ 1 }{ 20\pi }t \\
y_p'' & = & -\frac{ 1 }{ 400 \pi^2 }K\cos\frac{ 1 }{ 20\pi }t - \frac{ 1 }{ 400\pi^2 }M\sin\frac{ 1 }{ 20\pi }t
\end{array}{}
$$

$$
\begin{array}{}
\text{ ODE } \implies \left(\frac{ -K }{ 400\pi^2 } + 3.03 \times \frac{ M }{ 20\pi } + 170K\right)\cos\frac{ t }{ 20\pi } \\
\qquad\qquad\qquad\qquad\qquad\qquad+ \left( \frac{ -M }{ 400\pi^2 } - 3.03\times \frac{ K }{ 20\pi } + 170M \right)\sin\frac{ t }{ 20\pi } = 25\times \frac{ t }{ 20\pi }
\end{array}
$$

$$
\implies
\left\{
	\begin{array}{}
		-\frac{ K }{ 400\pi^2 } + 3.03 \times \frac{ M }{ 20\pi } + 170K = 0 \\
		\frac{ -M }{ 400\pi^2 } - 3.03\times \frac{ K }{ 20\pi } + 170M = 25
	\end{array}
\right.
$$

$$
\implies
\left\{
	\begin{array}{l}
		K = -4.17 \times 10^{ -5 } \\
		M = 0.147
	\end{array}
\right.
$$

$$
\begin{array}{}
y(t) = y_h + y_p = e^{ 1.515t }(A\cos12.9501t + B\sin12.9501t) - 4.17 \times 10^{ -5 }\cos\frac{ t }{ 20\pi } \\
\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad + 0.147 \times 10^{ -1 } \sin\frac{ t }{ 20\pi }
\end{array}
$$

## 4.

$$\text{ IVP } \qquad y(0) = 0 \quad y'(0) = \frac{ 1 }{ 20\pi }$$

$$
\implies 
\left\{
	\begin{array}{}
		A = 4.17 \times 10^{ -5 } = 0 \\
		1.515A + 12.950113 + \frac{ 0.147 }{ 20\pi } = \frac{ 1 }{ 20\pi }
	\end{array}
\right.
$$

$$
\implies 
\left\{
	\begin{array}{}
		A = 4.17 \times 10^{ -5 } \\
		B = 1.043 \times 10^{ -3 }
	\end{array}
\right.
$$

$$
\begin{array}{}
\implies y(t) = e^{ -1.515t }( 4.17 \times 10^{ -5 }\cos12.9501t + 1.043 \times 10^{ -3 }\sin 12.9501t ) \\
\qquad\qquad\qquad\qquad\qquad\qquad- 4.17 \times 10^{ -5 }\cos\frac{ t }{ 20\pi } + 1.47\times 10^{ -1 }\sin\frac{ 20\pi }{ t }
\end{array}
$$

## 5.

![[earth quake graph math project 3.png]]

# Section 3: Solving the ODE using Laplace Transform

## 1.

$$6.6\times 10^5 y'' + 2 \times 10^6 y' + 1.1188 \times 10^8y = 1.65 \times 10^7 \times \sin(\frac{ t }{ 20\pi })$$

$$y(0) = 0, \qquad y'(0) = \frac{ 1 }{ 2\pi }$$

$$
\begin{array}{}
\implies 6.6\times 10^5 \mathscr{ L }\{ y'' \} + 2 \times 10^6 \mathscr{ L }\{ y' \} + 1.1188 \times 10^8 \mathscr{ L }\{ y \} \\
\qquad\qquad\qquad\qquad\qquad\qquad\qquad= 1.65 \times 10^7 \mathscr{ L }\left\{ \sin\frac{ t }{ 20\pi } \right\}
\end{array}
$$

$$\implies Y( 6.6 \times 10^5 s^2 + 2 \times 10^6s + 1.1188 \times 10^8 ) = \frac{ \frac{ 8.25 }{ \pi } \times 10^5 }{ s^2 + \frac{ 1 }{ 400\pi^2 } } + \frac{ 6.6 \times 10^5 }{ 20\pi }$$

$$
\begin{array}{}
\implies Y = \frac{ 2.62606 \times 10^5 + \frac{ 6.6 \times 10^5 }{  20 \pi} ( s^2 + \frac{ 1 }{ 400\pi^2 } ) }{ s^2 + \frac{ 1 }{ 400\pi^2 } } \\
\qquad\qquad\qquad\times \frac{ 1 }{ 6.6 \times 10^5s^2 + 2 \times 10^6s + 1.1188 \times 10^8 }
\end{array}
$$

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
		A & = & -0.00004 \\
		B & = & 0.00235 \\
		C & = & 0.00004 \\
		D & = & 0.01370
	\end{array}
\right.
$$

$$
\implies
Y = 
\frac{ -0.00004s }{ s^2 + \frac{ 1 }{ 400\pi^2 } } +
0.14765 \times \frac{ \frac{ 1 }{ 20\pi } }{ s^2 + \frac{ 1 }{ 400\pi^2 } } + \frac{ 0.00004s + 0.0137 }{ s^2 + \frac{ 100 }{ 33 }s + \frac{ 5594 }{ 33 } }
$$

$$ = -0.00004\mathscr{ L }\left\{ \cos\frac{ t }{ 20\pi } \right\} + 0.14765 \mathscr{ L }\left\{ \sin\frac{ t }{ 20\pi } \right\} + \frac{ 0.00004s + 0.0137 }{ s^2 + \frac{ 100s }{ 33 } + \frac{ 5594 }{ 33 } }$$

$$
\begin{array}{}
= -0.00004\mathscr{ L }\left\{ \cos\frac{ t }{ 20\pi } \right\} + 0.14765 \mathscr{ L }\left\{ \sin\frac{ t }{ 20\pi } \right\} + \frac{ 0.00004 ( s + \frac{ 50 }{ 33 } ) }{ ( s + \frac{ 50 }{ 33 } )^2 + 167.21947 } \\
\qquad\qquad\qquad\qquad\qquad\qquad\qquad + 1.05476 \times 10^{ -3 } \times \frac{ 12.93133 }{ ( s + \frac{ 50 }{ 33 } )^2 + 167.21947 }
\end{array}
$$

$$
\begin{array}{}
= -0.00004 \mathscr{ L }\left\{ \cos\frac{ t }{ 20\pi } \right\} + 1.38921 \mathscr{ L }\left\{ \sin\frac{ t }{ 20\pi } \right\} \\ 
\qquad\qquad+ 0.00004\mathscr{ L }\left\{ e^{ -\frac{ 50 }{ 33 }t }\cos(167.21947t) \right\} \\
\qquad\qquad\qquad\qquad - 1.05476 \times 10^{ -5 }\mathscr{ L }\left\{ e^{ -\frac{ 50 }{ 33 }t }\sin(167.21947t) \right\}
\end{array}
$$

$$
\begin{array}{}
\implies y(t) = \underline{ -0.00004\cos\frac{ t }{ 20\pi } + 0.14765\sin\frac{ t }{ 20\pi } + 0.00004 e^{ -\frac{ 50 }{ 33 }t }\cos(12.9313t) } \\ 
\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\underline{ - 1.05476\times 10^{ -5 } e^{ -\frac{ 50 }{ 33 }t }\sin( 12.9313t ) }_{ \# }
\end{array}
$$

## 2

$$
\begin{array}{}
\text{ Laplace transform's result: }
\implies y(t) =  -0.00004\cos\frac{ t }{ 20\pi } + 0.14765\sin\frac{ t }{ 20\pi } \\ 
\qquad\qquad+ 0.00004 e^{ -\frac{ 50 }{ 33 }t }\cos(12.9313t)  
 - 1.05476\times 10^{ -5 } e^{ -\frac{ 50 }{ 33 }t }\sin( 12.9313t )
\end{array}
$$

$$
\begin{array}{l}
\text{ Undetermined coefficient: } \\
\implies y(t) = e^{ -1.515t }( 4.17 \times 10^{ -5 }\cos12.9501t + 1.043 \times 10^{ -3 }\sin 12.9501t ) \\
\qquad\qquad\qquad\qquad\qquad\qquad- 4.17 \times 10^{ -5 }\cos\frac{ t }{ 20\pi } + 1.47\times 10^{ -1 }\sin\frac{ 20\pi }{ t }
\end{array}
$$

$$\implies \text{ they are same }$$
## 3

$x$ axis: time
$y$ axis: position

![[earth quake graph math project 3.png]]

## 4

$$\text{ transfer function } = \frac{ 1.65 \times 10^7 }{ 
6.6 \times 10^5s^2 + 2 \times 10^6s + 1.1188 \times 10^8 }$$

Transfer function makes the relation between input and output clear.

# Section 4: Impulse Forcing

## 4.2

$$\text{ In 2nd Newton law: } \Delta P = m \int_1^2 f(t)dt$$

$$
f(t) = 
\left\{
	\begin{array}{}
		F & 1\leq t\leq 1 + \Delta t \\
		0 & \text{ otherwise }
	\end{array}
\right. , \qquad F = \frac{ P }{ \Delta t }
$$

$$\implies f(t) = \frac{ P }{ \Delta t }( u(t - 1) - u( t - ( 1 + \Delta t ) ) )$$

$$
\implies \text{ function: } m\frac{ d^2y }{ dt^2 } = -ky - c\frac{ dy }{ dt } + \frac{ P }{ \Delta t }[ u(t - 1) 
- u(t - (1 + \Delta t)) ]
$$

## 4.3

$$\text{ Amplitude } = \frac{ P }{ \Delta t } = \sin(2\pi ft) = \sin(\frac{ t }{ 20\pi })$$

$$\implies m\frac{ d^2y }{ dt^2 } = -ky-c\frac{ dy }{ dt } + \sin(\frac{ t }{ 20\pi })[u(t - 1) - u(t - (1 + \Delta t))]$$

## 4.4

## 4.5

$$my'' + cy' + ky = \sin(\frac{ t }{ 20\pi })[u(t - 1) - u(u - 2)], \quad y(0) = 0,\quad y'(0) = \frac{ 1 }{ 20\pi }$$

$$
\begin{array}{}
\implies m\left(s^2Y - sy(0) - y'(0)\right) + c(sY - y(0)) + kY = e^{ -1s }\mathscr{ L }\left\{ \sin\frac{ t + 1 }{ 20\pi } \right\} \\ 
\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad - e^{ -2s }\mathscr{ L }\left\{ \sin\frac{ t + 2 }{ 20\pi } \right\}
\end{array}
$$

$$\implies (ms^2 + cs + k)Y = \frac{ m }{ 20\pi } + e^{ 
-s }\frac{ \frac{ 1 }{ 20\pi } }{ (s + 1)^2 + (\frac{ 1 }{ 20\pi })^2 }$$

$$
\begin{array}{}
\implies Y = \frac{ m }{ 20\pi }\cdot \frac{ 1 }{ ms^2 + cs + k } + \frac{ e^{ -s } }{ 20\pi } \cdot \frac{ 1 }{ (s + 1)^2 + (\frac{ 1 }{ 20\pi })^2 }\cdot \frac{ 1 }{ ms^2 + cs + k } \\ 
- \frac{ e^{ -2s } }{ 20\pi } \cdot \frac{ 1 }{ (s + 2)^2 + (\frac{ 1 }{ 20\pi })^2 }\cdot\frac{ 1 }{ ms^2 + cs + k }
\end{array}
$$

$$\implies Y = \frac{ 1 }{ 20\pi }\cdot \frac{ 1 }{ (s^2 + \frac{ c }{ m }s + \frac{ c^2 }{ 2m^2 }) + \frac{ k }{ m } - \frac{ c^2 }{ 4m^2 } }$$