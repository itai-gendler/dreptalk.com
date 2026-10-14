---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "pairing-code",
      "effect": "changes",
      "to": "Approved"
    }
  ],
  "permits": [
    {
      "actors": [
        "drep",
        "spo",
        "cc-member",
        "proposer",
        "co-proposer",
        "delegator",
        "moderator"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/api/auth/pair/approve.ts"
    }
  ]
}
---

# Only a signed-in person approves a pairing code

A pairing code is approved from a device already signed in to the account the phone joins.
