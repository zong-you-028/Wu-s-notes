# STM32 命名方法

STM32F429ZI

Z 表示腳位數量

| 代碼 | Pin數量 |
| ---- | ------- |
| C    | 48      |
| R    | 64      |
| V    | 100     |
| Z    | 144     |
| I    | 176     |
| B    | 208     |
| N    | 216     | 

I 指快閃記憶體大小

| 代碼 | Code Size(KB) | 代碼 | Code Size(KB) |
| ---- | ------------- | ---- | ------------- |
| 0    | 1             | A    | 92            |
| 1    | 2             | B    | 128           |
| 2    | 4             | Z    | 192           |
| 3    | 8             | C    | 256           |
| 4    | 16            | D    | 384           |
| 5    | 24            | E    | 512           |
| 6    | 32            | F    | 768           |
| 7    | 48            | G    | 1024          |
| 8    | 64            | H    | 1536          |
| 9    | 72            | I    | 2048          | 

# IDE main.c

最前面有一些註解是使用者可以自行定義的地方。

```c
/* Includes ------------------------------------------------------------------*/
#include "main.h"

/* Private includes ----------------------------------------------------------*/
/* USER CODE BEGIN Includes */

/* USER CODE END Includes */

/* Private typedef -----------------------------------------------------------*/
/* USER CODE BEGIN PTD */

/* USER CODE END PTD */

/* Private define ------------------------------------------------------------*/
/* USER CODE BEGIN PD */
/* USER CODE END PD */
```

例如這裡，可以把定義寫在 `USER CODE BEGIN` 和 `USER CODE END` 之間，如果放在這之外的地方的話 IDE 會清除這些程式碼(因為這個 IDE 會自己產生程式碼在 `USER CODE BEGIN` 和 `USER CODE END` 以外的地方)。