HotKey

Mit diesem Programm kann man den Tasten des PDA/PNA's bis zu zwei Programme zuordnen, die bei längerem oder noch längerem Gedrückthalten der Taste gestartet werden. Bei loslassen der Taste nach der kurzen Wartezeit wird Programm 1 gestartet, wenn die Taste länger als die lange Wartezeit gedrücktgehalten wird, wird automatisch Programm 2 gestartet. Wenn die Taste noch vor der ersten Wartezeit wieder losgelassen wird, entspricht dies einem normalen Tastendruck und es wird kein Programm gestartet.
Die Konfiguration wird über eine Ini-Datei vorgenommen.

Wenn Hotkeys geladen wurden, verschwindet das Programm direkt als kleines Icon im Systray und kann durch klick auf den Bildschirm geholt werden.
Im Programmfenster kann man sich die KeyCodes der Tasten anschauen, um sie in der Ini eintragen zu können. Rechts befinden sich drei Schaltflächen:
Mit D deaktiviert man die Hotkeys, entsprechend kann man sie danach mit E wieder aktivieren und mit dem Zeichen unten rechts kann man das Fenster wieder ins Systray schicken.

Wird ein Programm über einen Hotkey ein zweites mal gestartet, bevor das erste beendet wurde, fragt das Programm nach, ob das erste terminiert werden soll, in der Regel sollte hier mit nein geantwortet werden und manuell zur ersten Instanz des schon laufenden Programms gewechselt werden.

Konfiguration:

Die Datei "HotKey.ini" muss im Unicode-Format gespeichert sein (z.B. Notepad->Speichern Unter->Codierung->Unicode) und sich im selben Verzeichnis wie HotKey.exe befinden.
Alle möglichen Einstellungen sind beispielhaft in der beiligenden Ini vorgenommen. Hier mit Erklärung:


SETTINGS		-> Allgemeine Einstellungen
ElapseTimeShort = 300	-> die Zeit, wie lange eine Taste gedrückt gehalten muss in Millisekunden, bis zum Start des ersten Programms
ElapseTimeLong = 1500	-> die Zeit, wie lange eine Taste gedrückt gehalten muss in Millisekunden, bis zum Start des zweiten Programms
CheckIntervall = 32	-> das Intervall, in dem nach Drücken einer Taste geprüft wird, ob die Taste frühzeitig losgelassen wurde, entspricht der minimalen Verzögerung eines Tastendrucks, der Wert sollte nicht zu hoch sein, 20 - 50 ist ganz gut, dann merkt man die Verzögerung noch nicht
QueryTermination = yes	-> Fragt nach ob ein noch laufender Prozess terminiert werden soll, wenn ein weiteres mal der Hotkey gedrückt wird, bei 'no' wird nicht nachgefragt, der Prozess nicht geschlossen und auch nicht nochmal gestartet.

HOTKEY			-> der 1. Hotkey
KeyCode = 193		-> Taste Zoom+ des T5000
CommandShort = \	-> Der Arbeitsplatz wird geöffnet

HOTKEY					-> der 2. Hotkey
KeyCode = 196				-> Navigationstaste, des T5000
CommandShort = \mnav\mnavdce.exe	-> Mobile Navigator 5 starten (bei Tastendruck länger als 0.3s und kürzer als 1.5s)
Disable = yes				-> mit ausführen dieses Hotkey, werden alle Hotkeys deaktivieren

HOTKEY						-> der 3. Hotkey
KeyCode = 38					-> "Nach Oben" Taste
CommandLong = \Program Files\MoveWindow.exe	-> starte MoveWindow (bei Tastendruck länger als 1.5s)

HOTKEY							-> der 4. Hotkey
KeyCode = 195						-> Zurücktaste (<-) Taste des T5000
CommandShort = \Program Files\ShowTaskbar.exe		-> starte ShowTaskbar (bei kurzem gedrückthalten)
CommandLong = \Program Files\PeriodicShowTaskbar2.exe	-> starte PeriodicShowTaskbar (bei langem gedrückthalten)

HOTKEY							-> der 5. Hotkey
KeyCode = 37						-> "Nach Links" Taste
#Command = \mnav\mnavdce.exe				-> gleichzeitig könnte auch ein Programm gestartet werden
NewIni = \Program Files\Hotkey\specialHotkeys.ini	-> mit ausführen dieses Hotkey, werden die Hotkeys aus der angegebenen Datei geladen




Änderung in Version 1.2:
------------------------
Es können bis zu zwei Programme mit einer Taste gestartet werden, je nach Zeitdauer des Gedrückthaltens wird das erste oder bei längerem halten das zweite Programm gestartet. Sehr nützlich bei Geräten mit sehr wenigen oder gar nur einer einzigen Taste.

Änderung in Version 1.1:
------------------------
Mit dem Attribut "NewIni" kann eine andere Ini nach dem Ausführen des Hotkeys geladen werden.
Die alten Hotkeys funktionieren danach nicht mehr, es sind also stets nur die Hotkeys einer Ini aktiv.
Ein Beispiel des neuen Attributes wurde in das obige Beipsiel eingebunden.