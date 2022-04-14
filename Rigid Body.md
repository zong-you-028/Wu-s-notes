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

## General plane motion

---

參考資料:

動力學上課

---

link:

