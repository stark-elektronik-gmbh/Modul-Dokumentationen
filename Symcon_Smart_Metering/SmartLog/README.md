# SmartLog
Der SmartLog spiegelt ein physisches Smart Energy Log Gerät wieder. Es kann eine beliebeige Anzahl von Geräten verwedent werden (in der Praxis abhängig von der Leistung der Symcon-Instanz und der Aktualisierungsrate der Messwerte).
Der SmartLog stellt einen MQTT Client dar und verbindet sich mit dem Symcon-MQTT-Server.

### Inhaltsverzeichnis

1. [Funktionsumfang](#1-funktionsumfang)
2. [Voraussetzungen](#2-vorraussetzungen)
3. [Software-Installation](#3-software-installation)
4. [Einrichten der Instanzen in IP-Symcon](#4-einrichten-der-instanzen-in-ip-symcon)
5. [Statusvariablen und Profile](#5-statusvariablen-und-profile)
6. [WebFront](#6-webfront)
7. [PHP-Befehlsreferenz](#7-php-befehlsreferenz)

### 1. Funktionsumfang

Der SmartLog spiegelt ein Physisches Smart Energy Log Gerät wieder. Es kann eine beliebeige Anzahl von Geräten verwedent werden (in der Praxis abhängig von der Leistung der Symcon-Instanz und der Aktualisierungsrate der Messwerte). Der SmartLog Stellt einen MQTT Client da und verbindet sich mit dem Symcon-MQTT-Server.

### 2. Vorraussetzungen

- IP-Symcon ab Version 5.5

### 3. Software-Installation

* Über den Module Store das 'SmartLog'-Modul installieren.

### 4. Einrichten der Instanzen in IP-Symcon

 Unter 'Instanz hinzufügen' kann das 'SmartLog'-Modul mithilfe des Schnellfilters gefunden werden.  

__Konfigurationsseite__:

Name     | Beschreibung
-------- | ------------------
SmartLog ID         |Die SmartLog ID dient dazu, die Empfangen Daten dem richtigen SmartLog Gerät zuzuordnern
      

### 5. Statusvariablen und Profile

Die Statusvariablen/Kategorien werden automatisch angelegt. Das Löschen einzelner kann zu Fehlfunktionen führen.

#### Statusvariablen

Name   | Typ     | Beschreibung
------ | ------- | ------------
Last Message Time       |   String      | Zeitpunkt der letzten Nachricht


### 6. WebFront

Der SmartLog zeitgt im Webfrot den Zeitpunkt der letzten Nachricht an. 

### 7. PHP-Befehlsreferenz

Die SmartMeter instanz bietet keine Befehlsfunktionen.
