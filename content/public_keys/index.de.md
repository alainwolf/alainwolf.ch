---
title: "Öffentliche Schlüssel"
date: 2023-12-03
lastmod: 2025-01-25
showPagination: false
showReadingTime: false
showDate: false
showDateUpdated: true
showTableOfContents: true
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
Schlüssel automatisch über meine E-Mail-Adresse.

{{< alert "triangle-exclamation" >}}
Lass  Dir vom Besitzer des privaten Schlüssels bestätigen, dass Du tatsächlich
seinen öffentlichen Schlüssel hast, indem Ihr den
<strong><font color=secondary-100>Fingerabdruck</font></strong>  miteinander
vergleicht, idealerweise bei einem persönlichen Treffen.{{< /alert >}}

<pre>
Benutzer ID: <strong>Alain Wolf &ltalain@alainwolf.ch&gt</strong>
Schlüssel ID: <strong>7223 89E4 2736 2DC5</strong>
Fingerabdruck:
  <strong><font color=secondary-100>5143 E0D3 C00C 9DB4 55BD
  FD76 7223 89E4 2736 2DC5</font></strong>
Erstellt: <strong>29. Januar 2022</strong>
Läuft ab: <strong>11. Dezember 2025</strong>
Algorithmus & Größe: <strong>RSA 4096 Bit</strong>
</pre>

Alternativ kannst Du den öffentlichen Schlüssel auch hier herunterladen:

{{< button href="/public_keys/0x722389E427362DC5.asc">}}
OpenPGP Schlüssel herunterladen
{{< /button >}}

<br />

Die herutergeladene Datei, im ASCII-geschützten Textformat, muss danach in
deinen Schlüsselbund importiert werden.

{{< details summary="OpenKeychain" >}}
Auf Android-Smartphones mit installierter
[OpenKeychain](https://www.openkeychain.org/) App kannst Du den folgenden
QR-Code verwenden, um meinen öffentlichen Schlüssel zu Deinem Schlüsselbund
hinzuzufügen:
{{< qr level="medium" scale=6 alt="OpenPGP QR code" title="OpenPGP FD76 7223 89E4 2736 2DC5" >}}
OPENPGP4FPR:5143E0D3C00C9DB455BDFD76722389E427362DC5
{{< /qr >}}
{{< /details >}}

## Persönliches Zertifikat

Mit dem folgenden persönlichen X.509 Zertifikat kannst Du mir verschlüsselte
[S/MIME](https://de.wikipedia.org/wiki/S/MIME) E-Mail-Nachrichten senden, sowie
Nachrichten oder Dokumente verifizieren, die ich damit signiert habe.

Die [WISeID Identity Platform](https://wiseid.com/) hat meinen Namen,
E-Mail-Adresse und Nationalität, in einem Online-Prozess anhand
meines Personalausweises verifiziert. Anschliessend wurde das Zertifikat von der
[WISeKey Zertifizierungsstelle](https://www.wisekey.com) ausgestellt. WISeKey
wird von allen Webbrowsern, E-Mail-Clients und Betriebssystemen als
vertrauenswürdig eingestuft.

Wenn Du eine E-Mail-Nachricht öffnest, die ich damit signiert habe, speichert
Deine E-Mail-App das Zertifikat, und es kann danach zur Verschlüsselung von
Nachrichten an mich verwendet werden.

<pre>
Betreff:
  C (Land): <strong>CH</strong>
  CN (allgemeiner Name): <strong>Alain Wolf</strong>
  EMAIL (E-Mail-Adresse): <strong>alain@alainwolf.ch</strong>
Aussteller:
  C (Land): <strong>CH</strong>
  O (Organisation): <strong>WISeKey</strong>
  CN (allgemeiner Name): <strong>WISeKey CertifyID Personal GB CA 3</strong>
Ausgestelltes Zertifikat
  Version: 3
  Seriennummer:
    <strong>3E7A EF83 BB80 1CD1 8239
    7858 C839 11C8 392C 6769</strong>
Ungültig vor: <strong>25.12.2024</strong>
Ungültig nach: <strong>25.12.2026</strong>
</pre>

Alternativ kannst Du das Zertifikat hier im PEM Text-Format herunterladen und in
Deine Mail-App oder Betriebssystem importieren:

{{< button href="/public_keys/c83911c8392c6769-chain.pem">}}
Zertifikat herunterladen
{{< /button >}}

## SSH Public Key

### Aus OpenPGP exportieren

Da ich zur Authentifizierung gegenüber
[SSH](https://en.wikipedia.org/wiki/Secure_Shell) Servern ebenfalls meinen
OpenPGP-Schlüssel verwende, kannst Du auch meinem SSH-Schlüssel vertrauen, wenn
Du meinen OpenPGP-Schlüssel bereits überprüft hast und ihm vertraust.

Um meinen Authentifizierungsunterschlüssel als OpenSSH-Schlüssel aus Deinem
Schlüsselbund zu exportieren:

```bash
$ gpg --export-ssh-key alain@alainwolf.ch
```

### Von GitHub oder Launchpad

Als weitere Alternative auf Ubuntu-Linux-Systemen kannst Du, mit dem Befehl
[ssh-import-id](https://manpages.ubuntu.com/manpages/noble/en/man1/ssh-import-id.1.html)
meinen öffentlichen SSH Schlüssel auch von [GitHub](https://github.com/alainwolf)
oder [Launchpad](https://launchpad.net/~awolf) importieren:

```bash
# Launchpad
$ ssh-import-id lp:awolf

# GitHub
$ ssh-import-id gh:alainwolf
```

### Download von dieser Website

Du kannst meinen öffentlichen SSH-Schlüssel auch hier herunterladen:

{{< button href="/public_keys/id_rsa.pub">}}
SSH Schlüsel herunterladen
{{< /button >}}

## WireGuard VPN

Für VPN Verbindungen mit [WireGuard](https://www.wireguard.com/), kann der
folgende öffentliche Wireguard Schlüssel verwendet werden:

```text
[Peer]
PublicKey = VM37YPASrxm1x2BuAAx5ep+IiIKdlil2Y3q9jX8tQBM=
AllowedIPs = 0.0.0.0/0, ::/0
PersistentKeepalive = 25
```
