---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "record-on-chain-votes"
    },
    {
      "type": "entity",
      "id": "vote-rationale"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/rationaleSync.ts#VOTE_RATIONALE_MIN_POWER_LOVELACE"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/voting-as-an-spo.md"
    }
  ]
}
---

# A rationale linked from outside DRepTalk is read only for voters with at least 10,000 ada

A rationale written on DRepTalk is always kept. For votes cast elsewhere, the linked document is read only when the voter holds at least 10,000 ada of voting weight; otherwise the vote shows Rationale unavailable.
