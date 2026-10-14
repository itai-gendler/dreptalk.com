---
{
  "entities": [
    {
      "entity": "thread",
      "shows": [
        "Title"
      ]
    },
    {
      "entity": "governance-action",
      "collects": [
        "Type",
        "Title",
        "Abstract",
        "Motivation",
        "Rationale",
        "Authors",
        "References",
        "On-chain changes"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/ga/new.astro"
    }
  ]
}
---

# Submit a governance action

The form that builds, reviews and submits a new governance action from the person's wallet.
