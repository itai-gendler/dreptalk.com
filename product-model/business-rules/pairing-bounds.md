---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "pair-device"
    },
    {
      "type": "capability",
      "id": "approve-device-pairing"
    },
    {
      "type": "entity",
      "id": "pairing-code"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/pairing.ts#PAIRING_TTL_SEC"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/pair-a-device.md"
    }
  ]
}
---

# A pairing code works for ten minutes and grants no more than the approving device holds

The phone redeems the code once, and its session never carries more roles than the session that approved it. Every approval adds a device-paired notice to the account.
