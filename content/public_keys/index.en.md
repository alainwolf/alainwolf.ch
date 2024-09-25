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

## OpenPGP Fingerprint

[OpenPGP](https://en.wikipedia.org/wiki/Pretty_Good_Privacy) for encryption and
digtal signing of mail messages, files and code commits. My private keys are
stored on [security tokens](https://en.wikipedia.org/wiki/Security_token).

Modern email client software, like
[Thunderbird](https://www.thunderbird.net/en-US/), will retrieve the public key
automatically using my email address. Otherwise:

```bash
gpg --locate-keys alain@alainwolf.ch
```

Or on your Android Smartphone using [OpenKeychain](openkeychain).

### Fingerprint

To verify, if you are using the right key, you can compare the last 16
characters of the [fingerprint](https://en.wikipedia.org/wiki/Public_key_fingerprint):

```bash
$ gpg --list-keys alain@alainwolf.ch | grep '7223 89E4 2736 2DC5'
    Key fingerprint = 5143 E0D3 C00C 9DB4 55BD  FD76 7223 89E4 2736 2DC5
```

The safest way would be to compare the fingerprint with me directly at a
personal meeting.

## SSH Public Key

In case you need to give me access to any of your computer systems trough
[SSH](https://en.wikipedia.org/wiki/Secure_Shell).

I also use my OpenPGP key to authenticate against SSH servers.

You can use GnuPG to retrieve my public key using my OpenPGP fingerprint to you
keyring:

```bash
gpg --locate-keys 0x722389E427362DC5
```

Once you have my public key in your keyring you can export it in the required
format for use with an SSH server:

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
