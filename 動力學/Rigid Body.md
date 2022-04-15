標籤: #動力學 

---

# Planar Rigid-Body Motion

包含了三種情況

1. [[#Translation]]: 平移
2. [[#Rotation about a fixed axis]]: 旋轉
3. [[#General plane motion]]: 邊旋轉邊平移

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

### Acceleration

$$a_B = a_A$$

## Rotation about a fixed axis

### Angular Acceleration

$$\alpha d\theta = \omega d\omega$$

> 跟 [[Acceleration]] 相似:
> $$ads = vdv$$

### Velocity

$$\vec v = \omega \times \vec r_p$$

$\vec v$: rigid body 上一個點 $P$ 的速度
$\vec r_p$: rigid body 上一個點 $P$ 的位置

### Acceleration

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

# Instantaneous Center of Zero Velocity

Instantaneous: 瞬心，在瞬心的速度為 $0$

瞬心的位置有幾種情況

![[different positions of instantaneous center a and b.jpg]]

![[different positions of instantaneous center c and d.jpg]]



---

參考資料:

動力學上課

---

link:

