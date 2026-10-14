---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "config/ncl-periods.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/treasury.ts"
    }
  ]
}
---

# Net Change Limit period

A budget period with its Net Change Limit, against which enacted treasury withdrawals are tracked.

## Information kept

- **Ceiling** — the operative Net Change Limit, with any earlier ceiling
- **Epochs** — the epochs the period runs, with any extension
- **Withdrawn** — enacted treasury withdrawals in the period
- **Remaining** — what is left under the ceiling
- **Defining actions** — the info actions that set the limit, and curated challengers
