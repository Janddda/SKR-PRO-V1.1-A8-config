# Disclaimer

Use at your own risk, this code is here if you know and understand what you are looking for. Applying unknown code on your hardware is always very dangerous.

# Notes

- This configuration is for the Marlin 2.0.x branch and was tested with the bugfix-2.0.x branch.
- Hardware is the Anet A8, for a SKR PRO 1.1 with 4 DRV8825 configured to 16 steps (The original A8 board uses 16steps drivers as well).
- LCD code is disabled since the A8 LCD panel is not compatible with the board. The pin for driving the buttons is 5V but the LCD from the A8 expects 3.3V. Connecting it to the board would destroy the microcontroller of the LCD.

# Installation

- Copy the config files in the Marlin source root folder
- Use `platformio run -e BIGTREE_SKR_PRO`
- Copy .pio/build/BIGTREE_SKR_PRO/firmware.bin to the root of the sdcard. The green led will blink for a few seconds during the flashing process.

# About the repo
This repo is not meant to be maintained since I now changed a lot of the hardware. You can build your own configuration from this example but it might not be compatible with the latest commits of Marlin. 
The commit b7f81632917f0a0da7d7dc974bd60dca9274d6c0 from bugfix-2.0.x is known to succesfully compile and work.

