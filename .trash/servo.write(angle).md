標籤: #arduino 

---

# 語法

```arduino
servo.write(angle)
```

`servo`: `Servo`型態的物件
`angle`: 一個0 到180 的數字。在一般伺服馬達上，這代表馬達轉向的角度。在[[Continuous Rotation Servo]]，這會是馬達的轉速，0反轉、180正轉、90停止。

---

# 範例

```arduino
#include <Servo.h> 

Servo myservo;

void setup() 
{ 
  myservo.attach(9);
  myservo.write(90);  // set servo to mid-point
} 

void loop() {} 
```

---

> 參考資料: [Servo - write()](https://www.arduino.cc/reference/en/libraries/servo/write/)