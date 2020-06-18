# Marlin-bugfix-2.0.x-Smart-Filament-Sensor
BTT 32bit board with LPC1768, build with marlin 2.0.x nightly bugfix, support BTT LCD E3 V2, On-board TMC2209 UART interface and 
BTT Smart Filament Sensor

Pls note that I am using youtuber "teaching tech" layout if you are using a different layout it may not work for you.

Note that if you are getting "TMC CONNECTION ERROR" this is likely due to that you are using the USB 5V 
to drive your SKR board, pls switch to the main PSU to drive the SKR board.

The BTT Smart Filament Sensor can be mount before or after the stepper motor that drive the filament.
I chose to install the sensor before teh stepper motor as this is a better position as once I get notify
by the Octoprint through Telegram I can still have sufficient filament left that I can pull the leftover
filament and insert a new roll of filament.

The following set in Configuration.h it works better
RUNOUT_DISTANCE_MM 25

the pins for the runout sernsor is P1_26, files located in lpc1768/pins_BTT_SKR_V1.4.h  
#define FIL_RUNOUT_PIN                     P1_26  // E0DET

