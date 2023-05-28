# ValueScaler
Dieses Modul überträgt einen Wert aus einem Wertebereich in einen anderen.

### Inhaltsverzeichnis

- [ValueScaler](#valuescaler)
    - [Inhaltsverzeichnis](#inhaltsverzeichnis)
    - [1. Funktionsumfang](#1-funktionsumfang)
    - [2. Voraussetzungen](#2-voraussetzungen)
    - [3. Software-Installation](#3-software-installation)
    - [4. Einrichten der Instanzen in IP-Symcon](#4-einrichten-der-instanzen-in-ip-symcon)
    - [5. Statusvariablen und Profile](#5-statusvariablen-und-profile)
      - [Statusvariablen](#statusvariablen)
      - [Profile](#profile)
    - [6. WebFront](#6-webfront)
    - [7. PHP-Befehlsreferenz](#7-php-befehlsreferenz)
    - [8. Aktionen](#8-aktionen)

### 1. Funktionsumfang

* Dieses Modul überträgt einen Wert aus einem Wertebereich in einen anderen.

### 2. Voraussetzungen

- IP-Symcon ab Version 6.0

### 3. Software-Installation

* Über den Module Store das 'ValueScaler'-Modul installieren.
* Alternativ über das Module Control folgende URL hinzufügen

### 4. Einrichten der Instanzen in IP-Symcon

 Unter 'Instanz hinzufügen' kann das 'ValueScaler'-Modul mithilfe des Schnellfilters gefunden werden.  
	- Weitere Informationen zum Hinzufügen von Instanzen in der [Dokumentation der Instanzen](https://www.symcon.de/service/dokumentation/konzepte/instanzen/#Instanz_hinzufügen)

__Konfigurationsseite__:

Es müssen keine Einstellungen vorgenommen werden.

### 5. Statusvariablen und Profile

Die Statusvariablen/Kategorien werden automatisch angelegt. Das Löschen einzelner kann zu Fehlfunktionen führen.

#### Statusvariablen

Name   | Typ     | Beschreibung
------ | ------- | ------------
Wert für Skalierung|Integer|Der Wert, welcher in einen anderen Wertebereich übertragen werden soll.
Min Wert|Integer|Der minimale Wert aus dem gegebenen Wertebereich.
Max Wert|Integer|Der maximale Wert aus dem gegebenen Wertebereich.
Skaliert Min|Integer|Der minimale Wert aus dem zukünftigen Wertebereich.
Skaliert Max|Integer|Der maximale Wert aus dem zukünftigen Wertebereich.
Ergebnis|Integer|Das errechnete Ergebnis.
Aktion|String|Mit einem Klick auf diese Variable wird die Berechnung ausgeführt.

#### Profile

Name   | Typ
------ | -------
ValueScaler.Aktion | String

### 6. WebFront

Die Funktionalität, die das Modul im WebFront bietet.
Über das Webfront kann eine Berechnung durchgeführt werden, dazu müssen die Variablen mit den gegebenen Werten gefüllt werden, danach kann die Berechnung mit einem Klick auf die Variable "Aktion" -> Skalieren ausgeführt werden.

### 7. PHP-Befehlsreferenz

`integer VS_scale(integer $InstanzID,$value, $min, $max, $scaledMin, $scaledMax);`
Diese Funktion führt eine Berechnung durch und gibt das Ergebnis aus.

Beispiel:
`VS_scale(12345,50,0,100,0,255);`
Das Ergebnis wäre 128.  

### 8. Aktionen

Mit der Aktion "Skaliere Variable" kann die Funktion des Moduls in jedem Ereignis oder Ablaufplan genutzt werden, sofern die Quellvariable, auf die das Ereignis gesetzt wird eine Integer Variable ist.
Für die Parametererklärung siehe die Tabelle der Statusvariablen.