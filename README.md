# Trinket-Battery-Shield
Adafruit Trinket Shield for Battery Charging and RGB status LED.

![Trinket Battery Charging Shield Front](https://raw.githubusercontent.com/bwshockley/Trinket-Battery-Shield/master/trinket_battery_charging_shield.png)
![Trinket Battery Charging Shield Back](https://raw.githubusercontent.com/bwshockley/Trinket-Battery-Shield/master/trinket_battery_charging_shield_2.png)

## About
This is an add-on circuit board for the [Adafruit Trinkets](https://www.adafruit.com/?q=trinket&).  This board adds a battery connector with an MCP73831 lipoly/NMhi battery charger set at 100mAH charging.
The charger has two indicator LEDs, one to indicate the battery is currently charging from the micro-usb port on the Trinket, and the other to indicate when the battery has fully charged.

## WS2812B LED
There is a pad for a WS2812B RGB LED.  This LED is connected to data pin #0.  The user can leave this LED unpopulated if only battery charging capability is required.

## Battery Power
Note that the Adafruit Trinkets come with circuits for using the battery power and automatically switching between USB power and battery power as needed.  If the user only wishes to have battery power and not the charging capability, the user only needs to populate the JST 2-Pin connector on the back of the Trinket.

## BOM
C1, C2 = 0805 series SMT capcitors 10uF and at least 10V to be safe.
R1, R2 = 0805 resistors.  These resistors determine the current each status LED uses.  Charging LED should not sink more than 25mA, and Done LED should not source more than 35mA.
R3 = 0805 resistor at 10KOhm.  This sets the charger at 100mAh.  Other values possible.  Recommend 100mAh.

IC1 = MCP73831T battery charging IC.

J1 = JST-2_SMD - Available via Adafruit, Sparkfun, or Mouser.

LEDs = 0805 LEDs. Not necessary for circuit to work.  Recommended LEDS:

* SML-LX0805SOC-TR (Orange) Charging LED with R1 = 390Ohm minimum
* SML-LX0805SUGC-TR (Green) Charged or Done LED with R2 = 270Ohm minimum

WS2812B LED - Not necessary, but if the user chooses to add, LED must be 5050 size.
