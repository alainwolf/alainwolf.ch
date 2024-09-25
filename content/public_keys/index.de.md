---
title: "Öffentliche Schlüssel"
date: 2023-12-03
lastmod: 2024-09-25
showPagination: false
showReadingTime: false
showDate: false
showDateUpdated: true
---

{{< lead >}}
Meine
[öffentlichen Schlüssel](https://de.wikipedia.org/wiki/Asymmetrisches_Kryptosystem)
für Verschlüsselung, digitale Unterschriften und Authentifizierung.
{{< /lead >}}

## OpenPGP

[OpenPGP](https://de.wikipedia.org/wiki/Pretty_Good_Privacy) dient der
Verschlüsselung und digitaler Signierung von E-Mail-Nachrichten, Dateien und
Quellcodes.

Moderne E-Mail-Client-Software, wie
[Thunderbird](https://www.thunderbird.net/de/), findet den öffentlichen
Schlüssel automatisch
[über meine E-Mail-Adresse](https://keys.openpgp.org/search?q=alain%40alainwolf.ch).
Ansonsten:

```bash
gpg --locate-keys alain@alainwolf.ch
```

Oder über Dein Android Smartphone mit [OpenKeychain](openkeychain).

### Fingerprint

Um zu überprüfen, ob Du auch den richtigen Schlüssel verwendest, kannst Du ihn
mit den letzen 16 Zeichen des unten angezeigten
[Fingerprint](https://de.wikipedia.org/wiki/Hashfunktion) vergleichen:

```bash
$ gpg --list-keys alain@alainwolf.ch | grep '7223 89E4 2736 2DC5'
    Key fingerprint = 5143 E0D3 C00C 9DB4 55BD  FD76 7223 89E4 2736 2DC5
```

Der sicherste Weg wäre, den Fingerprint mit mir direkt bei einem persönlichen
Treffen zu vergleichen.

## SSH Public Key

This allows you to give me access to one of your computer systems via
[SSH](https://en.wikipedia.org/wiki/Secure_Shell).

Zur Authentifizierung gegenüber SSH Servern benutze ich ebenfalls meinen
OpenPGP-Schlüssel.

Du meinen öffentlichen OpenPGP-Schlüssel in Schlüsselbund zu speichern und ihn
danach, im für SSH Server erforderlichen Format, exportieren:

```bash
# Meine Benutzer-ID auf Deinem System (ändere nach Bedarf)
$ _SSH_USER=wolf

# Mein OpenPGP Key suchen und installieren
$ gpg --search-keys 0x722389E427362DC5

# SSH Key exportieren und installieren
$ gpg --export-ssh-key 0x722389E427362DC5 \
    | sudo -u $_SSH_USER tee -a /home/${_SSH_USER}/.ssh/authorized_keys
```

## WireGuard VPN

Für VPN Verbindungen mit [WireGuard](https://www.wireguard.com/), kann folgender
öffentlicher Schlüssel meines persönlichen Computers verwendet werden:

```text
VM37YPASrxm1x2BuAAx5ep+IiIKdlil2Y3q9jX8tQBM=
```
