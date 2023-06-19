# Abrechnungsdaten Vermeiter
Diese Instanz spiegelt alle Informationen der Vermieter wieder und wird als Gateway genutzt.

### Inhaltsverzeichnis

- [Abrechnungsdaten Vermeiter](#abrechnungsdaten-vermeiter)
    - [Inhaltsverzeichnis](#inhaltsverzeichnis)
    - [1. Funktionsumfang](#1-funktionsumfang)
    - [2. Voraussetzungen](#2-voraussetzungen)
    - [3. Einrichten der Instanzen in IP-Symcon](#3-einrichten-der-instanzen-in-ip-symcon)

### 1. Funktionsumfang

* Spiegelt alle wichtigen Informationen für die Reports wieder

### 2. Voraussetzungen

* mindestens IPS Version 6.3
* Symcon_Smart_Metering Modul für die Zählervariablen

### 3. Einrichten der Instanzen in IP-Symcon

Sobald der Konfigurator für dieses Modul angelegt wird, wird ebenfalls diese Instanz erstellt.
 

__Konfigurationsseite__:

Name     | Beschreibung
-------- | ------------------
Firma | Firmennamen, welcher auf den Reports zu finden ist,
SMTP Instanz | Die SMTP Instanz wird benötigt, damit Symcon die E-Mails mit den Reports versenden kann, die SMTP Instanz muss zur Zeit einmalig per Hand erstellt werden und hier hinterlegt werden.
E-Mail | In diesem Textfeld muss die E-Mail Adresse des Vermieters hinterlegt werden. An diese E-Mail werden die Gesamt Reports gesendet. Eine Liste mit ; getrennt ist ebenfalls möglich.
E-Mail Betreff| In diesem Textfeld wird der Betreff für die Report E-Mail hinterlegt.
E-Mail Body| In diesem Textfeld wird der Inhalt hinterlegt, welcher in der E-Mail übermittelt wird.
Logo | Hier kann ein Logo hinterlegt werden, welches für den PDF Report verwendet werden soll.
Leere Zähler in Berichten | Wenn aktiviert, werden auch Zähler in den Report gelistet, welche keine Zuordnung besitzen.