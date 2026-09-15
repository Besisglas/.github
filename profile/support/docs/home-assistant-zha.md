# Setting Up Devices with Home Assistant ZHA

> Last reviewed: September 2026

Zigbee Home Automation (ZHA) is Home Assistant's built-in Zigbee integration. It connects supported Zigbee devices to Home Assistant through a compatible coordinator.

This is a general workflow. Use the repository for your exact Besisglas model for its pairing button, reset duration, LED pattern, supported entities, and verified compatibility.

## Before You Begin

Confirm that:

- Home Assistant is installed and running.
- Your Zigbee coordinator is supported by ZHA.
- The coordinator is connected and available to Home Assistant.
- The coordinator is not currently being used by Zigbee2MQTT or another Zigbee application.
- You know the exact Besisglas product model.

For a USB coordinator, a stable device path such as one under `/dev/serial/by-id/` is generally preferable to a changing path such as `/dev/ttyUSB0`. Home Assistant installations and operating systems differ, so follow the coordinator's own documentation.

For a network-connected coordinator, use the connection method and radio settings specified in its product repository. Prefer a stable local wired connection when available, and avoid placing the coordinator connection across a WAN or VPN.

## Add the ZHA Integration

Home Assistant may discover a compatible coordinator automatically. If it does not:

1. Open **Settings**.
2. Go to **Devices & services**.
3. Select **Add Integration**.
4. Search for **Zigbee Home Automation**.
5. Select the correct coordinator connection.
6. Follow the on-screen steps to create the Zigbee network.

Do not guess the radio type, baud rate, or flow-control setting. Use the values documented for your coordinator model.

## Add a Besisglas Device

1. Open **Settings → Connectivity → Zigbee** in Home Assistant. Interface wording may vary by Home Assistant version.
2. Select **Add device** to open the Zigbee network for joining.
3. Put the Besisglas device into pairing mode using its model-specific documentation.
4. Keep the device powered and wait for Home Assistant to discover and configure it.
5. When the device appears, give it a descriptive name and assign it to an area.
6. Open the device page and verify that the expected entities are present.
7. Trigger the sensor and confirm that its state changes in Home Assistant.

If a battery-powered device is discovered but configuration remains incomplete, follow its product instructions to wake or trigger it while ZHA completes the interview.

## Moving a Device from Another Zigbee Network

A Zigbee device can belong to only one network. If it was previously paired with another hub, coordinator, ZHA installation, or Zigbee2MQTT network, factory-reset it using the exact product instructions before trying to add it to the new network.

## Verify the Result

Check all functions documented for the model, such as:

- Temperature and humidity
- Open or closed state
- Water leak state
- Occupancy or presence state
- Battery level
- Signal or link-quality information, when available

An entity can take additional time or another device report to update after the initial join. Battery values in particular may not change immediately.

## If Pairing Fails

1. Confirm that ZHA is actively searching for devices.
2. Verify that the correct factory-reset or pairing procedure was used.
3. Install a fresh battery or confirm the power supply.
4. Try from the final installation location if a router is available there; otherwise test temporarily closer to the coordinator.
5. Move a USB coordinator away from the host using a shielded extension cable.
6. Keep a sleepy device awake if its product instructions require this during configuration.
7. Review ZHA logs and the [General Troubleshooting](general-troubleshooting.md) guide.

## Important Notes

- Do not remove and re-add the ZHA integration as a first troubleshooting step. That can disrupt the entire Zigbee network.
- Do not change the Zigbee channel casually on an established network. Some devices may take time to reconnect or may require additional recovery steps.
- Battery-powered sensors are often sleepy end devices. Short periods without communication do not always mean that the device has failed.

## Official Reference

- [Home Assistant: Zigbee Home Automation](https://www.home-assistant.io/integrations/zha/)
