---
{
  "relations": [
    {
      "entity": "vote-rationale",
      "verb": "has",
      "cardinality": "one-to-one"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/drepVotes.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/voting.md"
    }
  ]
}
---

# Vote

A Yes, No or Abstain from one voter on one governance action: a DRep, an SPO or a Constitutional Committee member. A later vote by the same voter replaces the earlier one, which stays visible.

## Information kept

- **Voter body** — DRep, SPO or CC
- **Choice** — Yes, No or Abstain
- **Rationale link** — the anchor of the rationale document the vote links, if any
- **Cast at** — when it was cast
- **Earlier votes** — the votes it replaced, each marked Changed or Revoted
- **Counted** — whether it counted toward the outcome; votes after ratification are not counted
- **Voting power** — the power behind it
- **Transaction** — the transaction that carried it

## States

### Pending

Cast through DRepTalk and shown at once; not yet seen on chain.

### Confirmed

Seen on chain by the vote sync.

### Failed

Cast through DRepTalk but never confirmed on chain.
