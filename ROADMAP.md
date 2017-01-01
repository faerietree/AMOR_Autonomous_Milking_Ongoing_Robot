#Roadmap


* Es gilt zunächst eine Mechanik aufzubauen, die das entwickelte Vakuumsystem enthält.
* Dann Eutererkennung voranzutreiben. (unter Verwendung des RobotOperatingSystem), um das Rad nicht neu zu erfinden. Das Ergebnis wird an die
* Manipulatorsteuerung weitergegeben. Andocken! (Feedback, high level control by Jetson, which is pausing other services like web if necessary)
* Tor- und Fütterungssystem (einfacher als vorangehende Punkte).
* Während des Melkvorgangs übernimmt ARM Jetson die Kontrolle der Milch-Messwerte, speichert sie in einer
* SQLLite oder UnQLite Datenbank (je immer nur eine Datei, letzteres speichert Schlüssel-Werte Paare, ersteres erlaubt SQL Abfragen). Ferner ist Jetson während dieser für ihn ruhigen Zeit für Webrequests als
* Webserver verfügbar. (da kann so viel schief gehen, dass in der Zeit kein zeitkritischer Task vom Hauptprozessor ausgeführt werden kann (selbst mit RealTime Kernel). Der 4-Kern ist also nur für das eine oder das andere verwendbar außer die 3D camera Daten Berechnungen laufen auf CUDA.)
* Der arduino-kompatible eingebettete Echtzeit-Cortex-M3 Mikrorechner <strike>kontrolliert die Vakuum-Messwert-Erfassung</strike> (zunächst kein Sensor vorhanden!) und die
    <strike>Steuerung der Vakuumpumpe und</strike> Ventile.

