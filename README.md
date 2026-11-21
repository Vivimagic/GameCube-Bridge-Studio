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

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <http://unlicense.org>
