---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "cast-vote"
    },
    {
      "type": "capability",
      "id": "record-on-chain-votes"
    },
    {
      "type": "entity",
      "id": "post",
      "facts": [
        "Vote"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/voteRationalePost.ts#removeVoteRationalePost"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/moderation.md"
    }
  ]
}
---

# A cross-posted rationale stands only while its vote stands

The frozen copy is replaced when the DRep votes again with the box ticked, removed when it votes again without it, and removed when the vote never confirms on chain.
