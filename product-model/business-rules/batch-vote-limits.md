---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "cast-vote"
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
      "target": "src/lib/governance/voteLimits.ts#MAX_UNIQUE_BATCH_RATIONALES"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/voting-on-multiple-actions.md"
    }
  ]
}
---

# A batch holds up to 50 votes and 10 different rationale texts

A batch is one transaction and all-or-nothing. A shared or repeated text counts once; each rationale holds at most 60,000 characters.
