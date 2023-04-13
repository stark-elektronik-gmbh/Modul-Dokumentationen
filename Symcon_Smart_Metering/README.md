# Symcon_Smart_Metering
Das Modul dient dazu die Smart Energy Log 2.0 Geräte von Stark Elektronik in Symcon zu integrieren. 

<img src="imgs/SmartEnergyLog20.png" width="40%" >

Der Smart Energy Log ist eine Kommunikationszentrale zur Erfassung von Verbrauchs- und Sensordaten via M-Bus wM-Bus.

Bezug über https://stark-elektronik.de/

* <a href="http://example.com/](https://www.stark-elektronik.de/epages/63653058.sf/de_DE/?ObjectPath=/Shops/63653058/Products/SE-LOG-2.0">Direktlink: Smart Energy Log 2.0</a>

* <a href="http://example.com/](https://www.stark-elektronik.de/epages/63653058.sf/de_DE/?ObjectPath=/Shops/63653058/Products/SE-LOG-2.0G">Direktlink: Smart Energy Log 2.0 mit LTE</a>


# Vorraussetungen 

* IP-Symcon (Mind. Version 5.5)
* Stark Elektronik Smart Energy Log 2.0 mit mindestens einem Sensor.

# SmartLog
Der SmartLog spiegelt ein physisches Smart Energy Log Gerät wieder. Es kann eine beliebeige Anzahl von Geräten verwedent werden (in der Praxis abhängig von der Leistung der Symcon-Instanz und der Aktualisierungsrate der Messwerte).
Der SmartLog stellt einen MQTT Client dar und verbindet sich mit dem Symcon-MQTT-Server.

__Konfigurationsseite__:

Name     | Beschreibung
-------- | ------------------
SmartLog ID         |Die SmartLog ID dient dazu, die Empfangen Daten dem richtigen SmartLog Gerät zuzuordnern
      

# SmartMeter
Das SmartMeter repräsentiert einen Zähler oder Sensor, der mit dem SmartLog Verbunden ist. Die einzelnen Parameter des Gerätes werden automatisch erstellt.

__Konfigurationsseite__:

Name     | Beschreibung
-------- | ------------------
SmartMeter ID         | Die SmartMeter ID dient dazu die die Empfangenen Daten dem richtigen Zähler oder Sensor zuzuordnern. Die ID wird beim Erstellen über den SmartMeterConfigurator automatisch zugewiesen. 
 Variablen automatisch erstellen        | Wenn das Flag "Variablen automatisch erstellen" ist werden die Von dem Sensor übertragen Daten automatisch als Variablen angelegt. Möchte man nicht alle Variablen nutzen kann man diese Funktion abschalten und die überflüssigen Variablen löschen. Bleibt die Funktion aktiv, werden auch neue oder selten gesendete Werte als neue variablen in Symcon angelegt

 # System
Die System Instanz visualisiert die Systemvariablen einer SmartMeter Loggers.

__Konfigurationsseite__:

Name     | Beschreibung
-------- | ------------------
SmartMeter ID         | Die SmartMeter ID dient dazu die die Empfangenen Daten dem richtigen Zähler oder Sensor zuzuordnern. Die ID wird beim Erstellen über den SmartMeterConfigurator automatisch zugewiesen. 
 Variablen automatisch erstellen        | Wenn das Flag "Variablen automatisch erstellen" ist werden die Von dem Sensor übertragen Daten automatisch als Variablen angelegt. Möchte man nicht alle Variablen nutzen kann man diese Funktion abschalten und die überflüssigen Variablen löschen. Bleibt die Funktion aktiv, werden auch neue oder selten gesendete Werte als neue variablen in Symcon angelegt

# SmartMeterConfigurator
Der SmartMeter Configurator wird für jedes SmartLog Separat angelegt und bietet die Möglichkeit die SmartMeter automatisch erstellen zu können. 

<img src="imgs/struktur.png" width="80%" >

# Installation
Im Symcon Store das Modul "Smart Metering" von Stark Elektronik GmbH auswählen und installieren. 


<img src="imgs/symconModul.png" width="40%" >

Hier wird man gefragt ob man eine SmartMeterConfigurator Instanz erstellen möchte. 
Dann wird man von Symcon automatisch dur die Einstellungen der Instanzen von SmartLog, MQTT-Server und Server Socket geführt. 

<img src="imgs/symconModulInstallation.png" width="40%" >

(Sofern auf dem System bereits MQTT-Server installiert sind muss der Server für die SmartLogs ggf manuell angelegt werden)

Nach erfolgreicher installation werden neue SmartLog Instanzen automatisch im SmartMeterConfigurator angezeigt und können erstellt werden.

<img src="imgs/symconConfigurator.png" width="80%" >


Die SmartMeter Instanzen werden unter SmartMetering/SmartLog[SmartLogID]/[Sensortyp]/[SensorID] angelegt. Die Variablennamen können nach belieben angepasst und an einen anderen Ort verschoben werden.   



