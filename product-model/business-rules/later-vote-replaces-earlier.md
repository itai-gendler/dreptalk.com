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
      "id": "vote",
      "facts": [
        "Earlier votes"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/voteHistory.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/voting.md"
    }
  ]
}
---

# A later vote replaces the earlier one while the action is open

The newest vote of a voter counts; the earlier ones stay listed, marked Changed when the position moved and Revoted when it did not. Once an action closes, votes are final.
