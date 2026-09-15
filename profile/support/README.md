# Besisglas Support

Common setup, pairing, network, and troubleshooting guides for Besisglas Zigbee products.

This repository contains information that applies to multiple products. For model-specific instructions—including the correct button sequence, LED behavior, power requirements, supported features, and verified compatibility—always use the documentation repository for your exact product model.

> [!IMPORTANT]
> Most Zigbee end devices require a compatible Zigbee hub or coordinator. They do not connect directly to a standard Wi-Fi router.

## Common Guides

| Guide | Use it when you need to… |
| --- | --- |
| [Getting Started with Zigbee](docs/getting-started-with-zigbee.md) | Understand the basic equipment, device roles, and setup order |
| [Home Assistant ZHA Setup](docs/home-assistant-zha.md) | Add a coordinator and pair Besisglas devices with ZHA |
| [Zigbee2MQTT Setup](docs/zigbee2mqtt.md) | Add a coordinator and pair Besisglas devices with Zigbee2MQTT |
| [Pairing, Re-pairing, and Factory Reset](docs/pairing-and-factory-reset.md) | Add a new device, move it to another network, or recover a failed pairing |
| [Zigbee Range and Network Reliability](docs/zigbee-network-reliability.md) | Improve coverage, reduce interference, or diagnose devices dropping offline |
| [Zigbee Battery Reporting](docs/battery-reporting.md) | Understand delayed, stepped, or apparently inaccurate battery readings |
| [General Troubleshooting](docs/general-troubleshooting.md) | Work through common symptoms before requesting support |

## Recommended Reading Order

If this is your first Zigbee installation:

1. Read [Getting Started with Zigbee](docs/getting-started-with-zigbee.md).
2. Choose either [Home Assistant ZHA](docs/home-assistant-zha.md) or [Zigbee2MQTT](docs/zigbee2mqtt.md).
3. Add mains-powered Zigbee router devices where additional coverage is needed.
4. Pair each product by following its model-specific repository.
5. Use the network and troubleshooting guides only if a problem appears.

## Repository Structure

```text
support/
├── README.md
├── docs/
│   ├── getting-started-with-zigbee.md
│   ├── home-assistant-zha.md
│   ├── zigbee2mqtt.md
│   ├── pairing-and-factory-reset.md
│   ├── zigbee-network-reliability.md
│   ├── battery-reporting.md
│   └── general-troubleshooting.md
└── assets/
    └── Add shared diagrams and screenshots here later
```

The `docs` directory is the published knowledge base. The optional `assets` directory can later contain shared screenshots, network diagrams, and icons. Product photographs and model-specific diagrams should remain in the corresponding product repository.

## Documentation Scope

The instructions in this repository are intentionally platform- and model-neutral. They do not replace:

- The user manual supplied with the product
- Safety instructions for the exact model
- Product-specific pairing and factory-reset steps
- Coordinator firmware and connection instructions
- The compatibility table in the product repository
- Official documentation from Home Assistant or Zigbee2MQTT

User-interface names and software behavior may change after this documentation is published. When a screen or option differs, check the official platform documentation linked at the end of each guide.

## Get Support

Start with the [General Troubleshooting](docs/general-troubleshooting.md) guide. If the issue remains, use the support option in the repository for your exact product model.

When requesting help, include the product model, coordinator model, smart home platform, Zigbee integration, LED behavior, and troubleshooting already attempted.

Do not post names, addresses, Amazon order numbers, network credentials, or other private information in a public GitHub issue. Use the private contact method shown in your Amazon order or product manual for order, replacement, refund, or shipping questions.

---

Copyright © 2026 Besisglas. All rights reserved.

Zigbee is a registered trademark of the Connectivity Standards Alliance. Home Assistant and other names are trademarks of their respective owners. References to third-party platforms do not imply endorsement or affiliation.
