---
title: "Public Keys"
date: 2023-12-03
lastmod: 2024-05-14
showPagination: false
showReadingTime: false
showDate: false
showDateUpdated: true
---

Following are my various
[public keys](https://en.wikipedia.org/wiki/Public-key_cryptography) for
encryption, signing and authentication.

## OpenPGP Fingerprint

[OpenPGP](https://en.wikipedia.org/wiki/Pretty_Good_Privacy) is my preferred
method for encryption and digtal signing of mail messages, files and code
commits. My private keys are stored on
[security tokens](https://en.wikipedia.org/wiki/Security_token).

Modern email client software, like
[Thunderbird](https://www.thunderbird.net/en-US/), will retrieve the public key
automatically using my email address. To verify, that you are using the right
key, you can compare it with the
[fingerprint](https://en.wikipedia.org/wiki/Public_key_fingerprint) displayed
below:

    5143 E0D3 C00C 9DB4 55BD
    FD76 7223 89E4 2736 2DC5

The safest way would be to get it from me in a personal meeting.

## SSH Public Key

In case you need to give me access to any of your computer systems trough
[SSH](https://en.wikipedia.org/wiki/Secure_Shell). I'm using an authentication
subkey of my OpenPGP key stored on a security token, as SSH key to autheticate
myself against a server.

You can use GnuPG to retrieve the public key using my OpenPGP fingerprint to you
keyring:

    gpg --locate-keys 0x722389E427362DC5

Once you have my public key in your keyring you can export it in the required
format for use with an SSH server:

    _SSH_USER=wolf
    gpg --export-ssh-key 0x722389E427362DC5 \
        >> /home/${_SSH_USER}/.ssh/authorized_keys
