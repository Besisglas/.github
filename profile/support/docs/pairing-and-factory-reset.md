# Pairing, Re-pairing, and Factory Reset

> Last reviewed: September 2026

Pairing procedures are model-specific. This guide explains the overall process but does not define a universal button duration or LED pattern. Always check the repository for the exact Besisglas model before resetting a device.

## Understand the Terms

| Term | Meaning |
| --- | --- |
| Pairing | Adding a device to a Zigbee network for the first time |
| Re-pairing | Joining the same device again after a connection or configuration problem |
| Factory reset | Erasing the device's current Zigbee network information and returning its configurable state to the documented default |

A factory reset may remove network information and settings. It does not necessarily remove the old device entry from the hub or smart home platform.

## Before Pairing

- Confirm the exact model number.
- Open its product repository and find the documented pairing procedure.
- Verify that the hub, coordinator, and Zigbee integration are online.
- Check that the device is supported by the selected platform.
- Install the correct battery or power supply.
- Make sure the device is not already joined to another Zigbee network.
- Confirm that the network has sufficient coverage at the installation location.

## Standard Pairing Workflow

1. Enable device joining in the Zigbee platform.
2. Activate pairing mode using the model-specific button sequence.
3. Confirm the documented LED or screen indication.
4. Keep the device powered until discovery and configuration finish.
5. Verify that the correct model and expected functions appear.
6. Trigger the sensor to confirm that it reports a state change.
7. Close device joining when finished.

Some battery-powered devices sleep quickly. If its product guide instructs you to press a button, trigger the sensor, or keep it awake during configuration, continue doing so until the interview completes.

## When Re-pairing May Help

Consider re-pairing when:

- The device was factory-reset accidentally.
- The initial interview did not finish.
- Expected entities or exposes did not appear.
- You moved the device to a different Zigbee network.
- The coordinator or platform was replaced without migrating the old network.

If a device is simply offline, first check power, range, routers, and interference. Re-pairing is not always necessary and should not be the first response to every connection problem.

## Moving to Another Hub or Coordinator

A Zigbee device normally remembers one network. To move it:

1. Record any automations or names that depend on the old device entry.
2. Remove the device gracefully from the old platform when possible.
3. Factory-reset it using the exact product instructions.
4. Enable joining on the new network.
5. Pair and verify every feature again.

## If the Device Is Not Discovered

- Confirm that the join window is still open.
- Repeat the reset sequence exactly; button duration and LED timing matter.
- Try a fresh battery, even if the existing battery shows some voltage.
- Move away from USB 3.x equipment and strong 2.4 GHz transmitters.
- Try closer to the coordinator or a known-good Zigbee router.
- Check whether the platform is detecting an unknown device in its logs.
- Wait for the current attempt to finish before starting another reset.

## If the Device Appears but Configuration Fails

- Keep the device awake if it is a sleepy end device.
- Do not remove power during the interview.
- Retry after improving signal conditions.
- Review the integration log for timeouts or unsupported clusters.
- Confirm that no outdated custom handler or external converter is interfering.
- Use the product repository to compare the expected model identifier and exposed functions.

## Related Guides

- [Home Assistant ZHA Setup](home-assistant-zha.md)
- [Zigbee2MQTT Setup](zigbee2mqtt.md)
- [Zigbee Range and Network Reliability](zigbee-network-reliability.md)
- [General Troubleshooting](general-troubleshooting.md)

## Official References

- [Home Assistant: Adding Zigbee Devices with ZHA](https://www.home-assistant.io/integrations/zha/#adding-devices)
- [Zigbee2MQTT: Allowing Devices to Join](https://www.zigbee2mqtt.io/guide/usage/pairing_devices.html)
