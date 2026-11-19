---
uid: Connector_help_XICHTEE_LMPSH-IP
---

# XICHTEE LMPSH-IP

## About

The XICHTEE LMPSH-IP is a PoE-powered RGB studio signal lamp used to show studio states such as on air, recording, rehearsal or call at studio entrances, voice-over booths, production control rooms and OB facilities. A single Ethernet cable supplies both power and IP control, and the illuminated sign can be used as one full-width section or as two independently controlled sections.

This connector integrates the LMPSH-IP into DataMiner over HTTP, so that you can monitor the state of the lamp and its sign sections, check device information, and control the lamp from the same environment you use for the rest of your broadcast infrastructure.

## Key Features

- **Lamp status monitoring**: See at a glance what each sign section is currently displaying, so operators always know which cue is shown in the studio.
- **Remote lamp control**: Change the state of the lamp directly from DataMiner, without needing to open the device's web interface.
- **Device information**: Keep track of device details such as identification, network settings and firmware version for every lamp in your facility.
- **Single and dual sign support**: Monitor and control lamps configured with one full-width section or with two independent sections.
- **Alarm monitoring and trending**: Use standard DataMiner alarm templates and trending on lamp parameters to detect communication loss or unexpected states.

## Use Cases

### Centralized Studio Signaling Overview

**Challenge**: In facilities with many studios and booths, staff have to walk around or check each lamp's web interface separately to know which rooms are live or recording.

**Solution**: The connector brings the status of every LMPSH-IP lamp into DataMiner, where it can be shown in a single overview, for example in a Visual Overview or a Low-Code App.

**Benefit**: Operators get an immediate, facility-wide view of studio states from one place.

### Automated On-Air Cues

**Challenge**: Studio signal lamps need to follow the actual broadcast workflow, and manual switching is error-prone.

**Solution**: Because the lamp can be controlled from DataMiner, its state can be changed from Automation scripts, correlation rules or other DataMiner-driven workflows.

**Benefit**: Studio cues stay in sync with production events, reducing the risk of someone entering a studio that is on air.

### Proactive Monitoring of Signaling Devices

**Challenge**: A lamp that has lost power or network connectivity can go unnoticed until it is needed.

**Solution**: DataMiner continuously polls the lamp and raises an alarm when communication is lost or when a monitored value goes out of its expected range.

**Benefit**: Problems with studio signaling are detected and fixed before they affect a live production.

## Technical Reference

### Prerequisites

- **IP connectivity** between the DataMiner Agent and the lamp, which receives its address through DHCP by default or can be configured with a static IPv4 address.
- **HTTP access** to the device's web service on the configured port (default: *80*).
- **Valid device credentials** for an authorized user account on the lamp.

### HTTP Connection - Main

This connector uses an HTTP connection and requires the following input during element creation:

HTTP CONNECTION:

- **IP address/host**: The polling IP or hostname of the lamp.
- **IP port**: The IP port of the lamp (default: *80*).

### Initialization

After the element has been created, enter the username and password of an authorized account on the lamp in the element's configuration parameters, so that the connector can authenticate with the device.

### Web Interface

The web interface is only accessible when the client machine has network access to the product.
