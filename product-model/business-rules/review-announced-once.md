---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "announce-governance-review"
    },
    {
      "type": "entity",
      "id": "governance-review-edition",
      "facts": [
        "Announced"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/reviewAnnouncements.ts#announceLatestEdition"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/governance-review.md"
    }
  ]
}
---

# Each Governance Review edition is announced once

A new edition reaches every account once; corrections to it send nothing.
