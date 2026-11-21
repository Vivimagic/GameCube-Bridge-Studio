<img width="150" height="150" alt="vivimagic-w012-installer" src="https://github.com/user-attachments/assets/246deaee-5015-44d3-b92a-7ddd40f881b5" /><?xml version="1.0" encoding="UTF-8"?>
# GC-Controller-Bridge
This is a fresh driver setup for the Mayflash adaptor to enable vibration for Steam on Windows, Mac and Linux.

When the Mayflash W012 rear switch is set to PC mode, it enumerates as a legacy DirectInput gamepad (0079:1846). Modern PC games expect XInput (Xbox 360/One), so controllers only respond when Steam forces Generic Gamepad wrapping — which strips force-feedback commands.

1. Wii U / NS Mode
Flipping the switch exposes native 057E:0337 with raw 4-port polling and binary rumble commands.

2. Dual USB Power
Both USB plugs must be connected: Black carries data, while the Gray plug exclusively powers the 5V rumble motors.

3. Single-Install Service
One installer binds WinUSB + signed XInput silently and auto-starts on boot — no Zadig clicks or apps to launch.

For more information on the license please go here: https://github.com/Vivimagic/GC-Controller-Bridge/blob/main/License
