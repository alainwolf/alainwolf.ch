---
title: "Support"
date: 2023-03-18
lastmod: 2025-01-25
showPagination: false
showReadingTime: false
showDate: false
showDateUpdated: true
showTableOfContents: true
---

{{< lead >}}
If you need help on your computer or smartphone, you can allow me to remote
control your device with the [RustDesk](https://rustdesk.com/) remote desktop
software.
{{< /lead >}}

## Download

Since the links change with every new version, I'm unable to provide a direct
download link.

Go to their
[GitHub release page](https://github.com/rustdesk/rustdesk/releases/latest) and
choose the approbriate installation package for your system:

### For Windows PC

- Architecture: **x86-64 (64-bit)**
- Windows: **MSI**

### Apple MacOS

#### Apple Silicon Models

Models with M1, M2, M3 oder M4 CPUs, since approx. 2020/2021.

- Architecture: **AArch64 (ARM64)**

#### Intel Models

Apple models before 2020:

- Architecture: **x86-64 (64-bit)**

## Installation

Depending on your operating system you may need to grant permissions.


## Relay Service

To establish the connection from my computer to yours via the Internet, a relay
service is needed.

At the bottom of the Window a recommendation is shown, to use your own server.

This can be set in the network configuration of the application:

### Open Settings

Click on the hamburger menu in the title-bar of the window:

{{< figure src="rustdesk-setup-step-1.en.png" title="RustDesk Settings: Step 1/8" >}}

### Open Network Settings

Click on **Network** on the left side of the window.

{{< figure src="rustdesk-setup-step-2.en.png" title="RustDesk Settings: Step 2/8" >}}

### Unlock Network Settings

The settings are locked for security reasons.

{{< figure src="rustdesk-setup-step-3.en.png" title="RustDesk Settings: Step 3/8" >}}

After clicking on the bar, your operating system will ask for your confirmation
to unlock it.

### ID/Relay Server Settings

Click on **ID/Relay server**:

{{< figure src="rustdesk-setup-step-4.en.png" title="RustDesk Settings: Step 4/8" >}}

This opens a new dialog window.

### Copy configuration

Copy the following long string to your clipboard:

```txt
==Qfi0zZ4UXeTJDM3EDO1UXWEl1RNx2KoFkUnZXR6F3UWRGNux0TExUOBRXQsZDNiojI5V2aiwiIiojIpBXYiwiIiojI5FGblJnIsICaj5iZs92dulWYsFmLzRmciojI0N3boJye
```

All required configuration data is encoded within.

If you move your mouse over the text field above, a link
**Copy** will appear that you can click on.

### Paste configuration

Back in the RustDesk configuration, click on the clipboard symbol in the
dialog window.

{{< figure src="rustdesk-setup-step-5.en.png" title="RustDesk Settings: Step 5/8" >}}

This will automatically fill out the form using the encoded data from your clipboard.

{{< figure src="rustdesk-setup-step-6.en.png" title="RustDesk Settings: Step 6/8" >}}

Your clipboard will be cleared afterwards.

You can then close the dialog window by clicking on **OK**.

### Close Settings

The **Settings** page can now also be closed again:

{{< figure src="rustdesk-setup-step-7.en.png" title="RustDesk Settings: Step 7/8" >}}

## Connection

Back in the main window, a green dot with the status message "Ready" should be
visible at the bottom, but this time without the note that you should set up
your own server.

In the left column under "Your Desktop" you will see a number.

I need this number to establish the connection to your computer.

{{< figure src="rustdesk-setup-step-8.en.png" title="RustDesk Settings: Step 8/8" >}}

Before the connection is established, you will be asked, if you want to allow it.

## Security and privacy

### The ID

{{< alert "triangle-exclamation" >}}
Never disclose your RustDesk ID number, except to people you fully trust!
{{< /alert >}}

You can generate a new random ID anytime in the **Settings** under the
**Security** section.

### The Software

The RustDesk software is open source, the code can be
[reviewed](https://github.com/rustdesk/rustdesk).

The relay service runs on a server I rented in a Swiss data center.

All communication between the two computers and the relay service
is encrypted.

Besides your internet provider, my internet provider and the
Swiss data center, there are no other parties involved.
