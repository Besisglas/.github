# Getting Started with Zigbee

> Last reviewed: September 2026

This guide explains what you need to use a Besisglas Zigbee product and the recommended order for building a new Zigbee network.

## What You Need

Most installations require all three of the following:

1. **A Zigbee coordinator or hub** — The radio that creates and manages the Zigbee network.
2. **A smart home platform** — For example, Home Assistant using ZHA or Zigbee2MQTT.
3. **One or more Zigbee devices** — Sensors, switches, routers, or other products that join the network.

A standard Wi-Fi router cannot replace a Zigbee coordinator. A network-connected Zigbee coordinator may use Ethernet or Wi-Fi to communicate with the host, but it still contains a separate Zigbee radio.

## Zigbee Device Roles

| Role | What it does | Typical examples |
| --- | --- | --- |
| Coordinator | Creates and manages one Zigbee network | USB or Ethernet Zigbee coordinator |
| Router | Relays messages and expands the mesh | Mains-powered plugs, repeaters, and some lights |
| End device | Sends sensor or control data and may sleep to save power | Battery sensors, door contacts, buttons |

A Zigbee network normally has one coordinator. A Zigbee device can belong to only one Zigbee network at a time. Battery-powered end devices normally do not extend network range.

## Choose One Integration

Home Assistant users commonly choose either ZHA or Zigbee2MQTT.

| Option | General characteristics |
| --- | --- |
| ZHA | Integrated directly into Home Assistant with setup and device management in the Home Assistant interface |
| Zigbee2MQTT | Runs as a separate Zigbee service, uses MQTT, and provides its own frontend and device definitions |

Do not configure the same coordinator in ZHA and Zigbee2MQTT at the same time. Choose one integration for each coordinator and Zigbee network.

Before choosing, check the repository for your exact Besisglas model. A product may expose different entities or features on different integrations.

## Plan the Network Before Pairing

- Place the coordinator away from Wi-Fi routers, USB 3.x equipment, SSDs, and other sources of 2.4 GHz interference.
- If using a USB coordinator, use a shielded USB extension cable when possible.
- Install reliable, always-powered Zigbee routers before adding distant battery sensors.
- Keep routers powered continuously. Switching off a router at the wall can interrupt routes used by other devices.
- Pair devices near their intended installation location when the mesh already has coverage there.

## First-Time Setup

1. Install and configure the coordinator using its own documentation.
2. Create the Zigbee network in ZHA, Zigbee2MQTT, or another supported platform.
3. Confirm that the coordinator is online and the platform is ready to accept devices.
4. Enable device joining in the platform.
5. Put the Besisglas product into pairing mode using its model-specific instructions.
6. Wait for discovery and configuration to finish before moving or testing the device.
7. Give the device a clear name and assign it to a room or area.
8. Test every reported function, not only whether the device appears online.
9. Close device joining when finished.

## After Pairing

Battery-powered devices may sleep for long periods and may not answer immediately. Trigger the sensor or briefly wake it according to its product instructions if configuration is still completing.

Test the device from its final location. Confirm that events and measurements update reliably over time. If the device becomes unavailable, review [Zigbee Range and Network Reliability](zigbee-network-reliability.md).

## Next Steps

- [Set up with Home Assistant ZHA](home-assistant-zha.md)
- [Set up with Zigbee2MQTT](zigbee2mqtt.md)
- [Pairing, Re-pairing, and Factory Reset](pairing-and-factory-reset.md)
- [General Troubleshooting](general-troubleshooting.md)

## Official References

- [Home Assistant: Zigbee Home Automation](https://www.home-assistant.io/integrations/zha/)
- [Zigbee2MQTT: Getting Started](https://www.zigbee2mqtt.io/guide/getting-started/)
