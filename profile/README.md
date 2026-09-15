<!--
  Besisglas GitHub Organization Profile README

  Publish this file at:
  Besisglas/.github/profile/README.md

  Before publishing:
  1. Replace every "MODEL-ID" with the product's exact model number.
  2. Replace each temporary https://github.com/Besisglas link with the
     corresponding product repository URL.
  3. The common-guide links assume a public repository named "support".
  4. Optionally add a brand logo at profile/assets/besisglas-logo.png and
     uncomment the image line below.
  5. Remove products that are not yet publicly supported.
-->

<div align="center">

<!-- <img src="assets/besisglas-logo.png" alt="Besisglas" width="200"> -->

# Besisglas

### Zigbee Products · Home Assistant Solutions · Product Support

Practical Zigbee products and clear documentation for open, flexible smart homes.

[Product Documentation](#product-documentation) · [Common Guides](#common-guides) · [Get Support](#get-support)

</div>

---

## Welcome

Besisglas offers Zigbee sensors, coordinators, and Home Assistant solutions for users who value local control, flexible integration, and straightforward setup.

This is the official documentation center for Besisglas products. Select your product below to find setup instructions, pairing and reset procedures, compatibility information, downloads, technical references, and troubleshooting help.

> [!IMPORTANT]
> Most Besisglas Zigbee end devices require a compatible Zigbee hub or coordinator. They do not connect directly to a standard Wi-Fi router. Always check the compatibility information for your exact product model before purchasing or configuring a device.

## Product Documentation

Model numbers are printed on the product label, packaging, or user manual. Products with a similar appearance may use different hardware, so please confirm the model number before following a guide.

### Environmental Sensors

| Product | Picture | Model | Main Feature | Documentation |
| --- | --- | --- | --- | --- |
| Zigbee Temperature & Humidity Sensor | <img src="images/Zigbee%20Temperature%20&%20Humidity%20Sensor.png" alt="Sensor" width="180"> | `ZB-TH` | Slim, AAA-powered environmental sensor | [Please wait for documentation](https://github.com/Besisglas) |
| Zigbee Temperature & Humidity Sensor with Display | <img src="images/Zigbee%20Temperature%20&%20Humidity%20Sensor%20With%20Display.png" alt="Sensor" width="180"> | `ZB-THD` | Local temperature and humidity display | [Please wait for documentation](https://github.com/Besisglas) |

### Presence Sensors

| Product | Picture | Model | Main Feature | Documentation |
| --- | --- | --- | --- | --- |
| Zigbee 24 GHz mmWave Presence Sensor | <img src="images/Zigbee%20Radar%20Motion%20&%20Human%20Presence%20Sensor.png" alt="Sensor" width="180"> | `MS01` | Detects both movement and stationary human presence | [View documentation](https://github.com/Besisglas/Zigbee-Radar-Motion-Human-Presence-Sensor) |

### Security & Safety Sensors

| Product | Picture | Model | Main Feature | Documentation |
| --- | --- | --- | --- | --- |
| Zigbee Water Leak Sensor with Probe Cable | <img src="images/Zigbee%20Water%20Leak%20Sensor%20with%20Probe%20Cable.png" alt="Sensor" width="180"> | `ZB-WLS` | Remote wired probe for leak detection | [Please wait for documentation](https://github.com/Besisglas) |
| Zigbee Door & Window Sensor | <img src="images/Zigbee%20Door%20&%20Window%20Sensor.png" alt="Sensor" width="180"> | `ZB-DWS` | Wireless open and close detection | [Please wait for documentation](https://github.com/Besisglas) |
| Zigbee Wired Door Sensor | <img src="images/Zigbee%20Wired%20Door%20Sensor.png" alt="Sensor" width="180"> | `ZB-WDS` | External wired contact for flexible installation | [Please wait for documentation](https://github.com/Besisglas) |

### Zigbee Coordinators & Connectivity

| Product | Picture | Model | Connection | Documentation |
| --- | --- | --- | --- | --- |
| Zigbee USB Dongle | <img src="images/Zigbee%20USB%20Dongle ZBM-MG21.png" alt="Dongle" width="180"> | `ZBM-MG21` | USB Zigbee coordinator for compatible smart home software | [View documentation](https://github.com/Besisglas) |
| Zigbee Ethernet & Wi-Fi Dongle | <img src="images/Zigbee%20Ethernet%20&%20Wi-Fi%20Dongle ETH-52P.png" alt="Dongle" width="180"> | `ETH-52P` | Network-connected Zigbee coordinator | [Please wait for documentation](https://github.com/Besisglas) |

### Home Assistant Kits

| Product | Picture | Model | Description | Documentation |
| --- | --- | --- | --- | --- |
| Home Assistant Box | <img src="images/Home%20Assistant%20Box HA70.jpg" alt="Box" width="180"> | `HA70` | Home Assistant box with selected accessories for getting started | [Please wait for documentation](https://github.com/Besisglas) |

## Common Guides

These guides apply to multiple Besisglas products:

- [Getting Started with Zigbee](support/docs/getting-started-with-zigbee.md)
- [Setting Up Devices with Home Assistant ZHA](support/docs/home-assistant-zha.md)
- [Setting Up Devices with Zigbee2MQTT](support/docs/zigbee2mqtt.md)
- [Pairing, Re-pairing, and Factory Reset](support/docs/pairing-and-factory-reset.md)
- [Improving Zigbee Range and Network Reliability](support/docs/zigbee-network-reliability.md)
- [Understanding Zigbee Battery Reporting](support/docs/battery-reporting.md)
- [General Troubleshooting](support/docs/general-troubleshooting.md)

## Compatibility Information

Zigbee interoperability can vary by product model, coordinator, hub, firmware version, and software integration. Support for one Besisglas product does not automatically mean that every Besisglas product is supported by the same platform.

Individual product repositories distinguish compatibility using the following terms:

- **Verified** — Tested directly with the specified platform or integration.
- **Community Reported** — Reported working by customers or community members, but not fully tested by Besisglas.
- **Not Tested** — No reliable test result is currently available.
- **Not Supported** — Known to be incompatible or missing required functionality.

For the most accurate information, always use the compatibility table in the repository for your exact model.

## Get Support

For technical help, open the documentation repository for your product and review its troubleshooting section first. If the issue remains, use the support option provided in that repository.

When requesting technical help, please include:

- Exact product model number
- Zigbee hub or coordinator model
- Smart home platform and integration, such as Home Assistant with ZHA or Zigbee2MQTT
- A short description of the problem
- LED behavior or error messages, if applicable
- Troubleshooting or reset steps already attempted

For questions involving an Amazon order, replacement, refund, shipping address, or other private information, please contact Besisglas through the private support method shown in your order or user manual.

> [!CAUTION]
> Do not post Amazon order numbers, names, email addresses, shipping addresses, network credentials, or other personal information in a public GitHub issue.

## About Besisglas

Besisglas focuses on practical Zigbee devices and Home Assistant accessories for connected homes. Our goal is to make smart home products easier to install, understand, integrate, and maintain through clear documentation and transparent compatibility information.

This GitHub organization contains product documentation and support resources. Product availability, specifications, package contents, and platform compatibility may vary by model and region. Refer to the documentation for the exact model you own.

---

<div align="center">

**Besisglas Product Documentation & Support**

Copyright © 2026 Besisglas. All rights reserved.

Zigbee is a registered trademark of the Connectivity Standards Alliance. Home Assistant and other product or company names are trademarks of their respective owners. References to third-party platforms do not imply endorsement or affiliation.

</div>
