標籤: #arduino 

---

相比[[servo.write(angle)]]更精確。

一般合乎規定的伺服馬達在1000是0度，在1500是90度，在2000是180度，但是有許多伺服馬達並不按照這個標準，通常最大值和最小值會在700和2300之間。

[[Continuous Rotation Servo]]也可以用這個函式控制。

---

# 語法

```arduino
servo.writeMicroseconds(us)
```

`servo`: 一個`Servo`定義的物件
`us`: 一個整數，單位是毫秒

---

# 範例

```arduino
#include <Servo.h> 

Servo myservo;

void setup() 
{ 
  myservo.attach(9);
  myservo.writeMicroseconds(1500);  // set servo to mid-point
} 

void loop() {} 
```

---

> 參考資料: [Servo - writeMicroseconds()](https://www.arduino.cc/reference/en/libraries/servo/writemicroseconds/)