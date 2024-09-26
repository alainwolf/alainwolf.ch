---
title: "Public Keys"
date: 2023-12-03
lastmod: 2024-09-25
showPagination: false
showReadingTime: false
showDate: false
showDateUpdated: true
---

{{< lead >}}
My [public keys](https://en.wikipedia.org/wiki/Public-key_cryptography) for
encryption, signing and authentication.
{{< /lead >}}

## OpenPGP

[OpenPGP](https://en.wikipedia.org/wiki/Pretty_Good_Privacy) can be used for
encryption and digtal signing of mail messages, files and code commits.

Modern email client software, like
[Thunderbird](https://www.thunderbird.net/en-US/), will retrieve the public key
automatically, based on my email address. Otherwise:

```bash
gpg --locate-keys alain@alainwolf.ch
```

Or on your Android Smartphone using [OpenKeychain](openkeychain).

### Verification

To verify that you are using the right key, you can compare the last 16
characters of the [fingerprint](https://en.wikipedia.org/wiki/Public_key_fingerprint):

```bash
gpg --list-keys alain@alainwolf.ch | grep '7223 89E4 2736 2DC5'
```

```txt
Key fingerprint = 5143 E0D3 C00C 9DB4 55BD  FD76 7223 89E4 2736 2DC5
```

The safest way would be to compare the fingerprint in a personal meeting.

## SSH Public Key

I use my OpenPGP key to authenticate against
[SSH](https://en.wikipedia.org/wiki/Secure_Shell) servers too.

To allow me to access your systems trough SSH, you can export my OpenPGP key as
SSH key:

```bash
# My user ID on your system (change as needed)
$ _SSH_USER=wolf

# Search and install my OpenPGP key
$ gpg --search-keys 0x722389E427362DC5

# Export and install my SSH key
$ gpg --export-ssh-key 0x722389E427362DC5 \
    | sudo -u $_SSH_USER tee -a /home/${_SSH_USER}/.ssh/authorized_keys
```

## WireGuard VPN

For VPN connections with [WireGuard](https://www.wireguard.com/), you can use
this WireGuard public key of my personal computer:

```text
VM37YPASrxm1x2BuAAx5ep+IiIKdlil2Y3q9jX8tQBM=
```
