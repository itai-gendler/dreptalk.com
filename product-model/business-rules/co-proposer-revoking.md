---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "co-proposer-mandate",
      "effect": "changes",
      "to": "Revoked"
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
      "target": "src/lib/db/proposerGrants.ts"
    }
  ]
}
---

# Only its proposer revokes a co-proposer

A proposer revokes only the mandates it granted.
