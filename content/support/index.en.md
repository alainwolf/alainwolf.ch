---
title: "Support"
date: 2023-03-18
lastmod: 2023-07-07
showPagination: false
showReadingTime: false
showDate: false
showDateUpdated: true
---

## Remote Desktop

If you need help on your computer or smartphone, you can allow me
to control your device with the software [RustDesk](https://rustdesk.com/).

To do this, download the appropriate installation package for your device from the
[RustDesk Homepage](https://rustdesk.com/), install and start the
Application.

### Settings

To establish the connection via the Internet, a relay service is
needed.

The relay service must be specified in the network settings of the
application:

{{< figure src="rustdesk_network_settings.png" title="RustDesk Network Settings" >}}

#### ID server

```txt
rds.alainwolf.ch
```

Please leave the fields "**Relay Server**" and "**API Server**" empty.

#### Key

```txt
46lAtA9LDOLn4dVSqzEvgRAh+lMGYDYu581702Syu8g=
```

You can copy the following string and insert it in the network settings window:

```txt
==Qfi0zZ4UXeTJDM3EDO1UXWEl1RNx2KoFkUnZXR6F3UWRGNux0TExUOBRXQsZDNiojI5V2aiwiIiojIpBXYiwiIiojI5FGblJnIsICaj5iZs92dulWYsFmLzRmciojI0N3boJye
```

### Connection

In the application you will see a number consisting of 3x3 digits. I need to
know this number to connect to your device.

{{< figure src="rustdesk_desktop_id.png" height="212" width="241" alt="RustDesk Desktop ID" >}}

Before the connection is established, you will be asked in a new window
if you want to allow this connection.

## Security and privacy

The software is open source, the code can be audited.

The relay service runs on a server I rented in a Swiss data center.

All communication between the two computers and the relay service
is encrypted.

Besides your internet provider, my internet provider and the
Swiss data center, there are no other parties involved.
