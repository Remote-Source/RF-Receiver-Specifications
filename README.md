 RF and LoRa Receiver Specifications & Wireless Remote Control Receiver Documentation

**Remote Source RF receiver specifications, wireless relay controllers, pairing references, and OEM integration resources.**

[**Project documentation on GitHub Pages**](https://remote-source.github.io/RF-Receiver-Specification/) · [**View this repository**](https://github.com/Remote-Source/RF-Receiver-Specification) · [**Browse RF receivers**](https://www.remotesource.net/oem-rf-remote-control-key-fob-receivers/)

![RF receiver specifications visual preview for RS477, RS404PC-V4.0 and RS402PC-V2.0](assets/rf-receiver-specifications-preview.png)

*Illustrative specifications preview using publicly listed models; it is not a screenshot of the repository interface. Confirm specifications against the latest product documentation.*

## Quick start

Review the [receiver comparison](#receiver-specification-examples), follow the [model-specific product links](#featured-rf-receiver-models), and check [pairing and integration](#integration-checklist) before selecting hardware.

To obtain a local copy of the documentation **when the repository is publicly accessible or you have GitHub access**:

```bash
git clone https://github.com/Remote-Source/RF-Receiver-Specification.git
cd RF-Receiver-Specification

# Inspect the files and locate datasheets/manuals, if included
find . -type f \( -iname '*.pdf' -o -iname '*.md' -o -iname '*.png' \)
```

Example **reference data** for one documented receiver (not a hardware-control API or a file guaranteed to exist in this repository):

```json
{
  "model": "RS477",
  "receiver_type": "2-channel RF relay controller",
  "frequency_mhz": 433.92,
  "supply_voltage": "9-24 V AC/DC",
  "remote_code_capacity": 400,
  "supported_code_families": ["fixed", "learning", "rolling"]
}
```

Source: [RS477 official product specification](https://www.remotesource.net/product/rs477-rf-receiver-controller/).

## About

RF receiver specs for 315/433 MHz controllers, wireless relays, remote pairing, and OEM integration.

This repository is intended as a discoverable technical reference for comparing radio-frequency (RF) remote control receivers and planning wireless control integrations. It focuses on model-level specifications, compatibility questions, and links to official Remote Source documentation. It is **documentation**, not a software SDK, radio protocol implementation, or claim of universal remote compatibility.

**Jump to:** [Receiver models](#featured-rf-receiver-models) · [Specifications](#receiver-specification-examples) · [Applications](#applications-and-use-cases) · [Integration checklist](#integration-checklist) · [LoRa reference](#rf-versus-lora) · [Official manuals](#official-documentation) · [OEM solutions](#remote-source-custom-rf-solutions)

## Featured RF receiver models

- **[RS477 — 433.92 MHz 2-channel RF receiver](https://www.remotesource.net/product/rs477-rf-receiver-controller/):** Two channels, 9–24 V AC/DC, and storage for up to 400 remote codes.
- **[RS404PC-V4.0 — universal 4-channel RF receiver](https://www.remotesource.net/product/rs404pc-v4-0-rf-receiver-controller/):** 315 MHz / 433.92 MHz frequency options, multiple code families, and four control channels.
- **[RS402PC-V2.0 — 2-channel universal RF receiver](https://www.remotesource.net/product/rs402pc-v2-0-rf-receiver-controller/):** 315 MHz / 433.92 MHz frequency options and support for up to 400 remote codes.
- **[RS218 — 433 MHz learning-code receiver](https://www.remotesource.net/product/rs218-433mhz-rf-receiver/):** Compact receiver for compatible RF transmitters and remote-control automation.

## Receiver specification examples

| Model | RF frequency | Channels | Input voltage | Remote-code storage |
| --- | --- | ---: | --- | --- |
| [RS477](https://www.remotesource.net/product/rs477-rf-receiver-controller/) | 433.92 MHz | 2 | 9–24 V AC/DC | Up to 400 |
| [RS404PC-V4.0](https://www.remotesource.net/product/rs404pc-v4-0-rf-receiver-controller/) | 315 / 433.92 MHz options | 4 | 12 / 24 V DC (typical) | Confirm exact variant |
| [RS402PC-V2.0](https://www.remotesource.net/product/rs402pc-v2-0-rf-receiver-controller/) | 315 / 433.92 MHz options | 2 | 9–24 V AC/DC | Up to 400 |

**Important:** Frequencies may be selectable product variants rather than simultaneous operating bands. Fixed-code, learning-code, and rolling-code support depends on the exact receiver and compatible transmitter/protocol. Treat listed figures as product-reference values, not electrical or regulatory approvals for a specific installation.

## Applications and use cases

- **Access control and gate automation:** Match wireless key fob transmitters with compatible RF relay receiver inputs and channel functions.
- **Garage-door and barrier controls:** Compare operating frequency, code support, relay behavior, and memory capacity.
- **Security and alarm systems:** Evaluate receiver pairing options and interface requirements before integration.
- **Industrial wireless switching:** Assess voltage, output channels, control modes, environmental constraints, and antenna placement.
- **Smart home and OEM product development:** Evaluate receiver and transmitter combinations for custom wireless control applications.

## Integration checklist

1. **Verify the RF band:** 315 MHz, 433 MHz, and 433.92 MHz should not be treated as interchangeable without confirmed hardware compatibility.
2. **Check encoding and pairing:** Confirm the specific fixed, learning, or rolling-code protocol; matching frequency alone is insufficient.
3. **Check electrical requirements:** Verify input voltage, current draw, relay contact ratings, wiring diagrams, and isolation requirements.
4. **Check channel behavior:** Momentary, toggle, latching, and timed-output behavior vary by product.
5. **Evaluate the installed environment:** Antenna position, enclosure materials, interference, and physical barriers affect actual range.
6. **Validate regulatory requirements:** Verify regional RF rules and any required certifications for the final configuration.

For background reading, see [How to Use an RF Remote Control](https://www.remotesource.net/blog/how-to-use-an-rf-remote-control/) and [Key Features to Check in an RF Receiver](https://www.remotesource.net/blog/features-to-check-in-rf-reciever/).

## RF versus LoRa

Conventional 315 MHz and 433 MHz remote-control receivers and **LoRa / LoRaWAN** gateways serve different wireless-system requirements. **Do not assume that a conventional RF relay receiver supports LoRa or LoRaWAN.** For a separate LoRaWAN hardware reference, see the [Remote Source Indoor Femto Gateway specifications (PDF)](https://www.remotesource.net/wp-content/uploads/2024/08/LoRa-Indoor-Gateway_13-8-24.pdf).

## Official documentation

Visit the [Remote Source product manual and downloads library](https://www.remotesource.net/downloads/) for receiver guides, wiring information, and model-specific manuals, including RS401, RS402, RS404, RS406, RS412, and RX-Multi families. Download and verify the correct model revision before installation.

**Documentation links:** [RS477](https://www.remotesource.net/product/rs477-rf-receiver-controller/) · [RS404PC-V4.0](https://www.remotesource.net/product/rs404pc-v4-0-rf-receiver-controller/) · [RS402PC-V2.0](https://www.remotesource.net/product/rs402pc-v2-0-rf-receiver-controller/) · [All manuals](https://www.remotesource.net/downloads/)

## GitHub repository topics

Suggested GitHub **Topics** (add these separately in the repository's **About → Topics** settings):

`rf-receiver` · `rf-remote` · `433mhz` · `315mhz` · `wireless-receiver` · `remote-control` · `relay-controller` · `radio-frequency` · `wireless-automation` · `access-control` · `oem` · `iot` · `hardware-documentation` · `lorawan`

## Remote Source custom RF solutions

> **Need a compatible RF receiver, replacement remote, or custom OEM wireless control solution?**
>
> **Remote Source** supports RF remote control development, receiver selection, custom programming, and OEM manufacturing. Explore our wireless receivers and contact us to discuss your product requirements.
>
> **[Visit RemoteSource.net — Official Remote Source Website](https://www.remotesource.net/)** · **[Explore RF Remotes & Receivers](https://www.remotesource.net/oem-rf-remote-control-key-fob-receivers/)**
