---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "sign-in"
    },
    {
      "type": "entity",
      "id": "device",
      "facts": [
        "Roles"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/resolveRole.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/handlers.ts#handleVerify"
    }
  ]
}
---

# Every role is confirmed on chain at sign-in, and a delegator sign-in is read-only

A DRep must be registered and active, an SPO's Calidus key registered to a pool, a CC hot key currently authorized and a proposer's reward address the submitter of an action. A delegator sign-in never carries a writer role, even for an account that holds one.
