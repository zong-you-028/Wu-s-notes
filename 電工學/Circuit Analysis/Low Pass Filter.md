標籤: #電工學 

---

# RC Filter

![[RC filter.png]]

$$G(\omega) = \frac{ v_o(\omega) }{ v_i(\omega) } \underbrace{ = }_{ \text{ voltage divider } } \frac{ \frac{ 1 }{ j\omega C } }{ R + \frac{ 1 }{ j\omega C } } = \frac{ 1 }{ jRC\omega + 1 }$$

$$ = \underbrace{ \frac{ 1 }{ \sqrt{ 1 + (\omega T)^2 } } }_{ \text{ gain } } \underbrace{ \angle -\tan^{ -1 }\omega T }_{ \text{ phase } } \qquad T = RC$$

![[rc filter diagram.png]]

# LR Filter

![[lr filter schematic diagram.png]]

$$G(\omega) = \frac{ v_o(\omega) }{ v_i(\omega) } = \frac{ 1 }{ 1 + j\omega T } \qquad T = \frac{ L }{ R }$$

# [[RLC Circuit#Operational Amplifier Filter|Operational Amplifier Filter]]

![[op amp filter.png]]

Op amp filter 是一種 "Active Filter" ，也就是輸出的電流源和輸入的電流源不同，因此可以串接

$$Z_1 = R$$

$$Z_f = R \vert\vert \frac 1 { j\omega C }$$

$$\implies \frac{ v_o }{ v_i } = 
\frac{ 
	-\frac{ 
		R \cdot \frac{ 1 }{ j\omega C } 
	}
	{
		R + \frac{
			1
		}
		{
			j\omega C
		}
	}
}
{ R } = 
\frac { -1 }{ 1 + j\omega RC }$$

---

參考資料:

電工學上課

---

link:

[[Amplifier]]