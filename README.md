# -TM1637
Код очень простой :
```cpp
int HOURS;
int min;
#include <microDS3231.h>
#include "GyverTM1637.h"
GyverTM1637 disp(2, 3);
MicroDS3231 rtc;
void setup() {
  disp.clear();        // очистить
  disp.brightness(7);  // яркость 0-7
  rtc.setTime(COMPILE_TIME);
  disp.point(1);
}

void loop() { 
  HOURS = rtc.getHours();
  min = rtc.getMinutes();
  disp.displayClock(der, min);  // вывести часы и минуты
}
```
