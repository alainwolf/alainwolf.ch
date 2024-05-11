---
title: "Public Keys"
date: 2023-12-03
lastmod: 2024-05-11
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

## S/MIME Certificate

As a fallback, in case your are not able to use OpenPGP.

I have a personal x509 certificate, issued by [WISeID](https://wiseid.com/).
WiseID did a very basic online authentication check.

The certificate can be used to encrypt mails by
[S/MIME](https://en.wikipedia.org/wiki/S/MIME) or for authentication against web
services.

{{< alert >}}
Due to technical issues, the private key related to this certificate is
currently not stored on secure hardware.
{{< /alert >}}

To use it, one has to [download it](/public_keys/alain-wolf-chain.p7b) manually
and import it in the software to use it.

The SHA-265 fingerprint of this certificate is:

    7573 856F 132F 2AFF 6FDF 3580 DFC3 D42C
    B03A 7237 84C9 9482 4770 F518 B9C7 2DFE
