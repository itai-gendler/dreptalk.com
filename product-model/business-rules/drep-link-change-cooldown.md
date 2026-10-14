---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "change-drep-link"
    },
    {
      "type": "entity",
      "id": "drep-link"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/drepLink/claim.ts#checkClaimPolicy"
    }
  ]
}
---

# A drep.link changes at most every 90 days, and an old name redirects for 180

No new name is taken while an earlier one still redirects; switching back to it is possible once the cooldown ends.
