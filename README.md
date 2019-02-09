IThermometer ESP OLED
=====================

WIFI Thermometer ESP OLED Kombi für Brauerei  
http://www.schopfschoppe.de/Download.html

Danksagung:
-----------

Ein großes Dankeschön soll an dieser Stelle an universam gehen, der mit seiner
ISpindel praktisch eine fast fertige Vorlage für meinen Thermometer geliefert
hat.  
https://github.com/universam1/iSpindel  
Ebenfalls Danke möchte ich glassart sagen, der mich immer kräftig beim Testen
unterstützt.

Bauteileliste:
--------------

-   ESP8266 OLED Kombi (Siehe Bild unten)

-   DS18B20 Temperatursensor

-   Widerstand 4,7 KOhm

-   ggf. USB-Kabel und USB-Steckernetzteil ( hat wohl jeder heute was rum zu
    liegen )

Sieht kompliziert aus, ist es aber gar nicht ....

IThermometer gem. Schaltplan.jpg verdrahten

![Schaltplan](Schaltplan.jpg)

Installation:
-------------

-   IThermometer am USB-Port anschließen

-   ESP8266Flasher.exe **mit Adminrechten** öffnen ( Rechtsclick - Als
    Administrator ausführen )

-   Auf Config Reiter wechseln

-   IThermometer_ESP_OLED.bin öffnen ( Erstes Zahnrädchen )

-   Auf Operation Reiter wechseln

-   COM-Port des WEMOS auswählen

-   Flashen

### Der IThermometer ist fertig !

Bedienung:
----------

-   Zwei mal Reset am WEMOS drücken, dazwischen ein zwei Sekunden Pause lassen.

-   WEMOS spannt ein eigenes WLAN-Netzwerk auf, die LED am WEMOS leuchtet
    durchgehend.

-   Mit geeignetem Gerät mit dem WLAN des WEMOS verbinden ( z.B. Handy, Tablet,
    Laptop.... )

-   Browser an dem verbunden Gerät öffnen.

-   Wenn die Config-Seite nicht automatisch öffnet im Browser die Adresse
    192.168.4.1 eingeben

-   Auf Config clicken und die WLAN-Daten eingeben - anschliessend "SAVE"
    drücken

-   Der WEMOS prüft jetzt, ob die Eingaben stimmen, verbindet sich mit dem
    angegebenen WLAN-Netzwerk.

Verhalten:
----------

Der WEMOS sendet jetzt im 5 Sekundentakt UDP-Nachrichten auf dem eingegeben Port
durchs Netzwerk.

Bedienung in der Brauerei:
--------------------------

-   In der Brauerei Temperaturmessung "Arduino" wählen.

-   Auf dem Arduino Reiter "LAN/WLAN" wählen und den passenden "Port-IN" wählen

-   "Port-Out", "IP-Out" und "Sensortyp" spielen für das iThermometer keine
    Rolle.

Abschluss:
----------

Fertig, die Brauerei sollte jetzt die Temperatur anzeigen. Diese Prozedur ist
nur einmal nötig. Die Einstellungen bleiben in der Brauerei und im WEMOS
erhalten. Will man die Einstellungen ändern, 2x mit kurzem Abstand Reset am
WEMOS drücken. Die USB-Verbindung ist ebenfalls nicht mehr nötig. Der WEMOS kann
mit einem beliebigen Handy-USB-Ladegerät mit Spannung versorgt werden. Die
Datenübertragung erfolgt kabellos per WLAN.
