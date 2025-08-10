Frage: Warum wird der Typ Zero von Arduino verwendet?  
Antwort: Es handelt sich beim Zero um eine verbesserte Version des bekannten Arduino Uno mit einem wesentlich schnelleren Prozessor und viel größerem Speicher. Das Wesentliche ist jedoch, dass er mit einer Spannung von 3,3 Volt arbeitet, und nicht mit 5 Volt wie die meisten Arduinos. Dadurch entfallen "Pegelwandler" zu den meist mit 3,3 Volt betriebenen Sensoren. Eine Alternative wäre noch ein Prozessor aus der ESP32-Serie. Hier hat sich jedoch gezeigt, dass die Erzeugung des Programmcodes sehr lange dauert, was bei Wettbewerben hinderlich ist.

Frage: Wozu braucht die Motorsteuerung einen eigenen Prozessor?  
Antwort: Man könnte die Schrittmotortreiber auch direkt vom Arduino ansteuern, dann gingen aber schnell dessen Digitalanschlüsse aus. Mit einem zusätzlichen Prozessor ESP32-S3 ist eine I2C-Bus-Anbindung möglich, die sowieso vorhanden ist. Der ESP32 setzt einfach die Befehle von I2C in Schrittmotor-Signale um. Da der ESP32-S3 zwei Kerne besitzt, kann die Motorsteuerung unabhängig erfolgen, d.h. der Arduino kann weiter arbeiten und I2C-Befehle senden, während die Motoren laufen.

Frage: Warum ist kein Gyro-Sensor bei db-robotix enthalten?  
Antwort: Gyroskope sind für die Winkelbestimmung zu ungenau und arbeiten unzuverlässig. Details findest du unter: https://github.com/db-robotix/Unterricht/blob/main/Gyrosensorik.pdf  

Frage: In den Software-Bibliotheken finde ich kein Programm zur Linienverfolgung. Warum?  
Antwort: In den Libraries anadigMaster und i2cMaster sind nur elementare Funktionen für die Komponenten enthalten, denn du sollst dich selber mit der Roboter-Programmierung für Wettbewerbe beschäftigen und dadurch lernen. Wenn du noch keine Idee hast, kannst du in https://github.com/db-robotix/Projekt/blob/main/ProgrammierAnleitung.pdf lernen, was hinter einer Linienverfolgung steckt.

Frage: Gibt es auch eine grafische Programmiermöglichkeit für Anfänger?  
Antwort: Nein. Du sollst hier lernen "richtig" zu programmieren. Grafische Programme wie z.B. Sketch sind zwar geeignet, einen spielerischen Einstieg in das Programmieren zu finden, "Profis" nutzen aber höhere Programmier-Sprachen. Außerdem werden grafische Lösungen schnell unübersichtlich.

Frage: Warum wird in C programmiert und nicht in Python?  
Antwort: Durch die Programmieroberfläche Arduino-IDE erhältst du ein weit entwickeltes, kostenloses Tool - optimiert für Arduinos und mit vielen frei verfügbaren Bibliotheken. Und diese IDE basiert eben auf der (auch bei Profis weit verbreiteten) Sprache C. Außerdem wird Python nur mit so genannten "Interpretern" genutzt, die die Programmausführung sehr verlangsamen.

Frage: Welches Alter wird für das Arbeiten mit diesem Projekt empfohlen?  
Antwort: Das kann man nicht generell sagen, da es sehr vom Wissenstand abhängt. Ab 14 Jahren ist es bestimmt lohnenswert, sich mit diesem Projekt zu beschäftigen. Aber es gibt sicherlich auch Jüngere, die sehr wissensdurstig in der Technik sind. Teilnehmer an der World Robot Olympiad dürfen maximal 18 Jahre alt sein.

Frage: Wie kann ich am Wettbewerb "World Robot Olympiad" teilnehmen?  
Antwort: Auf der Webseite https://www.worldrobotolympiad.de findest du alle Informationen dazu. Es besteht zwar die Möglichkeit, als "Privat-Team" teilzunehmen, Anfängern empfehle ich jedoch, sich einer Organisation anzuschließen. Frage mal in deiner Schule nach, ob dort Robotik-Kurse angeboten werden. In manchen Orten gibt es auch Vereine, die solche Kurse organisieren und Gruppen betreuen. 

Frage: Muss ich die Unterlagen in https://github.com/db-robotix/Lessons lernen und verstehen?  
Antwort: Nein. Den Roboter-Bau und die Programmierung kannst du auch so bewerkstelligen. Denn diese Unterlagen gehen recht tief in die Physik. Wenn du jedoch an dem Bezug zwischen Robotik und Physik stark interessiert bist, lohnt es sich, mal hinein zu schauen.
