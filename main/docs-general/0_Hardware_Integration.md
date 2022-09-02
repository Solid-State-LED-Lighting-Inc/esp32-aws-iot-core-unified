//
// LEDs
//
You may integrate up to 4 color indicators by simply assigning 4 GPIO pins over at indication_defs.hpp

Two entries please.  Here is an example:

#define LED_NAME GPIO_NUM_XX

#define ColorA LED_NAME

Use LED_NAME throughout the application.  The Indication object is a strong tool for creating feedback with one or two of the first colors.  Also note that you get feedback software verson over 3 LEDs on start of the application during POTs.  Software version is set over in system_defs.hpp

//
// SWITCHs
//
Switches are important for input during development.  They must be wired into the correct ISR over in system_gpio.  We use a RTOS queue to handles all GPIO events.  Follow
the pattern you see there for good results.

Example define:

#define GPIO_YOUR_SW GPIO_NUM_XX

Use GPIO_YOUR_SW in the code as needed.

//
// NOTHING ELSE IN HARDWARE TO INTEGRATE AT THIS TIME
//
