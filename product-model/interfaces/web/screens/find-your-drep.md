---
{
  "entities": [
    {
      "entity": "drep",
      "shows": [
        "Name",
        "Image",
        "Voting power"
      ]
    },
    {
      "entity": "governance-action",
      "shows": [
        "Title",
        "Type",
        "Abstract"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/match.astro"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/drep-matching.md"
    }
  ]
}
---

# Find your DRep

A quiz of real governance questions that ranks DReps by how their past votes match the answers.
