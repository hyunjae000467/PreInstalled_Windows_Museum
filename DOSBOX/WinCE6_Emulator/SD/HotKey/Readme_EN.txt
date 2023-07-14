HotKey 

With this program, can the keys of the PDA / PNA 's up to two programs assign, in a long time or even holding down the button to start. When the button is released after the brief wait, Program 1, when the key is longer than the long wait gedrücktgehalten will automatically program 2 starts. If the button even before the first qualifying period is released, this corresponds to a normal keypress and it is not a program. 
The configuration will have a ini file. 

If hot keys are loaded, the program disappears as a small icon in the systray and can click through on your screen are. 
In the program window to see the keycodes of the keys look to include them in the ini to be able to register. Right there are three buttons: 
With D disables the hotkeys, you can be then re-enable with E and with the sign bottom right of the window can be re-send Systray. 

If a program on a hotkey to start a second time before the first has finished, the program asks whether the first scheduled to be in the rule should be here with no reply, and manually to the first instance of the current program has to be changed. 

Configuration: 

The file "HotKey.ini" must be in Unicode format (eg Notepad-> Save As-> Encoding-> Unicode) and in the same directory as HotKey.exe are. 
All possible settings are exemplary in the enclosed Ini made. Here with the statement: 


SETTINGS		-> General Settings 
ElapseTimeShort = 300 	-> the time how long a key must be kept in milliseconds to start the first program 
ElapseTimeLong = 1500 	-> the time how long a key must be kept in milliseconds to the start of the second program 
CheckIntervall = 32 	-> the interval in which, after pressing a button is checked whether the button was released early, the minimal delaying a key pressure, the value should not be too high, 20 - 50 is quite good, then you notice the Delay is not yet 
QueryTermination = yes 	-> Ask for whether an ongoing process to be terminated if another times hotkey is pressed, the 'no' is not in demand, the process is closed and will not start again. 

HotKey 			-> 1 st Hotkey 
Keycode = 193 		-> Zoom + button of the T5000 
CommandShort = \ 	-> The job is open 

HotKey 					-> the 2nd Hotkey 
Keycode = 196 				-> navigation button, the T5000 
CommandShort = \mnav\mnavdce.exe	-> Mobile Navigator 5 start (when you press the button for longer than shorter than 0.3s and 1.5s) 
Disable = yes 				-> run with this hotkey, all hotkeys disable 

HotKey 						-> of the 3rd Hotkey 
Keycode = 38 					-> "Top" button 
CommandLong = \Program Files\MoveWindow.exe	-> start MoveWindow (when you press the button for longer than 1.5s) 

HotKey 							-> the 4th Hotkey 
Keycode = 195 						-> Back button (<-) button on the T5000 
CommandShort = \Program Files\ShowTaskbar.exe 		-> start ShowTaskbar (when holding down recently) 
CommandLong = \Program Files\PeriodicShowTaskbar2.exe	-> start PeriodicShowTaskbar (for holding down long) 

HotKey 							-> the 5th Hotkey 
Keycode = 37 						-> "Left" button 
# Command = \mnav\mnavdce.exe 				-> at the same time could also be a program 
NewIni = \Program Files\Hotkey\specialHotkeys.ini 	-> execute with this hotkey, the hotkey from the specified file 




Changes in version 1.2: 
------------------------ 
It can store up to two programs with one button, depending on the duration of the holding will be the first time or keep the second program. Very useful for devices with very few or even just a single button. 

Changes in version 1.1: 
------------------------ 
The attribute "NewIni" can be another Ini after running the hot keys are loaded. 
The old hotkeys no longer work, so they are always just a hotkey Ini active. 
An example of the new attribute in the above example involved.