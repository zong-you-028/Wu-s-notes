標籤: #電工學 

---

用來分析電路

- 有 $N - 1$ 個 current law
- 有 $L$ 個 voltage law

# Node(Voltage Node)

A connected wire or plate shared the same voltage

# Arc

A one port element which has two terminals

# 用文字表示電路

![[Kirchhoff's Law Example.png]]

| Arc | Node 1 | Node 2 | Value |
| --- | ------ | ------ | ----- |
| V   | 1      | 0      | 48    |
| R   | 1      | 2      | 9     |
| I   | 2      | 0      | 7     |
| R   | 2      | 0      | 5     |
| R   | 0      | 3      | $R_L$ |
| R   | 2      | 3      | 2     | 

- Node 1 與 Node 2 代表電流的方向
- 在 power source 的情況下，電流從 Node 2 流向 Node 1
- 在 element 的情況下，電流從 Node 1 流向 Node 2

# Euler Formula

$$L + N - 1 = A$$

$L$: loops (只計最小的 node)
$N$: node 的數量
$A$: arc 的數量

# Kirchhoff Law

- Kirchhoff Current Law: The total current entering a "node" is zero
- Kirchhoff Voltage Law: The sum of all voltages on the individual "elements" on a "loop" is zero

## Open Circuit

![[Open Circuit.png]]

$$R_L = \underbrace{ \infty }_{ \text{ Light Load 輕載 } } \text{ : open circuit }$$

$$\implies i_L = 0$$

$$v_L = v_{ oc }$$

$v_{ oc }$ is called open circuit voltage

---

$$R_L = \underbrace{ 0 }_{ \text{ Heavy Load 重載 } } \text{ : short circuit }$$

$i_L$ to be solved, known to the short circuit current

---

參考資料:

電工學上課 2022-02-17

---

link:

[[Cramer's Rule]]