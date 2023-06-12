# SmartLogHTTPS
Der SmartLogHTTPS spiegelt ein physisches Smart Energy Log Gerät wieder. Es kann eine beliebige Anzahl von Geräten verwendet werden (in der Praxis abhängig von der Leistung der Symcon-Instanz und der Aktualisierungsrate der Messwerte).
Der SmartLogHTTPS stellt einen WebHook bereit, welcher über den SmartMeter Logger aufgerufen werden kann, um so die Daten in IP-Symcon zu übertragen.

### Inhaltsverzeichnis

- [SmartLogHTTPS](#smartloghttps)
    - [Inhaltsverzeichnis](#inhaltsverzeichnis)
    - [1. Funktionsumfang](#1-funktionsumfang)
    - [2. Vorraussetzungen](#2-vorraussetzungen)
    - [3. Software-Installation](#3-software-installation)
    - [4. Einrichten der Instanzen in IP-Symcon](#4-einrichten-der-instanzen-in-ip-symcon)
    - [5. Konfiguration des SmartMeterLoggers](#5-konfiguration-des-smartmeterloggers)
    - [6. Statusvariablen und Profile](#6-statusvariablen-und-profile)
      - [Statusvariablen](#statusvariablen)
    - [7. WebFront](#7-webfront)
    - [8. PHP-Befehlsreferenz](#8-php-befehlsreferenz)

### 1. Funktionsumfang

Der SmartLogHTTPS spiegelt ein physisches Smart Energy Log Gerät wieder. Es kann eine beliebige Anzahl von Geräten verwendet werden (in der Praxis abhängig von der Leistung der Symcon-Instanz und der Aktualisierungsrate der Messwerte).
Der SmartLogHTTPS stellt einen WebHook bereit, welcher über den SmartMeter Logger aufgerufen werden kann, um so die Daten in IP-Symcon zu übertragen.

### 2. Vorraussetzungen

- IP-Symcon ab Version 5.5
- Einstellungen im SmartMeterLogger

### 3. Software-Installation

* Über den Module Store das 'SmartLogHTTPS'-Modul installieren.

### 4. Einrichten der Instanzen in IP-Symcon

 Unter 'Instanz hinzufügen' kann das 'SmartLogHTTPS'-Modul mithilfe des Schnellfilters gefunden werden.  

__Konfigurationsseite__:

Name     | Beschreibung
-------- | ------------------
SmartLog ID         |Die SmartLog ID dient dazu, die Empfangen Daten dem richtigen SmartLog Gerät zuzuordnen
WebHook Username         |Der Username schützt den WebHook in Kombination mit einem Passwort
WebHook Passwort         |Der Username schützt den WebHook in Kombination mit einem Passwort

Name     | Beschreibung
-------- | ------------------
Report Adresse | Die Report Adresse ist die Connect URL, welche im SmartMeter Logger unter "Report address" eingetragen werden muss.
Report Verzeichnis | Das Report Verzeichnis ist der Pfad, welcher im SmartMeter Logger unter "Report directory" eingetragen werden muss. Der Pfad stellt in IP-Symcon einen WebHook dar.

### 5. Konfiguration des SmartMeterLoggers
  - Unter Report eine neue Report Instanz anlegen.
  - Report Mode: TLS
  - Report Format: JSON
  - Report address: Die URL aus der Konfigurationsform (Report Adresse)
  - Report directory: Der PFad aus der Konfigurationsform (Report Verzeichnis)
- Installation Zertifikat auf dem SmartMeterLogger
  - Download Zertifikat: https://curl.se/docs/caextract.html (https://curl.se/ca/cacert.pem)
  - Die Datei cacert.pem in ReportX.pem umbenennen, das X steht für die Report Nummer des SmartMeter Loggers.
  - Die Datei ReportX.pem in das Verzeichnis /app auf dem SmaterMeter Logger laden.
  - Den SmartMeterLogger neustarten

### 6. Statusvariablen und Profile

Die Statusvariablen/Kategorien werden automatisch angelegt. Das Löschen einzelner kann zu Fehlfunktionen führen.

#### Statusvariablen

Name   | Typ     | Beschreibung
------ | ------- | ------------
Last Message Time       |   String      | Zeitpunkt der letzten Nachricht


### 7. WebFront

Der SmartLogHTTPS zeigt im Webfrot den Zeitpunkt der letzten Nachricht an. 

### 8. PHP-Befehlsreferenz

Die SmartMeter instanz bietet keine Befehlsfunktionen.
