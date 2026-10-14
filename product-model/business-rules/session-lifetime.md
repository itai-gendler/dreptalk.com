---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "sign-in"
    },
    {
      "type": "capability",
      "id": "pair-device"
    },
    {
      "type": "entity",
      "id": "device"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/session.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/signing-in.md"
    }
  ]
}
---

# A device stays signed in 30 days after its last use and 90 days at most

After that it signs in again with a new signature, or a new pairing code on a phone.
