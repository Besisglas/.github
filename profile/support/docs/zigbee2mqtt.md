# Setting Up Devices with Zigbee2MQTT

> Last reviewed: September 2026

Zigbee2MQTT connects Zigbee devices to an MQTT broker through a supported coordinator. It includes a web frontend for network management, pairing, device settings, exposes, logs, and other functions.

This guide provides a general workflow. Use the repository for your exact Besisglas model for its pairing method, LED pattern, supported features, and any model-specific notes.

## Before You Begin

You need:

- A coordinator supported by Zigbee2MQTT
- A host system for Zigbee2MQTT
- A working MQTT broker
- The correct serial, Ethernet, or Wi-Fi connection details for the coordinator
- The exact model number of the Besisglas device

The coordinator must not be in use by ZHA or another Zigbee application. One coordinator cannot be actively controlled by ZHA and Zigbee2MQTT at the same time.

## Configure Zigbee2MQTT

1. Install Zigbee2MQTT using the official instructions for your platform.
2. Open the first-run onboarding page or configuration interface.
3. Enter the MQTT broker information.
4. Select the correct coordinator and adapter type.
5. Configure the coordinator path or network address using its product documentation.
6. Enable the frontend and Home Assistant integration if they are part of your installation.
7. Start Zigbee2MQTT and confirm that the coordinator initializes without errors.

Adapter type, port, baud rate, and flow-control settings depend on the coordinator. Do not copy settings from an unrelated adapter.

## Pair a Besisglas Device

1. Open the Zigbee2MQTT frontend.
2. Select **Permit join** to temporarily allow new devices to join.
3. Put the Besisglas device into pairing mode using its model-specific instructions.
4. Watch the Zigbee2MQTT log for discovery, interview, and configuration progress.
5. Wait until the interview completes successfully.
6. Rename the device with a clear, stable friendly name.
7. Open the device page and verify its **Exposes** and reported values.
8. Disable **Permit join** when pairing is complete.

If the device was previously paired with another Zigbee network, factory-reset it before pairing.

## Pairing Through a Router

Zigbee2MQTT can allow a device to join through a selected coordinator or router. This can be helpful when installing a device far from the coordinator, but it does not guarantee that the same route will remain in use permanently.

For most installations, first build a healthy mesh with reliable, always-powered routers, then pair the device near its final location.

## Verify the Device

After pairing:

- Confirm that the device is identified by the expected model.
- Check that all expected exposes are present.
- Trigger the device and confirm that new messages appear.
- Check the product repository for supported settings and known limitations.
- Allow sleeping battery devices time to send their first scheduled reports.

If a Besisglas product repository states that no external converter is required, do not install one unless the documentation specifically instructs you to do so.

## If Pairing or Interview Fails

1. Confirm that joining is permitted.
2. Repeat the exact factory-reset procedure.
3. Check the battery, power supply, and polarity.
4. Keep the device powered and awake during the interview when required.
5. Improve coordinator placement and reduce USB or Wi-Fi interference.
6. Retry near a known-good router or temporarily closer to the coordinator.
7. Review the Zigbee2MQTT logs for the failure stage.
8. Check whether the exact product model is listed as supported.

## Official References

- [Zigbee2MQTT: Getting Started](https://www.zigbee2mqtt.io/guide/getting-started/)
- [Zigbee2MQTT: Allowing Devices to Join](https://www.zigbee2mqtt.io/guide/usage/pairing_devices.html)
- [Zigbee2MQTT: Supported Devices](https://www.zigbee2mqtt.io/supported-devices/)
