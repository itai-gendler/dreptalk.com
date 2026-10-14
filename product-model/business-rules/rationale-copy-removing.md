---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "post",
      "effect": "changes",
      "to": "Deleted"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "writes",
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
      "target": "src/lib/db/voteRationalePost.ts#removeVoteRationalePost"
    }
  ]
}
---

# A cross-posted rationale leaves the discussion only through its DRep's next vote or a failed vote

Members never delete posts; the DRep's own re-vote, or the Product when the vote never confirms, removes the frozen copy.
