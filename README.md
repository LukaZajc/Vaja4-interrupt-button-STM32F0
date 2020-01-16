Vaja 4 CubeMX

2.

b) Glede na vašo razvojno ploščo in razširitveno vezje s tipkami, iozberite ustrezen digitalni vhod kot interrupt (GPIO_EXT...) in izhod za zeleno LED.
   Zapišite izbrana pina.
   - Izbral sem input pin PA0 (moder PushButton) ter output pina PC8 (modra LED) ter PC9 (zelena LED).



3.

d) Ukaz za vklop/izklop zelene LED.
   - HAL_GPIO_TogglePin(GPIOC, GPIO_PIN_9); 

e) Koliko znaša (v mili sekundah) zapisana zakasnitev?
   - Zakasnitev znaša 500 mili sekund.

f) Ukaz za utripanje modre LED.
  - HAL_GPIO_TogglePin(GPIOC, GPIO_PIN_8);

g) V to zanko dodajte ukaz za zakasnitev s funkcijo Delay iz knjižnice HAL, in sicer pol sekunde.
   - HAL_Delay(500);



4.

b) Opazujte utripanje modre LED. Kaj se zgodi, ko pritisnemo na modro tipko STM32F0?
   - Modra LED še vedno utripa, kakor prej.

c) Ali pritisk na modro tipko vpliva na utripanje modre LED in zakaj?
   - Modra tipka ne moti delovanja modre LED zaradi funkcije "while". Zelena LED ne moti modre LED.



Komentar:
 - Sprva sem imel malo težav z iskanjem NVIC configuration. Ko sem to našel in vklopil, je vse delovalo kot je treba.

