---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/delegatorFollows.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/for-delegators.md"
    }
  ]
}
---

# Delegation

Where a signed-in account's stake currently delegates its voting power, read from the chain.

## Information kept

- **Delegated to** — a DRep, Always abstain, Always no confidence, or nothing
- **Delegated since** — the epoch of the latest vote-delegation certificate
- **Stake address** — the stake address followed; it stays on the server
- **Last checked** — when the delegation was last read from the chain

## States

### Looking up

Not read from the chain yet.

### Tracked

Read from the chain and followed.
