---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "vote",
      "effect": "changes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "casts",
          "entity": "drep"
        }
      ]
    },
    {
      "unattended": true
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/drepVotes.ts"
    }
  ]
}
---

# Only its DRep changes a vote

A DRep replaces only its own vote; the Product confirms or fails votes from the chain.
