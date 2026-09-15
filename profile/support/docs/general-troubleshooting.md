# General Troubleshooting

> Last reviewed: September 2026

Use this guide for common Zigbee problems. Product-specific instructions always take priority, especially for pairing buttons, reset timing, LED patterns, supported entities, power supplies, and safety information.

## Start Here

Before changing the network:

1. Confirm the exact Besisglas model number.
2. Open the repository for that model.
3. Check the correct battery type or power supply.
4. Confirm which platforms and integrations are verified for the model.
5. Record the current symptom and LED behavior.
6. Change only one thing at a time.

## Symptom Guide

| Symptom | Common causes | First actions |
| --- | --- | --- |
| Device is not discovered | Joining closed, incorrect reset sequence, device still belongs to another network, weak signal, low battery | Reopen joining, repeat the exact model-specific reset, check power, test closer to a coordinator or router |
| Device appears but setup does not finish | Sleepy device stopped responding, interference, weak route, unsupported device definition | Keep the device awake as documented, improve placement, retry, review integration logs |
| Device goes offline after installation | Weak mesh, router powered off, interference, low battery, device moved after pairing | Check power and routers, test closer, improve coordinator placement, review the network map |
| Expected entity or expose is missing | Integration support difference, incomplete interview, wrong model identification, outdated custom handler | Compare the model ID, wake and reconfigure the device, check the product compatibility table |
| Battery percentage looks wrong | Delayed reporting, voltage-to-percentage estimation, different battery chemistry | Use the specified battery, trigger a report, wait for normal check-ins, read the battery guide |
| Sensor reports false or unstable values | Placement, environment, probe installation, sensitivity settings, radio interruptions | Follow the product installation guide, verify placement, check power and signal, review model settings |
| Device responds slowly | Weak route, congested mesh, interference, sleeping behavior | Check routers and interference; compare with the expected behavior for the device type |

## 1. Check Power

- Confirm battery polarity and remove any insulating tab.
- Try a fresh, known-good battery of the specified type.
- For powered devices, confirm the required voltage, cable, and power supply.
- Look for loose contacts, corrosion, damage, swelling, or leakage.

Do not use an unapproved power supply or battery type.

## 2. Check the Coordinator and Platform

- Confirm that the coordinator is online.
- Confirm that ZHA, Zigbee2MQTT, or the selected integration is running normally.
- Make sure another application is not trying to use the same coordinator.
- Check whether multiple Zigbee devices failed at the same time. If so, investigate the coordinator or network before resetting one sensor.
- Review recent software, firmware, USB, IP address, or network changes.

## 3. Check Pairing State

- Verify that the platform is actively permitting devices to join.
- Use the exact product-specific pairing or factory-reset sequence.
- If the device belonged to another network, reset it before joining the new one.
- Wait for discovery and the full interview to complete.
- Keep a sleepy device awake only as instructed for that model.

## 4. Check Range and Interference

- Test temporarily closer to the coordinator or a known-good router.
- Move a USB coordinator away from the computer with a shielded extension cable.
- Separate the coordinator from Wi-Fi access points, USB 3.x equipment, SSDs, and metal objects.
- Confirm that mains-powered Zigbee routers are still powered.
- Add a reliable router if the final location lacks coverage.

See [Zigbee Range and Network Reliability](zigbee-network-reliability.md) for a structured network check.

## 5. Check Device Data

After the device joins:

- Confirm that the manufacturer and model identifiers match the product documentation.
- Trigger each supported sensor function.
- Allow battery and periodic measurements time to report.
- Check the integration log for interview, configuration, or reporting errors.
- Remove outdated custom handlers or converters only when the product documentation says they are unnecessary or conflicting.

## 6. Reset or Re-pair Only When Needed

Do not factory-reset a device simply because it missed one update. First check power, mesh health, and expected sleepy-device behavior.

If reset or re-pairing is appropriate, follow [Pairing, Re-pairing, and Factory Reset](pairing-and-factory-reset.md). Record automation names or platform settings that may be affected before removing the existing device entry.

## Information to Include in a Support Request

- Besisglas product name and exact model
- Purchase region and approximate purchase date; do not post an order number publicly
- Hub or coordinator model
- Coordinator firmware version, when known
- Platform and version
- Integration, such as ZHA or Zigbee2MQTT
- What you expected to happen
- What actually happened
- LED behavior and error messages
- Troubleshooting already attempted
- Relevant logs with personal information and network credentials removed

For order, replacement, refund, address, or shipping questions, use the private support method shown in your Amazon order or product manual.

## Official References

- [Home Assistant: Zigbee Home Automation](https://www.home-assistant.io/integrations/zha/)
- [Zigbee2MQTT: Getting Started](https://www.zigbee2mqtt.io/guide/getting-started/)
- [Zigbee2MQTT: Improve Network Range and Stability](https://www.zigbee2mqtt.io/advanced/zigbee/02_improve_network_range_and_stability.html)
