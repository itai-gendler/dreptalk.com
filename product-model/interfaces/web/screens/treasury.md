---
{
  "entities": [
    {
      "entity": "net-change-limit-period",
      "shows": [
        "Ceiling",
        "Epochs",
        "Withdrawn",
        "Remaining",
        "Defining actions"
      ]
    },
    {
      "entity": "governance-action",
      "shows": [
        "Title",
        "Deposit",
        "On-chain changes",
        "Decided epoch"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/treasury.astro"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/treasury/[periodId].astro"
    }
  ]
}
---

# Treasury

Enacted treasury withdrawals tracked against the Net Change Limit of each budget period.
