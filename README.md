# monostable_LCD_backlight
555 timer monostable (one shoot) based power supply, used with dual function gas heater controller.
This particular controller was located in dark basement, where LCD wasn't easily readable. Controller LCD already had LEDs and resistors in place, but it was lacking the rest of circuitry to drive backlight.
J1 is connected to controller board voltage (approx. 12V), left encoder button, which acts as a trigger for backlight and GND.
J2 is connected to LED circuit, already embedded in LCD and GND. Current limiting resistors were already present.
7.5V was calculated as optimal voltage output to drive LEDs. 
LDO had to be inserted on external board, because this part of controller board was not populated.

# electrical info
Vin ~> Vout + 2V (drop on 555) + 1V (drop on LDO)
Iin < 500 mA // LEDs and LDO draw about 40 mA in this configuration, so entire circuit can be powered of 555 timer leg.
Vout ~ 7,5 V, adjustable via R2 and R3 configuration
Ton ~ 30 seconds, adjustable via R1 and C2 configuration // T=1.1*R1*C2
