---
title: "Support"
date: 2023-03-18
lastmod: 2024-12-23
showPagination: false
showReadingTime: false
showDate: false
showDateUpdated: true
---

## Remote Desktop

Falls Du Hilfe auf Deinem Computer oder Smartphone benötigst, kannst Du mir mit
der Software [RustDesk](https://rustdesk.com/) die Fernsteuerung deines Gerätes
erlauben.

### Download

Da sich der Download-Link mit jeder Version ändert, kann ich hier leider keinen
direkten Link zur Verfügung stellen.

Gehe dazu auf die
[GitHub Release Seite](https://github.com/rustdesk/rustdesk/releases/latest) des
Projekts und wähle aus der angezeigten Tabelle die passende version für Dein
System, lade diese herunter und installiere sie:

#### Für Windows PC

- Architecture: **x86-64 (64-bit)**
- Windows: **MSI**

#### MacOS Modelle mit Apple Silicon

Modelle mit M1, M2, M3 oder M4 Prozessor, seit ca. 2020/2021.

Architecture: **AArch64 (ARM64)**

#### MacOS Modelle mit Intel Prozessor

Apple Modelle bis ca. 2020

- Architecture: **x86-64 (64-bit)**

### Vermittlungsdienst

Um die Verbindung von meinem zu Deinem Rechner übers Internet herzustellen, wird
ein Vermittlungs-Dienst benötigt.

Zuunterst im Fenster wird ein Hinweis eingeblendet, dass man einen eigenen
Server einrichten sollte.

Dieser wird in den Netzwerk-Einstellungen der Anwendung eingestellt:

#### Einstellungen Öffnen

Klicke dazu auf das Hamburger-Menü in der Titelleiste des Fensters:

{{< figure src="rustdesk-setup-step-1.de.png" title="RustDesk Einstellungen: Schritt 1/8" >}}

#### Die Netzwerk-Einstellungen Öffnen

Klicke dazu auf **Netzwerk** in der linken Spalte:

{{< figure src="rustdesk-setup-step-2.de.png" title="RustDesk Einstellungen: Schritt 2/8" >}}

#### Die Netzwerk-Einstellungen Entsperren

Die Einstellungen sind aus Sicherheitsgründen gesperrt.

{{< figure src="rustdesk-setup-step-3.de.png" title="RustDesk Einstellungen: Schritt 3/8" >}}

Nach dem Klick auf den Balken wirst Du von Deinem Betriebssystem aufgefordert
die Aufhebung der Sperre zu bestätigen.

#### ID/Relay-Server Einstellungen

Klicke auf **ID/Relay-Server**:

{{< figure src="rustdesk-setup-step-4.de.png" title="RustDesk Einstellungen: Schritt 4/8" >}}

Darauf öffnet sich ein neues Dialog-Fenster.

#### Konfiguration Kopieren

Kopiere die folgende lange Zeichnekette in Deine Zwischenablage:

```txt
==Qfi0zZ4UXeTJDM3EDO1UXWEl1RNx2KoFkUnZXR6F3UWRGNux0TExUOBRXQsZDNiojI5V2aiwiIiojIpBXYiwiIiojI5FGblJnIsICaj5iZs92dulWYsFmLzRmciojI0N3boJye
```

Sie enthält alle benötigten Konfigurationsdaten in codierter Form.

Wenn Du mit Deiner Maus über das obige Textfeld fährst, wird ein Link
**Kopieren** erscheinen, den Du anklicken kannst.

#### Konfiguration Einfügen

Zurück in der RustDesk-Konfiguration, klicke auf das Klemmbrett-Symbol im
Dialogfenster.

{{< figure src="rustdesk-setup-step-5.de.png" title="RustDesk Einstellungen: Schritt 5/8" >}}

Dadurch wird das Formular, mittels den codierten Daten aus Deiner Zwischenablage,
automatisch ausgefüllt.

{{< figure src="rustdesk-setup-step-6.de.png" title="RustDesk Einstellungen: Schritt 6/8" >}}

Deine Zwischenablage wird anschliessend geleert.

Du kannst das Dialogfenster danach mit einem Klick auf **OK** schliessen.

#### Einstellungen Schliessen

Auch die **Einstellungen** kännen nun wieder geschlossen werden:

{{< figure src="rustdesk-setup-step-7.de.png" title="RustDesk Einstellungen: Schritt 7/8" >}}

### Verbindung

Zurück im Hauptfenster, sollte zuunterst nun wiederum ein grüner Punkt mit der
Statusmeldung "Bereit" sichtbar sein, aber nun ohne den Hinweis, dass man einen
eigenen Server einrichten sollte.

In der linken Spalte unter "Ihr Desktop" wird Dir eine Nummer angezeigt.

Diese Nummer benötige ich um die Verbindung zu Deinem Rechner aufzubauen.

{{< figure src="rustdesk-setup-step-8.de.png" title="RustDesk Einstellungen: Schritt 8/8" >}}

Bevor die Verbindung hergestellt wird, wirst Du durch ein Dialogfenster gefragt
ob Du die Verbindung erlauben willst.

## Sicherheit und Datenschutz

### Die ID

**Gib Deine ID niemals weiter, ausser an Personen zu denen Du volles Vertrauen hast!**

Du kannst Dir in den **Einstellungen** unter der Rubrik **Sicherheit** jederzeit
eine neue zufällige ID erzeugen.

### Die Software

Die RustDesk Software ist Open-Source, der Code kann
[überprüft](https://github.com/rustdesk/rustdesk) werden.

### Der Relay Server

Der Vermittlungsdienst läuft auf einem von mir gemieteten Server in einem
Schweizer Rechenzentrum.

Sämtliche Kommunikation zwischen unseren beiden Rechnern und dem
Vemittlungsdienst ist verschlüsselt.

Es sind, ausser Deinem Intenet-Provider, meinem Internet-Provider und dem
Schweizer Rechenzentrum, keine weiteren Parteien involviert.
