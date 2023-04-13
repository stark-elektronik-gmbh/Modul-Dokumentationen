# Konfigurator
Diese Instanz erstellt die einzelnen Geräteinstanzen mit den erforderlichen Einstellungen.

### Inhaltsverzeichnis

- [Konfigurator](#konfigurator)
    - [Inhaltsverzeichnis](#inhaltsverzeichnis)
    - [1. Funktionsumfang](#1-funktionsumfang)
    - [2. Voraussetzungen](#2-voraussetzungen)
    - [3. Einrichten der Instanzen in IP-Symcon](#3-einrichten-der-instanzen-in-ip-symcon)

### 1. Funktionsumfang

* Erstellt die erforderlichen Instanzen anhand einer CSV Datei, welche die Wohnungen mit den dazugehörigen Zählernummern enthält.

### 2. Voraussetzungen

* mindestens IPS Version 6.3
* Symcon_Smart_Metering Modul für die Zählervariablen
* CSV Datei als Vorlage in nachstehendem Format:
  * Wohnungs Name;Stromzählernummer;Kaltwasserzählernummer;Warmwasserzählernummer;Wärmemengenzählernummer;Webfront Passwort;Mieter E-Mail Adresse

### 3. Einrichten der Instanzen in IP-Symcon

 Unter 'Instanz hinzufügen' kann das 'Konfigurator'-Modul mithilfe des Schnellfilters gefunden werden.  
	- Weitere Informationen zum Hinzufügen von Instanzen in der [Dokumentation der Instanzen](https://www.symcon.de/service/dokumentation/konzepte/instanzen/#Instanz_hinzufügen)

__Konfigurationsseite__:

Name     | Beschreibung
-------- | ------------------
CSV Datei für Wohnungen | Über diesen Dateiupload muss die CSV Datei hochgeladen werden, welche die Wohnungen inkl. Zählernummern enthält.
SMTP Instanz | Die SMTP Instanz wird benötigt, damit Symcon die E-Mails mit den Reports versenden kann, die SMTP Instanz muss zur Zeit einmalig per Hand erstellt werden und hier hinterlegt werden.
Vermeiter E-Mail | In diesem Textfeld muss die E-Mail Adresse des Vermeiters hinterlegt werden, diese Adresse wird benötigt, damit der Versand per E-Mail erfolgen kann.
Konfigurator| Über diese Liste können die einzelnen Instanz erstellt werden, über welche die Reports für die Wohnungen bzw. für die gesamte Wohneinheit erstellt und versendet werden können.