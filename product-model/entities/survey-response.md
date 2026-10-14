---
{
  "domain": "surveys",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/surveyTally.ts"
    }
  ]
}
---

# Survey response

One DRep's answer to a survey, read from the index once it is on chain.

## Information kept

- **Answers** — the chosen options or values
- **Counted** — whether it counts, or why it is excluded
- **Transaction** — the transaction that carried it
