---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "drep-link",
      "effect": "changes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "owns",
          "entity": "drep"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/drepLink/claimRequest.ts"
    }
  ]
}
---

# Only its DRep changes a drep.link

A DRep changes only its own drep.link.
