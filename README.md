# arduino-blink-possible-defects

```c
01. // the setup function runs once when you press reset or power the board
02. void setup() {
03.   // initialize digital pin 13 as an output.
04.   pinMode(13, OUTPUT);
05. }
06.
07. // the loop function runs over and over again forever
08. void loop() {
09.   digitalWrite(13, HIGH);   // turn the LED on (HIGH is the voltage level)
10.   delay(1000);              // wait for a second
11.   digitalWrite(13, LOW);    // turn the LED off by making the voltage LOW
12.   delay(1000);              // wait for a second
13. }
```

- рядок 1. можна забути додати коментар `//`. В мові С++ немає інструкціі `the setup function runs once when you press reset or power the board`. Помилка
- рядок 4. ми пишемо аутпут 13, а світлодіод вставляєм в аутпут 12. Помилка
- рядок 5. забули додати фігурну дужку. функція сетап не закінчиться. Помилка
- рядок 10. `delay(1)` лампочка буде запалюватись на 1мс, це не буде видно оку. Помилка.

Загальне зауваження до цього коду. ми маємо в 3 місцях цифру 13. це магічне число якого варто уникати. як? створити окрему змінну, назвати її `OUTPUT_PIN_NUMBER` і використати її тричі.
