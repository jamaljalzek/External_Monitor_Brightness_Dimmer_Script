# External Monitor Brightness Dimmer
The purpose of this script is to help you fall asleep easier by reducing the light output of your monitor before bed time. This is similar to apps such as f.lux (https://justgetflux.com/) and LightBulb (https://github.com/Tyrrrz/LightBulb). At the time of writing this script, those apps do not directly dim a monitor's backlight, but simulate a dimming effect through changing display color settings. This isn't completely effective because the backlight still bleeds through, which can cause blacks to look more gray. It is recommended to pair this script with one of the above apps, as you get the best of both worlds.

This script is compatible with external monitors that implement the DDC/CI standard, calling upon functions from Microsoft Windows' Win32 C++ API. Specifically, monitors that implement functionality that allow desktop applications to read and change their backlight brightness.

When launched, the script sleeps until the predefined start time. Then, it gradually dims the physical backlight of the primary external monitor over the predefined duration to its minimum supported value. To change the dimming start time and/or dimming duration:
1. Launch the script.
2. In the taskbar's tray menu (located near the date and time) right click on the script icon, opening its menu.
3. In the script menu, select "Edit dimming settings". This will open up a new window, showing you the current settings and allowing you to update them.

To run the script, you can launch it manually by double clicking it (with AutoHotkey installed). To have the script automatically launch on start-up:
1. Create a shortcut for the "MonitorBrightnessDimmer Main Class.ahk2" file.
2. Place the shortcut in one of the start-up folders:
    a. For all users on a PC: "%PROGRAMDATA%\Microsoft\Windows\Start Menu\Programs\StartUp"
    b. For just one (the current) user on a PC: "%APPDATA%\Microsoft\Windows\Start Menu\Programs\Startup"

This script is written in and only compatible with AutoHotkey 2 (https://www.autohotkey.com/), as well as Microsoft Windows. If desired, you can bundle the script files with the AutoHotkey interpreter into a self-contained executable file for portability: https://lexikos.github.io/v2/docs/Scripts.htm#ahk2exe