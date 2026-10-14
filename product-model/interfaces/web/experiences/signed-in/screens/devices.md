---
{
  "entities": [
    {
      "entity": "device",
      "shows": [
        "Label",
        "Signed in at",
        "Last used"
      ]
    },
    {
      "entity": "pairing-code",
      "shows": [
        "Device label"
      ],
      "collects": [
        "Code"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/settings/devices.astro"
    }
  ]
}
---

# Devices

Settings, Devices: every signed-in device of the account, and approving a pairing code.
