標籤: #動力學 

---

# Planar Rigid-Body Motion

包含了三種情況

1. [[#Translation]]: 平移
2. [[#Rotation about a fixed axis]]: 旋轉
3. [[#General plane motion]]: 邊旋轉邊平移

最重要的是 3. ，因為它最泛用

## Translation

假設 $A, B$ 點為一個 rigid body 上的兩個參考點

### Position

$$r_B = r_A + r_{ B / A }$$

### Velocity

$$v_B = v_A + \frac{ d r_{ B / A } }
{ dt }$$

$$\because dr_{ B / A } / dt = 0 \quad (A, B\text{ 點間沒有相對運動，因為是 translation})$$

$$\therefore \underline{
v_B = v_A }_{ \# }$$

### [[Acceleration]]

$$a_B = a_A$$

## Rotation about a fixed axis

### Angular [[Acceleration]]

$$\alpha d\theta = \omega d\omega$$

> 跟 [[Acceleration]] 相似:
> $$ads = vdv$$

### Velocity

$$\vec v = \omega \times \vec r_p$$

$\vec v$: rigid body 上一個點 $P$ 的速度
$\vec r_p$: rigid body 上一個點 $P$ 的位置

### [[Acceleration]]

$$a_t = \alpha r$$

$$a_n = \omega^2 r$$

$\alpha$: 角加速度

對於 rigid body 其中一點 $P$ ，角加速度可以用 [[Cross Product]] 表示

$$\vec a = \alpha \times \vec r_p + \omega \times (\omega \times \vec r_p)$$

$$\vec a = \vec a_t + \vec a_n = 
\alpha \times \vec r - \omega^2 \vec r$$

## General plane motion (Relative-Motion Analysis)

需要使用 Relative-Motion Analysis 分析

### Position

$$\vec r_B = \vec r_A + \vec r_{ B / A }$$

### Displacement

$A$ and $B$ undergo displacements $dr_A$ and $dr_B$

$$\implies d\vec r_B = 
d\vec r_A + d\vec r_{ B / A }$$

### Velocity

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

### [[Acceleration]]

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

# Instantaneous Centor of Zero Velocity

![[Instantaneous Center]]

# Translating Coordinate System

Use for analyzing motions of two points on a mechanism which are not located in the same body

> example of translating coordinate system
> ![[example of translating coordinate system.png|400]]
> 譬如以上的例子，我們希望分析 $C$ 點與 $O$ 點之間的相對運動，而他們在不同的 body 上。這時我們就可以使用 translating coordinate system ，架設一個會隨著 body 轉動的 coordinate (圖中 $x, y$)。

在以下的結果中，你會發現有點類似[[#General plane motion Relative-Motion Analysis|一般 rigid body]] 的算法，但是在這裡的情況不同，座標軸是會旋轉的。因此底下結果的推導多考慮了座標軸的旋轉（類似[[極座標]]的推導），因此結果也不同。

注意以下的向量皆是使用 $x, y$ 座標軸，而不是 $X, Y$ 座標軸。

## Position 

$$ { \bf r }_B = 
{ \bf r }_A + { \bf r }_{ B / A }$$

## Velocity

$${ \bf v }_B = 
{ \bf v }_A + 
{ \bf \Omega } \times { \bf r }_{ B / A } + 
({ \bf v }_{ B / A })_{ xyz }$$

## [[Acceleration]]

$${ \bf a }_B = 
{ \bf a }_A + 
{ \bf \Omega } \times 
{ \bf r }_{ B / A } + 
{\bf\Omega} \times 
({\bf \Omega } \times 
{ \bf r }_{ B / A }) +
2{ \bf \Omega } \times 
({ \bf v }_{ B / A })_{ xyz } + 
({ \bf a }_{ B / A })_{ xyz }$$

# Force and [[Acceleration]] of Rigid Body

## Mass [[Moment]] of Inertia

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

### Common Mass [[Moment]] of Inertia

[List of moment of inertia - wiki](https://en.wikipedia.org/wiki/List_of_moments_of_inertia)

| Figure                           | [[Moment]] of Inertia           |
| -------------------------------- | --------------------------- |
| ![[rod moment of inertia.png]]   | $$I = \frac 1 { 12 } mL^2$$ |
| ![[plate moment of inertia.png]] | $$I_z = \frac 1 2 mr^2$$ $$I_x = I_y = \frac 1 4 mr^2$$                           |

### Parallel-Axis Theorem

![[parallel axis theorem.png|300]]

$$I_2 = I_1 + md^2$$

$m$: 總質量
$I_1$: 相對軸 1 的 inertia
$I_2$: 相對軸 2 的 inertia
$d$: 軸 1 和軸 2 的距離

### Radius of Gyration

The [[moment]] of inertia of a body about a specified axis can be expressed using the radius of gyration, $k$

$$I = mk^2$$

$$\text{ or }$$

$$k = \sqrt{ \frac{ I }{ m } }$$

## Planar Kinetic Equations of Motion

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
		\sum M_P & = & -\bar ym(a_G)_x & 
		+ & \bar xm(a_G)_y & + I_G \alpha
	\end{array}
\right.
$$

---

參考資料:

動力學上課

---

link:

