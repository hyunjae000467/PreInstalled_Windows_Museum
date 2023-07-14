HotKey

Mit diesem Programm kann man den Tasten des PDA/PNA's bis zu zwei Programme zuordnen, die bei l�ngerem oder noch l�ngerem Gedr�ckthalten der Taste gestartet werden. Bei loslassen der Taste nach der kurzen Wartezeit wird Programm 1 gestartet, wenn die Taste l�nger als die lange Wartezeit gedr�cktgehalten wird, wird automatisch Programm 2 gestartet. Wenn die Taste noch vor der ersten Wartezeit wieder losgelassen wird, entspricht dies einem normalen Tastendruck und es wird kein Programm gestartet.
Die Konfiguration wird �ber eine Ini-Datei vorgenommen.

Wenn Hotkeys geladen wurden, verschwindet das Programm direkt als kleines Icon im Systray und kann durch klick auf den Bildschirm geholt werden.
Im Programmfenster kann man sich die KeyCodes der Tasten anschauen, um sie in der Ini eintragen zu k�nnen. Rechts befinden sich drei Schaltfl�chen:
Mit D deaktiviert man die Hotkeys, entsprechend kann man sie danach mit E wieder aktivieren und mit dem Zeichen unten rechts kann man das Fenster wieder ins Systray schicken.

Wird ein Programm �ber einen Hotkey ein zweites mal gestartet, bevor das erste beendet wurde, fragt das Programm nach, ob das erste terminiert werden soll, in der Regel sollte hier mit nein geantwortet werden und manuell zur ersten Instanz des schon laufenden Programms gewechselt werden.

Konfiguration:

Die Datei "HotKey.ini" muss im Unicode-Format gespeichert sein (z.B. Notepad->Speichern Unter->Codierung->Unicode) und sich im selben Verzeichnis wie HotKey.exe befinden.
Alle m�glichen Einstellungen sind beispielhaft in der beiligenden Ini vorgenommen. Hier mit Erkl�rung:


SETTINGS		-> Allgemeine Einstellungen
ElapseTimeShort = 300	-> die Zeit, wie lange eine Taste gedr�ckt gehalten muss in Millisekunden, bis zum Start des ersten Programms
ElapseTimeLong = 1500	-> die Zeit, wie lange eine Taste gedr�ckt gehalten muss in Millisekunden, bis zum Start des zweiten Programms
CheckIntervall = 32	-> das Intervall, in dem nach Dr�cken einer Taste gepr�ft wird, ob die Taste fr�hzeitig losgelassen wurde, entspricht der minimalen Verz�gerung eines Tastendrucks, der Wert sollte nicht zu hoch sein, 20 - 50 ist ganz gut, dann merkt man die Verz�gerung noch nicht
QueryTermination = yes	-> Fragt nach ob ein noch laufender Prozess terminiert werden soll, wenn ein weiteres mal der Hotkey gedr�ckt wird, bei 'no' wird nicht nachgefragt, der Prozess nicht geschlossen und auch nicht nochmal gestartet.

HOTKEY			-> der 1. Hotkey
KeyCode = 193		-> Taste Zoom+ des T5000
CommandShort = \	-> Der Arbeitsplatz wird ge�ffnet

HOTKEY					-> der 2. Hotkey
KeyCode = 196				-> Navigationstaste, des T5000
CommandShort = \mnav\mnavdce.exe	-> Mobile Navigator 5 starten (bei Tastendruck l�nger als 0.3s und k�rzer als 1.5s)
Disable = yes				-> mit ausf�hren dieses Hotkey, werden alle Hotkeys deaktivieren

HOTKEY						-> der 3. Hotkey
KeyCode = 38					-> "Nach Oben" Taste
CommandLong = \Program Files\MoveWindow.exe	-> starte MoveWindow (bei Tastendruck l�nger als 1.5s)

HOTKEY							-> der 4. Hotkey
KeyCode = 195						-> Zur�cktaste (<-) Taste des T5000
CommandShort = \Program Files\ShowTaskbar.exe		-> starte ShowTaskbar (bei kurzem gedr�ckthalten)
CommandLong = \Program Files\PeriodicShowTaskbar2.exe	-> starte PeriodicShowTaskbar (bei langem gedr�ckthalten)

HOTKEY							-> der 5. Hotkey
KeyCode = 37						-> "Nach Links" Taste
#Command = \mnav\mnavdce.exe				-> gleichzeitig k�nnte auch ein Programm gestartet werden
NewIni = \Program Files\Hotkey\specialHotkeys.ini	-> mit ausf�hren dieses Hotkey, werden die Hotkeys aus der angegebenen Datei geladen




�nderung in Version 1.2:
------------------------
Es k�nnen bis zu zwei Programme mit einer Taste gestartet werden, je nach Zeitdauer des Gedr�ckthaltens wird das erste oder bei l�ngerem halten das zweite Programm gestartet. Sehr n�tzlich bei Ger�ten mit sehr wenigen oder gar nur einer einzigen Taste.

�nderung in Version 1.1:
------------------------
Mit dem Attribut "NewIni" kann eine andere Ini nach dem Ausf�hren des Hotkeys geladen werden.
Die alten Hotkeys funktionieren danach nicht mehr, es sind also stets nur die Hotkeys einer Ini aktiv.
Ein Beispiel des neuen Attributes wurde in das obige Beipsiel eingebunden.