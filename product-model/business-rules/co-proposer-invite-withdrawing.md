---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "co-proposer-mandate",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "grants",
          "entity": "proposer"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/api/auth/co-proposer/withdraw.ts"
    }
  ]
}
---

# Only its proposer withdraws an invite

A proposer withdraws only its own pending invites.
