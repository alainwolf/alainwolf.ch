---
title: "Public Keys"
date: 2023-12-03
lastmod: 2025-01-25
showPagination: false
showReadingTime: false
showDate: false
showDateUpdated: true
showTableOfContents: true
---

{{< lead >}}
My [public keys](https://en.wikipedia.org/wiki/Public-key_cryptography) for
encryption, signing and authentication.
{{< /lead >}}

## OpenPGP

[OpenPGP](https://en.wikipedia.org/wiki/Pretty_Good_Privacy#OpenPGP) can be used
for encryption of mail messages and files. I'm using it to digitally sign email
messages, files and code commits.

Modern email client software, like
[Thunderbird](https://www.thunderbird.net/en-US/), will retrieve the public key
automatically, [based on my email address](https://keys.openpgp.org/search?q=alain%40alainwolf.ch).

{{< alert "triangle-exclamation" >}}
Have the owner of the private key confirm that you actually have his public key
by comparing your <strong><font color=secondary-100>fingerprints</font></strong>,
ideally during a face-to-face meeting.
{{< /alert >}}

<pre>
User ID: <strong>Alain Wolf &ltalain@alainwolf.ch&gt</strong>
Key ID: <strong>7223 89E4 2736 2DC5</strong>
Fingerprint:
  <strong><font color=secondary-100>5143 E0D3 C00C 9DB4 55BD
  FD76 7223 89E4 2736 2DC5</font></strong>
Created: <strong>January 29, 2022</strong>
Expires: <strong>December 11, 2025</strong>
Algorithm & Size: <strong>RSA 4096 bits</strong>
</pre>

Alternatively, you can download the public key here:

{{< button href="/public_keys/0x722389E427362DC5.asc">}}
Download OpenPGP Key
{{< /button >}}

<br />

The downloaded file, in ASCII armored text format, must then be imported into
your keyring.


{{< details summary="OpenKeychain" >}}
On Android smartphones with the [OpenKeychain](https://www.openkeychain.org/)
app installed you can use the following QR-Code to add my public key into your
keyring:
{{< qr level="medium" scale=6 alt="OpenPGP QR code" title="OpenPGP FD76 7223 89E4 2736 2DC5" >}}
OPENPGP4FPR:5143E0D3C00C9DB455BDFD76722389E427362DC5
{{< /qr >}}
{{< /details >}}

## Personal Certificate

The follwoing personal X.509 certificate can be used to send me encrypted
[S/MIME](https://en.wikipedia.org/wiki/S/MIME) mail messages and verify messages
or documents I have digitally signed with.

The [WISeID Identity Platform](https://wiseid.com/) has verified my name,
email-address and nationality in an online process using my ID
card. The certificates has been issued subsequently by the
[WISeKey Certification Authority](https://www.wisekey.com), which is
trusted by all web-browsers, mail clients and operating systems.

When you open an email message that I signed with it,
your email app saves the certificate and can then be used to encrypt
messages to me.

<pre>
Subject:
  C (Country): <strong>CH</strong>
  CN (Common Name): <strong>Alain Wolf</strong>
  EMAIL (Email Address): <strong>alain@alainwolf.ch</strong>
Issuer:
  C (Country): <strong>CH</strong>
  O (Organization): <strong>WISeKey</strong>
  CN (Common Name): <strong>WISeKey CertifyID Personal GB CA 3</strong>
Issued Certificate
  Version: 3
  Serial Number:
    <strong>3E7A EF83 BB80 1CD1 8239
    7858 C839 11C8 392C 6769</strong>
  Not Valid Before: <strong>December 25, 2024</strong>
  Not Valid After: <strong>December 25, 2026</strong>
</pre>

Alternatively, you can download the certificate here in PEM text format and
import it into your mail app or operating system:

{{< button href="/public_keys/c83911c8392c6769-chain.pem">}}
Download Certificate
{{< /button >}}

You can then import it into your mail app or operating system.

## SSH Public Key

### Export from OpenPGP

Since I use my OpenPGP key to authenticate against
[SSH](https://en.wikipedia.org/wiki/Secure_Shell) servers too, you can safely
trust my SSH key, if you already have verified and trust my OpenPGP public key.

To export my authentication subkey as OpenSSH key from your keyring:

```bash
$ gpg --export-ssh-key alain@alainwolf
```

### From GitHub or Launchpad

As another alternative on Ubuntu Linux systems you can get my public key from
either [GitHub](https://github.com/alainwolf) or
[Launchpad](https://launchpad.net/~awolf) using the
[ssh-import-id](https://manpages.ubuntu.com/manpages/noble/en/man1/ssh-import-id.1.html)
command:

```bash
# GitHub
$ ssh-import-id gh:alainwolf

# Launchpad
$ ssh-import-id lp:awolf
```

### Download from this Website

Altenatively you can download my SSH public key from here:

{{< button href="/public_keys/id_rsa.pub">}}
Download SSH Public Key
{{< /button >}}

## WireGuard VPN

For VPN connections with [WireGuard](https://www.wireguard.com/), you can use
this WireGuard public key of my personal computer:

```text
[Peer]
PublicKey = VM37YPASrxm1x2BuAAx5ep+IiIKdlil2Y3q9jX8tQBM=
AllowedIPs = 0.0.0.0/0, ::/0
PersistentKeepalive = 25
```
