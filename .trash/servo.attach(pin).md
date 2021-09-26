標籤: #arduino 

---

# 語法

```arduino
servo.attach(pin) 
servo.attach(pin, min, max)
```

`servo`: 一個`Servo`定義的物件
`pin`: 針腳的數字
`min`: [[脈衝訊號寬度]]最小值(ms)，0度，預設為544
`max`: [[脈衝訊號寬度]]最大值(ms)，180度，預設為2400

---

# 範例

```arduino
#include <Servo.h> 

Servo myservo;

void setup() 
{ 
  myservo.attach(9);
} 

void loop() {} 
```

---

> 參考資料: [Arduino Servo - attach()](https://www.arduino.cc/reference/en/libraries/servo/attach/)