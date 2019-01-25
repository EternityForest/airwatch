# AirWatch: ESP8266 I2C/ADC/Battery board

#AS IS!!!!!
I've changed some stuff since actually building these. I'll write some proper docs eventually I suppose.
Mostly just gettingthis under VC.

## Features/Hacks used

* Somethinng is wrong with the 0805 footprints. The
* There's a ton of voltage  drop on the way to the battery. 
* It might only charge to 50% from 5v. Good enough, they don't like full charge anyway.
* WiFi Is Fussy! Or maybe it isn't? I'm testing with unfinished code.
* Totally untested fancy easy to solder bigger 0805 pads!

* You can't use the TX pin, it controls the battery charger
* Ok, maybe the world won't end if you send some stuff anyway?
* You can controll the charger!
* 5v-24v input.
* No onboard programming
* A button! It conflicts with the RX pin!
* A power switch! That actually disconnecxts the battery!
* A reliance on the load dump protectionof the LDO
* ^ to save it from the tiny reverse current in battery mode when filling the input cap
* An ADC(ADS1015 at 0x49, not the adafruit lib default)

* read the schematic
* a transistor as a standin for a reg I didn't have a footprint for
* The reg will probably overheat if you use it from more than 7v or so, unless you're always in sleep mode.
* Will probably not work at all if you use a cheaper LDO
* seriously read it

