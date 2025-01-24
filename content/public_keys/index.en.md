---
title: "Public Keys"
date: 2023-12-03
lastmod: 2025-01-23
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

```text
User ID: Alain Wolf <alain@alainwolf.ch>
Key ID: 0x722389E427362DC5
Fingerprint: 5143 E0D3 C00C 9DB4 55BD  FD76 7223 89E4 2736 2DC5
Created: January 29, 2022
Expires: December 11, 2025
Algorithm & Size: RSA 4096 bits
```

Download my OpenPGP public key:

- [ASCII text format (.asc)](/public_keys/0x722389E427362DC5.asc)
- [Binary format (.gpg)](/public_keys/0x722389E427362DC5.gpg)

To ensure that a key actually belongs to a specific person, the fingerprint
should be checked. Ideally, this happens during a personal meeting.

{{< details summary="OpenKeychain" >}}
On Android smartphones with the [OpenKeychain](https://www.openkeychain.org/)
app installed you can use the following QR-Code to add my public key into your
keyring:
{{< qr level="medium" scale=6 alt="OpenPGP QR code" title="OpenPGP FD76 7223 89E4 2736 2DC5" >}}
OPENPGP4FPR:5143E0D3C00C9DB455BDFD76722389E427362DC5
{{< /qr >}}
{{< /details >}}

## S/MIME

The follwoing personal certificate can be used to send me encrypted
[S/MIME](https://en.wikipedia.org/wiki/S/MIME) mail messages and verify messages
or documents I have digitally signed with.

The [WISeID Identity Platform](https://wiseid.com/) has verified my name,
email-address, country and identity in an online process using my national ID
card. Certificates are then issued by
[WISeKey’s Certification Authorities](https://www.wisekey.com), which are
trusted by all web-browsers, mail clients and operating systems.

```text
Subject Name:
  C (Country): CH
  CN (Common Name): Alain Wolf
  EMAIL (Email Address): alain@alainwolf.ch
Issuer Name:
  C (Country): CH
  O (Organization): WISeKey
  CN (Common Name): WISeKey CertifyID Personal GB CA 3
Issued Certificate
  Version: 3
  Serial Number:
    3E 7A EF 83 BB 80 1C D1 82 39 78 58 C8 39 11 C8 39 2C 67 69
  Not Valid Before: 2024-12-25
  Not Valid After: 2026-12-25
```

Download my certificate:

- [Certificate only PEM text format (.crt)](/public_keys/c83911c8392c6769.crt)
- [Certificate only DER binary format (.der)](/public_keys/c83911c8392c6769.der)
- [Certificate chain PEM text format (.pem)](/public_keys/c83911c8392c6769-chain.pem)
- [Certificate chain PKCS#7 format (.p7b)](/public_keys/c83911c8392c6769-chain.p7b)

You can then import it into your mail app or operating system.

## SSH Public Key

I use my OpenPGP key to authenticate against
[SSH](https://en.wikipedia.org/wiki/Secure_Shell) servers too.

If you already have verified and trust my OpenPGP key, you can also safely trust
my SSH key.

To allow me to access your systems trough SSH, you can export my OpenPGP key as
SSH key:

```bash
# My user ID on your system (change as needed)
$ _SSH_USER=wolf

# Search and add my public key to your keyring
$ gpg --search-keys 0x722389E427362DC5

# Export my SSH public key from your keyring and install it
$ gpg --export-ssh-key 0x722389E427362DC5 \
    | sudo -u $_SSH_USER tee -a \
        /home/${_SSH_USER}/.ssh/authorized_keys
```

On Ubuntu Linux systems you can get my public key from either
[Launchpad](https://launchpad.net/~awolf) or
[GitHub](https://github.com/alainwolf):

```bash
# Launchpad
ssh-import-id lp:awolf

# GitHub
ssh-import-id gh:alainwolf
```

Altenatively you can download my SSH public key:

- [OpenSSH RSA public key format (id_rsa.pub)](/public_keys/id_rsa.pub)

## WireGuard VPN

For VPN connections with [WireGuard](https://www.wireguard.com/), you can use
this WireGuard public key of my personal computer:

```text
[Peer]
PublicKey = VM37YPASrxm1x2BuAAx5ep+IiIKdlil2Y3q9jX8tQBM=
AllowedIPs = 0.0.0.0/0, ::/0
PersistentKeepalive = 25
```
