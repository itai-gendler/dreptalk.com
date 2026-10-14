---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "pairing-code",
      "effect": "changes",
      "to": "Used"
    }
  ],
  "permits": [
    {
      "actors": [
        "visitor"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/api/auth/pair/poll.ts"
    }
  ]
}
---

# Only the phone that showed a pairing code redeems it

The approved code signs in the phone that showed it, once.
