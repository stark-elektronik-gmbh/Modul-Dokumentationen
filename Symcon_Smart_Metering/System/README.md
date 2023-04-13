# System
Die System Instanz legt die Systemvariablen des SmartMeter Loggers an.

### Inhaltsverzeichnis

- [System](#system)
    - [Inhaltsverzeichnis](#inhaltsverzeichnis)
    - [1. Funktionsumfang](#1-funktionsumfang)
    - [2. Vorraussetzungen](#2-vorraussetzungen)
    - [3. Software-Installation](#3-software-installation)
    - [4. Einrichten der Instanzen in IP-Symcon](#4-einrichten-der-instanzen-in-ip-symcon)
    - [5. Statusvariablen und Profile](#5-statusvariablen-und-profile)
      - [Profile](#profile)
    - [6. WebFront](#6-webfront)
    - [7. PHP-Befehlsreferenz](#7-php-befehlsreferenz)

### 1. Funktionsumfang

* Zeigt die Variablen der verbundenen SmartMeter Geräte an.


### 2. Vorraussetzungen

- IP-Symcon ab Version 5.5
- Es müssen alle Attribute zur Übertragung aktiviert sein.

### 3. Software-Installation

* Über den Module Store das 'SmartMeter'-Modul installieren.
(ggf. muss vorher eine Freischaltung über den "Testing-Kanal" erfolgen)

### 4. Einrichten der Instanzen in IP-Symcon

 Unter 'Instanz hinzufügen' kann das 'SmartMeter'-Modul mithilfe des Schnellfilters gefunden werden.  

__Konfigurationsseite__:

Name     | Beschreibung
-------- | ------------------
SmartMeter ID         | Die SmartMeter ID dient dazu die die Empfangenen Daten dem richtigen Zähler oder Sensor zuzuordnern. Die ID wird beim Erstellen über den SmartMeterConfigurator automatisch zugewiesen. 
 Variablen automatisch erstellen        | Wenn das Flag "Variablen automatisch erstellen" ist werden die Von dem Sensor übertragen Daten automatisch als Variablen angelegt. Möchte man nicht alle Variablen nutzen kann man diese Funktion abschalten und die überflüssigen Variablen löschen. Bleibt die Funktion aktiv, werden auch neue oder selten gesendete Werte als neue variablen in Symcon angelegt

### 5. Statusvariablen und Profile

Die Variablen werden automatisch angelegt unter SmartMetering/SmartLog[SmartLogID]/[Sensortyp]/[SensorID] angelegt.


#### Profile

Das Modul liefert Profile für diverse Zähler und Sensoren mit. Die SmartMeter-Profile beginnen mit "SM_" und werden automatisch erstellt. Ein Löschen dieser Profile kann zu Problemen führen. Die Profile der Variablen können jedoch überschrieben werden. 

### 6. WebFront

Die System Instanz zeigt die Daten im WebFront an.

### 7. PHP-Befehlsreferenz

Die System Instanz bietet keine Befehlsfunktionen.
