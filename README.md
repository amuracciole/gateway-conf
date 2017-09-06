# The Things Network Frequency Plans

This repository contains the Things Network's frequency plans, in a YAML format. Those frequency plans are derived from the LoRaWAN regional parameters.

## Format

```yml
band-id: "BAND_ID" # ID of the band
channels: # List of channels
- frequency: 863000000 # Channel frequency
  data-rate: # Optional: If forcing a data rate for this specific frequency
    index: 3 # Index of the data rate to force within the region's data rates list
lora-std-channel: # Optional: specify a LoRa standard channel, according to the same specs than the previous frequency plans. Follows the same format than other channels.
  frequency: 863000000
  data-rate:
    index: 6
FSK-channel: # Optional: specify a FSK channel, according to the same specs than the previous frequency plans. Follows the same format than other channels.
  frequency: 868800000
  data-rate:
    index: 7
lbt: # Optional: Enabling listen-before-talk
  rssi-offset: 0 # Optional: RSSI offset
  rssi-target: -80 # Optional: RSSI offset
  scan-time: 128 # Scan time in micro-seconds
```
