---
title: "Öffentliche Schlüssel"
date: 2023-12-03
lastmod: 2024-12-25
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

[OpenPGP](https://de.wikipedia.org/wiki/OpenPGP) kann für Verschlüsselung von
E-Mail-Nachrichten und Dateien verwendet werden. Ich verwende es für digitale
Signierung von E-Mail-Nachrichten, Dateien, Dokumente sowie
Quellcode-Änderungen.

Moderne E-Mail-Clients, wie
[Thunderbird](https://www.thunderbird.net/de/), finden den öffentlichen
Schlüssel automatisch
[über meine E-Mail-Adresse](https://keys.openpgp.org/search?q=alain%40alainwolf.ch).

```text
Benutzer ID: Alain Wolf <alain@alainwolf.ch>
Schlüssel ID: 0x722389E427362DC5
Fingerabdruck: 5143 E0D3 C00C 9DB4 55BD FD76 7223 89E4 2736 2DC5
Erstellt: 29. Januar 2022
Läuft ab: 11. Dezember 2025
Algorithmus & Größe: RSA 4096 Bit
```

[Öffentlichen OpenPGP Schlüssel herunterladen (ASCII-Textformat)](https://keys.openpgp.org/vks/v1/by-fingerprint/5143E0D3C00C9DB455BDFD76722389E427362DC5)

Um sicher zu gehen, dass ein Schlüssel tatsächlich zu einer bestimmten Person
gehört, sollte der Fingerabdruck überprüft werden. Im Idealfall geschieht dies
bei einem persönliches Treffen.

Auf Android-Smartphones mit installierter
[OpenKeychain](https://www.openkeychain.org/) App, kann der folgende QR-Code
verwendet werden, um meinen öffentlichen Schlüssel zu Deinem Schlüsselbund
hinzuzufügen:

[OpenPGP QR-Code](openpgp)

## S/MIME Zertifikat

Mit dem folgenden persönlichen Zertifikat kannst Du mir verschlüsselte
[S/MIME](https://en.wikipedia.org/wiki/S/MIME) E-Mail-Nachrichten senden und
Nachrichten oder Dokumente verifizieren, die ich damit digital signiert habe.

Die [WISeID Identity Platform](https://wiseid.com/) hat meinen Namen, meine
E-Mail-Adresse, mein Land und meine Identität in einem Online-Prozess anhand
meines Personalausweises verifiziert. Anschließend werden Zertifikate von
[WISeKeys Zertifizierungsstellen](https://www.wisekey.com) ausgestellt, die von
allen Webbrowsern, E-Mail-Clients und Betriebssystemen als vertrauenswürdig
eingestuft werden.

```Text
Ausgestellt für:
    Name: Alain Wolf
    E-Mail: alain@alainwolf.ch
    Land: CH
Ausgestellt durch:
    Name: WISeKey CertifyID Personal GB CA 3
    Organisation: WiseKey
    Land: CH
Seriennummer:
  17:a9:b7:ec:67:7e:57:9e:8e:ef:94:f9:59:5b:1c:e4:15:93:72:4e
Erstellt: 20. Oktober 2024
Läuft ab: 20. Oktober 2026
Algorithmus & Grösse: RSA 2048 Bit
```

Du kannst das Zertifikat herunterladen und in Deine Mail-App oder Betriebssystem
importieren:

[Zertifikat herunterladen – PEM-Format (.crt)](17a9b7ec677e579e8eef94f9595b1ce41593724e.crt)

## SSH Public Key

Auch zur Authentifizierung gegenüber
[SSH](https://en.wikipedia.org/wiki/Secure_Shell) Servern benutze ich meinen
OpenPGP-Schlüssel.

Wenn Du meinen OpenPGP-Schlüssel bereits überprüft hast und ihm vertraust,
kannst Du somit auch meinem SSH-Schlüssel vertrauen.

Um mir per SSH Zugriff auf Deine Systeme zu gewähren, kannst Du meinen
OpenPGP Key als SSH Key exportieren.

```bash
# Meine Benutzer-ID auf Deinem System (ändere nach Bedarf)
$ _SSH_USER=wolf

# Meinen OpenPGP Key in Deinen Schlüsselbund aufnehmen
$ gpg --search-keys 0x722389E427362DC5

# SSH Key aus dem Schlüsselbund exportieren und installieren
$ gpg --export-ssh-key 0x722389E427362DC5 \
    | sudo -u $_SSH_USER tee -a /home/${_SSH_USER}/.ssh/authorized_keys
```

Auf Ubuntu-Linux-Systemen kannst Du meinen öffentlichen Schlüssel auch aus
[Launchpad](https://launchpad.net/~awolf) oder
[GitHub](https://github.com/alainwolf) importieren:

```bash
# Launchpad
ssh-import-id lp:awolf

# GitHub
ssh-import-id gh:alainwolf
```

Alternativ kannst Du meinen öffentlichen SSH-Schlüssel auch hier herunterladen:

[Öffentlichen SSH-Schlüssel herunterladen (RSA 4096 Bit)](0x722389E427362DC5.pub)

## WireGuard VPN

Für VPN Verbindungen mit [WireGuard](https://www.wireguard.com/), kann der
folgende öffentliche Wireguard Schlüssel verwendet werden:

```text
[Peer]
PublicKey = VM37YPASrxm1x2BuAAx5ep+IiIKdlil2Y3q9jX8tQBM=
AllowedIPs = 0.0.0.0/0, ::/0
PersistentKeepalive = 25
```
