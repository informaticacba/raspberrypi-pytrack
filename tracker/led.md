# Python LED Module - led.py

This library provides access to the PITS+ / PITS Zero LEDS.

## Sample Usage

	from led import *
	from signal import pause
	
	print("Creating LED object ...")
	status_leds = PITS_LED();
	
	status_leds.fail()
	pause()

This causes the LEDs to both flash.


## Reference

### Object Creation

	PITS_LED()

WhenNewPosition and WhenLockChanged are callbacks (see below).

### Functions

	fail()

Blinks both LEDs at 5Hz; used to indicate a catastrophic failure (e.g. tracker software cannot start)

	GPS_LockStatus(HaveLock)

Used to indicate if we have GPS lock or not.

GPS lock is indicated by the green "OK" LED flashing at 2Hz, and the red "Warn" LED off.

No GPS lock is indicated by the red "Warn" LED flashing at 2Hz, and the green "OK" LED off.
 
## Testing

Run the supplied test program to flash both LEDs at 5Hz:

	python3 test_leds.py
