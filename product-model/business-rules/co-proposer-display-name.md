---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "changes",
      "facts": [
        "Display name"
      ]
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
      "target": "src/lib/db/proposerGrants.ts#redeemGrant"
    }
  ]
}
---

# A co-proposer's display name is set when they accept their invite

The person accepting an invite picks the name their posts show; an existing name is never overwritten.
