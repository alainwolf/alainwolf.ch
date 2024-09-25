---
title: "Support"
date: 2023-03-18
lastmod: 2024-09-25
showPagination: false
showReadingTime: false
showDate: false
showDateUpdated: true
---

## Remote Desktop

Falls Du Hilfe auf Deinem Computer oder Smartphone benötigst, kannst Du mir mit
der Software [RustDesk](https://rustdesk.com/) die Fernsteuerung deines Gerätes
erlauben.

Lade dazu das zu deinem Gerät passende Installations-Paket von der
[RustDesk Homepage](https://rustdesk.com/) herunter, installiere und starte die
Anwendung.

### Einstellungen

Um die Verbindung übers Internet herzustellen, wird ein Vermittlungs-Dienst
benötigt.

Der Vermittlungsdienst muss in den Netzwerk-Einstellungen der
Anwndung eingestellt werden:

{{< figure src="rustdesk_network_settings.png" title="RustDesk Network Settings" >}}

#### ID server

```txt
rds.alainwolf.ch
```

Die Felder "**Relay Server**" und "**API Server**" bitte leer lassen.

#### Key

```txt
46lAtA9LDOLn4dVSqzEvgRAh+lMGYDYu581702Syu8g=
```

Du kannst die folgenden Zeichnekette kopieren und in den Netzwerk-Einstellungen
einfügen:

```txt
==Qfi0zZ4UXeTJDM3EDO1UXWEl1RNx2KoFkUnZXR6F3UWRGNux0TExUOBRXQsZDNiojI5V2aiwiIiojIpBXYiwiIiojI5FGblJnIsICaj5iZs92dulWYsFmLzRmciojI0N3boJye
```

### Verbindung

In der Anwendung sieht du eine aus 3x3 Zahlen bestehende Nummer. Unter dieser
Nummer kann ich die Verbindung zu Deinem Gerät herstellen.

{{< figure src="rustdesk_desktop_id.png" title="RustDesk Desktop ID" >}}

Bevor die Verbindung hergestellt wird, wirst du in einem neuen Fenster gefragt
ob Du diese Verbindung erlauben willst.

## Sicherheit und Datenschutz

Die Software ist Open-Source, der Code kann überpfüft werden.

Der Vermittlungsdienst läuft auf einem von mir gemieteten Server in einem
Schweizer Rechenzentrum.

Sämtliche Kommunikation zwischen den beiden Rechnern und dem Vemittlungsdienst
ist verschlüsselt.

Es sind, ausser Deinem Intenet-Provider, meinem Internet-Provider und dem
Schweizer Rechenzentrum, keine weiteren Parteien involviert.
