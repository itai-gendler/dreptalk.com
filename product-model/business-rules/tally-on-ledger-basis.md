---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "view-governance-action"
    },
    {
      "type": "entity",
      "id": "governance-action",
      "facts": [
        "Tallies",
        "Thresholds"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/thresholds.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/understanding-a-governance-action.md"
    }
  ]
}
---

# A tally is the yes share of the counted stake

For each voting body, abstaining stake is excluded and stake that did not vote counts on the No side, the basis the chain uses for ratification; an action with a threshold shows whether it is met.
