標籤: #動力學 

---

# 2D Motion

## Planar Motion

包含了三種情況

1. [[#Translation]]: 平移
2. [[#Rotation about a fixed axis]]: 旋轉
3. [[#General plane motion Relative-Motion Analysis|General plane motion]]: 邊旋轉邊平移

最重要的是 3. ，因為它最泛用

### Translation

假設 $A, B$ 點為一個 rigid body 上的兩個參考點

#### Position

$$r_B = r_A + r_{ B / A }$$

#### Velocity

$$v_B = v_A + \frac{ d r_{ B / A } }
{ dt }$$

$$\because dr_{ B / A } / dt = 0 \quad (A, B\text{ 點間沒有相對運動，因為是 translation})$$

$$\therefore \underline{
v_B = v_A }_{ \# }$$

#### [[Acceleration]]

$$a_B = a_A$$

### Rotation about a fixed axis

#### Angular [[Acceleration]]

$$\alpha d\theta = \omega d\omega$$

> 跟 [[Acceleration]] 相似:
> $$ads = vdv$$

#### Velocity

$$\vec v = \omega \times \vec r_p$$

$\vec v$: rigid body 上一個點 $P$ 的速度
$\vec r_p$: rigid body 上一個點 $P$ 的位置

#### [[Acceleration]]

$$a_t = \alpha r$$

$$a_n = \omega^2 r$$

$\alpha$: 角加速度

對於 rigid body 其中一點 $P$ ，角加速度可以用 [[Cross Product]] 表示

$$\vec a = \alpha \times \vec r_p + \omega \times (\omega \times \vec r_p)$$

$$\vec a = \vec a_t + \vec a_n = 
\alpha \times \vec r - \omega^2 \vec r$$

### General plane motion (Relative-Motion Analysis)

需要使用 Relative-Motion Analysis 分析

#### Position

$$\underline{ 
	\vec r_B = \vec r_A + \vec r_{ B / A }
}_\#$$

#### Displacement

$A$ and $B$ undergo displacements $dr_A$ and $dr_B$

$$\implies d\vec r_B = 
d\vec r_A + d\vec r_{ B / A }$$

#### Velocity

$$\frac{ d\vec r_B }{ dt } = 
\frac{ d\vec r_A }{ dt } + 
\frac{ d\vec r_{ B / A } }{ dt }$$

$$\implies \underline{ 
\vec v_B = 
\vec v_A + \vec v_{ B / A } }_{ \# }$$

$\because \vec v_{ B / A }$ 是相對運動，因此可以用 [[Cross Product]] 表示

$$\implies \underline{ \vec v_B = 
\vec v_A + 
\omega \times \vec r_{ B / A } }_{ \# }$$

#### [[Acceleration]]

在上面我們知道 velocity 的關係

$${ \bf v }_B = 
{ \bf v }_A + { \bf v }_{ B / A }$$

$$\implies 
\frac{ d{ \bf v }_B }{ dt } = 
\frac{ d{ \bf v }_A }{ dt } + 
\frac{ d{ \bf v }_{ B / A } }{ dt }$$

$$\implies \underline{ { \bf a }_B = 
{ \bf a }_A + 
( { \bf a }_{ B / A } )_t + 
( { \bf a }_{ B / A } )_n }_{ \# }$$

這個結果可以用圖片來看

![[rigid body acceleration.png]]

並且上式也可以用角加速度與角速度表示

$$\implies 
\underline{ { \bf a }_B = 
{ \bf a }_A + 
\alpha \times { \bf r }_{ B / A } +
\omega \times (
	\omega \times  { \bf r }_{ B / A } 
) }_{ \# }$$

$$\implies 
\underline{ { \bf a }_B = 
{ \bf a }_A + 
\alpha \times { \bf r }_{ B / A } - 
\omega^2 { \bf r }_{ B / A } }_{ \# }$$

$\alpha$: 角加速度

## Instantaneous Centor of Zero Velocity

![[Instantaneous Center]]

## Translating Coordinate System

Use for analyzing motions of two points on a mechanism which are not located in the same body

> example of translating coordinate system
> ![[example of translating coordinate system.png|400]]
> 譬如以上的例子，我們希望分析 $C$ 點與 $O$ 點之間的相對運動，而他們在不同的 body 上。這時我們就可以使用 translating coordinate system ，架設一個會隨著 body 轉動的 coordinate (圖中 $x, y$)。

在以下的結果中，你會發現有點類似[[#General plane motion Relative-Motion Analysis|一般 rigid body]] 的算法，但是在這裡的情況不同，座標軸是會旋轉的。因此底下結果的推導多考慮了座標軸的旋轉（類似[[極座標]]的推導），因此結果也不同。

注意以下的向量皆是使用 $x, y$ 座標軸，而不是 $X, Y$ 座標軸。

### Position 

$$ { \bf r }_B = 
{ \bf r }_A + { \bf r }_{ B / A }$$

### Velocity

$${ \bf v }_B = 
{ \bf v }_A + 
{ \bf \Omega } \times { \bf r }_{ B / A } + 
({ \bf v }_{ B / A })_{ xyz }$$

### [[Acceleration]]

$${ \bf a }_B = 
{ \bf a }_A + 
\dot{ \bf \Omega } \times 
{ \bf r }_{ B / A } + 
{\bf\Omega} \times 
({\bf \Omega } \times 
{ \bf r }_{ B / A }) +
2{ \bf \Omega } \times 
({ \bf v }_{ B / A })_{ xyz } + 
({ \bf a }_{ B / A })_{ xyz }$$

## Force and [[Acceleration]]

### Mass [[Moment]] of Inertia

根據牛頓定律

$${ \bf F } = m { \bf a }$$

而 [[moment]] 等於

$${ \bf M } = I { \bf \alpha }$$

其中 $I$ 是 mass [[moment]] of inertia，$\alpha$ 是角速度

mass [[moment]] of inertia 的計算相似於 [[Area Moment of Inertia]] ，如下

$$I = \int_m r^2 dm$$

using volume elements $V$

$$I = \int_V r^2 \rho dV$$

$\rho$: 密度

#### Common Mass [[Moment]] of Inertia

[List of moment of inertia - wiki](https://en.wikipedia.org/wiki/List_of_moments_of_inertia)

| Figure                                       | [[Moment]] of Inertia                                   |
| -------------------------------------------- | ------------------------------------------------------- |
| ![[rod moment of inertia.png]]               | $$I = \frac 1 { 12 } mL^2$$                             |
| ![[plate moment of inertia.png]]             | $$I_z = \frac 1 2 mr^2$$ $$I_x = I_y = \frac 1 4 mr^2$$ |
| ![[solid sphere of radius r and mass m.png]] | $$I = \frac 2 5 mr^2$$                                  | 

#### Parallel-Axis Theorem

![[parallel axis theorem.png|300]]

$$I_2 = I_1 + md^2$$

$m$: 總質量
$I_1$: 相對軸 1 的 inertia
$I_2$: 相對軸 2 的 inertia
$d$: 軸 1 和軸 2 的距離

#### Radius of Gyration

The [[moment]] of inertia of a body about a specified axis can be expressed using the radius of gyration, $k$

$$I = mk^2$$

$$\text{ or }$$

$$k = \sqrt{ \frac{ I }{ m } }$$

### Planar Kinetic Equations of Motion

$$\sum { \bf F } = m { \bf a }_G$$

$$\sum { \bf M }_P = -\bar y m(a_G)_x + 
\bar x m(a_G)_y + I_G \alpha$$

![[planar kinetic equations of motion.png|350]]

$$
\implies
\left\{
	\begin{array}{}
		\sum F_x & = & m(a_G)_x \\
		\sum F_y & = & m(a_G)_y \\
		\sum M_G & = & I_G \alpha \\
		& \text{ or } \\
		\sum M_P & = & -\bar ym(a_G)_x & 
		+ & \bar xm(a_G)_y & + I_G \alpha
	\end{array}
\right.
$$

#### Rotation about a Fixed Axis

![[force and acceleration rotation around a fixed axis.png|350]]

$$\left\{
	\begin{array}{}
		\sum F_n & = & m(a_G)_n & = & m\omega^2 r_G \\
		\sum F_t & = & m(a_G)_t & = & m \alpha r_G \\
		\sum M_G & = & I_G \alpha
	\end{array}
\right.$$

也可以對 $O$ 點取 [[Moment]]

$$\left\{
	\begin{array}{}
		\sum F_n & = & m(a_G)_n & = & m\omega^2 r_G \\
		\sum F_t & = & m(a_G)_t & = & m \alpha r_G \\
		\sum M_O & = & I_O \alpha
	\end{array}
\right.$$

#### [[Moment]] Equation about the Instantaneous Centor

也可以對 Instantaneous Centor 取 [[Moment]]

$$\underline{ \sum M_{ IC } = I_{ IC } \alpha }_{ \# }$$

## [[Work]] and Energy

### Kinetic Energy

![[kinetic energy of rigid body.png|350]]

The kinetic energy of the entire body is 

$$T = \frac 1 2 \int_m dm v_i^2$$

if the body has an angular velocity $\omega$

$${\bf v}_i = {\bf v}_p + {\bf v}_{ i / p }$$

$$ = (v_p)_x \hat i + 
(v_p)_y \hat j + 
\omega \hat k \times (x\hat i + y\hat j)$$

$$ = [(v_p)_x - \omega y]\hat i + 
[(v_p)_y + \omega x]\hat j$$

$$\implies {\bf v}_i \cdot {\bf v}_i = v_i^2$$

$$ = [(v_p)_x - \omega y]^2 + [(v_p)_y + \omega x]^2$$

$$ = (v_p)_x^2 - 2(v_p)_x\omega y + \omega^2y^2 + (v_p)_y^2 + 2(v_p)_y\omega x + \omega^2x^2$$

$$ = v_p^2 - 2(v_p)_x \omega y + 2(v_p)_y\omega x + \omega^2 r^2$$

$$\implies T = \frac 1 2(\int_m dm)v_p^2 - (v_p)_x\omega(\int_mydm) + (v_p)_x\omega(\int_mxdm) + \frac 1 2 \omega^2(\int_m r^2dm)$$

> Since 
> $$\bar ym = \int ydm$$
> $$\bar xm = \int xdm$$
> they represent the location of the body's center of mass $G$ with respect to $P$
> 
> $$\int_m r^2dm = I_p$$

As a special case, if $P$ coincides with $G$, $\bar y = \bar x = 0$

$$\implies \underline{ T = \frac 1 2 mv_G^2 + \frac 1 2 I_G \omega^2 }_\#$$

#### Rotation about a Fixed Axis

![[kinetic energy rotation about a fixed axis.png|250]]

$$T = \frac 1 2 m v_G^2 + \frac 1 2 I_G \omega^2$$

$$ = \frac 1 2 m r_G^2 \omega^2 + \frac 1 2 I_G \omega^2$$

$$ = \frac 1 2(I_G + mr_G^2)\omega^2$$

$$ = \underline{ \frac 1 2 I_o \omega^2 }_\#$$

#### General Plane Motion

$$T = \frac 1 2 m v_G^2 + \frac 1 2 I_G \omega^2$$

$$ = \underline{ \frac 1 2 I_{ IC } \omega^2 }_\#$$

similar to rotation about a fixed axis

### The [[Work]] of a Force

#### [[Work]] of a Variable Force

$$\underline{ U_F = \int{ \bf F } \cdot d{\bf r} = \int_s F\cos \theta ds }_\#$$

#### The [[Work]] of a Couple [[Moment]]

$$\underline{ U_M = \int_{ \theta_1 }^{ \theta_2 } Md\theta }_\#$$

if ${\bf M}$ has constant magnitude

$$\underline{ U_M = M(\theta_2 - \theta_1) }_\#$$

#### Principle of [[Work]] and Energy

$$\underline{ T_1 + \sum U_{ 1 - 2 } = T_2 }_\#$$

## Linear and Angular Momentum

### Linear Momentum

$${\bf L} = m {\bf v}_G$$

### Angular Momentum

angular momentum of $i$th particle is

$$({\bf M}_P)_i = {\bf r} \times m_i{\bf v}_i$$

using cartesian vectors

$$\implies (H_P)_i \hat k = m_i(x \hat i + y\hat j) \times [(v_P)_x \hat i + (v_P)_y \hat j + \omega \hat k \times(x \hat i + y \hat j)]$$

$$\implies (H_P)_i = -m_iy(v_P)_x + m_i x (v_P)_y + m_i \omega r^2$$

$$\implies H_P = -\left(\int_m ydm\right)(v_P)_x + \left(\int_m xdm\right)(v_P)_y + \left( \int_m r^2dm \right)\omega$$

$$\implies H_P = -\bar y m (v_P)_x + \bar x m(v_P)_y + I_P \omega$$

$$\implies \underline{ H_G = I_G \omega }_\#$$

### Momentum of Motions

#### Translation

$$
\underline{
	\begin{array}{}
		L & = & mv_G \\
		H_G & = & 0
	\end{array}
}_\#
$$

#### Rotation About a Fixed Axis

$$
\underline{
	\begin{array}{}
		L & = & mv_G \\
		H_G & = & I_G \omega
	\end{array}
}_\#
$$

$$\implies \underline{ H_O = I_O \omega }_\#$$

#### General Plane Motion

$$
\underline{
	\begin{array}{}
		L & = & mv_G \\
		H_G & = & I_G \omega
	\end{array}
}_\#
$$

$$\implies \underline{ H_{IC} = I_{ IC }\omega }_\#$$

### Principle of Impulse and Momentum

if motion occurs in the $x-y$ plane:

$$
\underline{
	\left\{
		\begin{array}{}
			m(v_{ Gx })_1 & + & \sum\int_{ t_1 }^{ t_2 } F_xdt & = & m(v_{ Gx })_2 \\
			m(v_{ Gy })_1 & + & \sum \int_{ t_1 }^{ t_2 }F_y dt & = & m(v_{ Gy })_2 \\
			I_G\omega_1 & + & \sum\int_{ t_1 }^{ t_2 }M_G dt & = & I_G \omega_2 
		\end{array}
	\right.
}_\#
$$

# 3D Motion

## Rotation About a Fixed Point

> ### Euler's Theorem
> two "component" rotations about different axis passing through a point are equivalent to a single resultant rotation about an axis passing through the point
> 
> $\implies$ If more than two rotations are applied, they can be combined into pairs, and each pair can be further reduced to combine into one rotation

#### Finite Rotations

If component rotations used in Euler's theorem are finite, it is important that the order in which they are applied be maintained.

![[why finite rotations order matters.png]]

如上圖，如果先轉 $\theta_2$ 再轉 $\theta_1$ 結果會完全不同

#### Infinitesimal Rotations

與 Finite Rotations 相反

When defining the 3D angular motions, only rotations which are infinitesimally small will be considered and they can be classified as vector, so they can be added easilly.

### Velocity for Rotation

$$\vec v = \vec \omega \times \vec r$$

### Acceleration for Rotation

$$\vec a = \vec \alpha \times \vec r + \vec \omega \times ( \vec \omega \times \vec r )$$

## The Time Derivative of a Vector

> 這個常用在計算 angular velocity $\Omega$ 和 angular acceleration $\dot\Omega$
> $$\Omega = \sum \omega_i$$
> $$\dot\Omega = \sum \dot\omega_i$$
> 其中一個 $\dot \omega_i$ 我們會用 time derivative of a vector 的公式求出
> $$\dot\omega = (\dot\omega)_{xyz} + \underbrace{\Omega}_{\text{ 前面的角速度加總 }} \times \omega$$

當在空間中架設一個會隨時間轉動的座標軸 $xyz$ ，並且有一個以此座標軸表示的向量 $\vec A$ ， $\dot { \vec A }$ 會使用接下來的公式算

![[time derivative of a vector.png|300]]

$$\vec A = A_x \hat i + A_y \hat j + A_z \hat k$$

因為 $\hat i, \hat j, \hat k$ 相對於 $xyz$ 座標軸沒有轉動

$$\implies (\dot {\vec A})_{ xyz } = 
\dot A_x \hat i + 
\dot A_y \hat j + 
\dot A_z \hat k$$

但 $\hat i, \hat j, \hat k$ 對 $XYZ$ 有轉動，因此

$$\implies \dot { \vec A } = \dot A_x \hat i +
\dot A_y \hat j +
\dot A_z \hat k +
A_x \dot {\hat i} +
A_y \dot {\hat j} +
A_z \dot {\hat k}
$$

並且 $\dot{ \hat i }, \dot{ \hat j }, \dot{ \hat k }$ 可以用 $\vec \Omega$ 與外積算出

$$
\left\{
	\begin{array}{}
		\dot {\hat i} = \vec \Omega \times \hat i \\
		\dot {\hat j} = \vec \Omega \times \hat j \\
		\dot {\hat k} = \vec \Omega \times \hat k 
	\end{array}
\right.
$$

$$\implies \underline{\dot{ \vec A } = (\dot {\vec A})_{xyz} + \vec \Omega \times \vec A}_\#$$

### Example

`TODO: 20.1`

## Rigid Body General Motion

![[general motion.png]]

The general motion is defined by

$$\vec v_{ B / A } = \omega \times \vec r_{B / A}$$

$$\vec a_{ B / A } = \alpha \times \vec r_{B / A} + \omega \times (\omega \times \vec r_{B / A})$$

The absolute velocity and acceleration of point $B$ can be determined from

$$\underline{ \vec v_B = \vec v_A + \omega \times \vec r_{B / A} }_\#$$

$$\underline{\vec a_B = \vec a_A + \alpha \times \vec r_{B / A} + \omega \times (\omega \times \vec r_{B / A})}_\#$$

## Relative-Motion Analysis Using Translating and Rotating Axes

![[relative motion analysis using translating and rotating axes.png]]

### Position

If the position of "$B$ with respect to $A$" is specified by the relative-position vector $\vec r_{B / A}$, then

$$\underline{
	\vec r_B = \vec r_A + \vec r_{B / A}
}_\#$$

### Velocity

The velocity of point $B$ measured from $X, Y, Z$ is

$$\dot {\vec r}_B = \dot {\vec r}_A + \dot{\vec r}_{B / A}$$

$$\dot {\vec r}_{B / A} = (\dot{\vec r}_{B / A})_{xyz} + \Omega \times \vec r_{B / A}$$

$$ = (\vec v_{B / A})_{xyz} + \Omega \times \vec r_{B / A}$$

Here $(\vec v_{B / A})_{xyz}$ is the relative velocity of $B$ with respect to $A$ measured from $x, y, z$. Thus,

$$\underline{\underbrace{\vec v_B = \vec v_A + \Omega \times \vec r_{B / A}}_{\text{ for rigid body }} + \underbrace{(\vec v_{B / A})_{xyz}}_{\text{ not rigid body }}}_\#$$

### Acceleration

The acceleration of point $B$ measured from $X, Y, Z$ is

$$\dot{ \vec v }_B = \dot{\vec v}_A + \dot \Omega \times \vec r_{B / A} + \Omega \times \dot{\vec r}_{B / A} + \frac{d}{dt}(\vec v_{B / A})_{xyz}$$

where

$$\frac{d}{dt}(\vec v_{B / A})_{xyz} = (\dot{\vec v}_{B / A})_{xyz} + \Omega \times (\vec v_{B / A})_{xyz} $$
$$= (\vec a_{B / A})_{xyz} + \Omega \times (\vec v_{B / A})_{xyz}$$

$(\vec a_{B / A})_{xyz}$ is the relative acceleration of $B$ with respect to $A$ measured from $x, y, z$, thus

$$\underline{\vec a_B = \vec a_A + \dot \Omega \times \vec r_{B / A} + \Omega \times (\Omega \times \vec r_{B / A}) + 2\Omega \times (\vec v_{B / A})_{xyz} + (\vec a_{B / A})_{xyz}}_\#$$

---

參考資料:

動力學上課

---

link:
