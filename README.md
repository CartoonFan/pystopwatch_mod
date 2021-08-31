# pystopwatch_mod

A fork of Xyne's [pystopwatch](https://xyne.archlinux.ca/projects/pystopwatch/)
with some extra features.

---
# Name

pystopwatch - A stopwatch written in Python with a clock and two countdown functions that can minimize to the tray.

# Synopsis
`pystopwatch`




# Description
pystopwatch is a simple GUI stopwatch emulator with 4 modes:

Current Time
:   This mode shows the current system time by default but may be adjusted by the user. To shift the time, press stop, adjust the time accordingly, then press start. "Reset" will reset the time to the system time.

Stopwatch
:   This mode measures the time that has passed since it was started.

Countdown Timer A
:   This mode will count down a given amount of time, e.g. 15 minutes. When the time is up, it will trigger the alarm.

Countdown Timer B
:   This mode will count down to a given time, e.g. 18:00 (6:00 PM). It will also trigger the alarm when the time is reached.

Left-clicking the tray icon will toggle minimizaion to the tray while right-clicking will display a menu to access the preferences and help dialogues as well as quit the application. This menu can also be accessed by right-clicking the display frame in the main window.


# Hotkeys

"h", "m" and "s" increment hours, minutes and seconds, respectively. "H", "M" and "S" decrement the same. The tab key and <alt>+m toggle the mode, "r" and "<alt>+r" activate reset, and space toggles the start and stop button.




# Preferences
alarm command
:   If set, the alarm command will be executed when the alarm is triggered. See the section below for examples.

alarm text
:   If set, a window will pop up in the center of the screen with this text when the alarm is triggered. The control sequence "%t" will be replaced with the current time as displayed in pyStopwatch. To display a literal "%t", use "%%t".

    If the alarm text begins with "#!", the rest of the text is interpretted as a command and its output will be used as the alarm text. For example, "#!date" would display the output of the "date" command in the alarm text popup window.

The rest of the options should be self-explanatory.



# Alarm Command Examples
Always add an ampersand ("&") to the end of your alarm command to background the process, otherwise pyStopwatch will lock while waiting for the command to finish. Here are some examples of what can be done when the alarm is triggered:

`mpg123 /path/to/some_song.mp3 &`
:   play some_song.mp3

`flite "some text to be spoken" &`
:   have flite say something

`feh /path/to/some_img.jpg &`
:   display some_img.jpg

`/path/to/some/script &`
:   run a script or other command 
