---
title: "Öffentliche Schlüssel"
date: 2023-12-03
lastmod: 2024-05-14
showPagination: false
showReadingTime: false
showDate: false
showDateUpdated: true
---

Meine
[öffentlichen Schlüssel](https://de.wikipedia.org/wiki/Asymmetrisches_Kryptosystem)
für Verschlüsselung, digitale Unterschriften und Authentifizierung.

## OpenPGP Fingerprint

[OpenPGP](https://de.wikipedia.org/wiki/Pretty_Good_Privacy) ist mein
bevorzugter Methode zur Verschlüsselung und digitaler Signierung von
E-Mail-Nachrichten, Dateien und Quellcodes. Die privaten Schlüssel sind auf
[Security-Tokens](https://de.wikipedia.org/wiki/Security-Token) gespeichert.

Moderne E-Mail-Client-Software, wie
[Thunderbird](https://www.thunderbird.net/de/), findet den öffentlichen
Schlüssel automatisch über meine E-Mail-Adresse.

Um zu überprüfen, dass Du den richtigen Schlüssel verwendest, kannst Du ihn mit
dem unten angezeigten [Fingerprint](https://de.wikipedia.org/wiki/Hashfunktion)
vergleichen:

    5143 E0D3 C00C 9DB4 55BD
    FD76 7223 89E4 2736 2DC5

Der sicherste Weg wäre, den Fingerprint mit mir an einem persönlichen Treffen zu
vergleichen.

## SSH Public Key

Falls Du mir Zugang zu einem Deiner Computersysteme über
[SSH](https://de.wikipedia.org/wiki/Secure_Shell) geben musst.

Zur Authentifizierung gegenüber einen SSH Server benutze ich ebenfalls meinen,
auf einen Security-Token gespeicherten, OpenPGP-Schlüssel.

Du kannst GnuPG verwenden, um den öffentlichen Schlüssel über meinen
OpenPGP-Fingerprint abzurufen und in Deinen PGP-Schlüsselbund zu speichern:

    gpg --locate-keys 0x722389E427362DC5

Sobald Du meinen öffentlichen Schlüssel in Deinem Schlüsselbund hast,
kannst Du ihn, im für SSH Server erforderlichen Format, exportieren:

    _SSH_USER=wolf
    gpg --export-ssh-key 0x722389E427362DC5 \
        >> /home/${_SSH_USER}/.ssh/authorized_keys
