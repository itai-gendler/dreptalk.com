---
{
  "kind": "person",
  "acts": "external",
  "relations": [
    {
      "entity": "account",
      "verb": "uses",
      "cardinality": "one-to-one"
    },
    {
      "entity": "thread",
      "verb": "opens",
      "cardinality": "one-to-many"
    },
    {
      "entity": "post",
      "verb": "writes",
      "cardinality": "one-to-many"
    },
    {
      "entity": "reaction",
      "verb": "gives",
      "cardinality": "one-to-many"
    },
    {
      "entity": "flag",
      "verb": "raises",
      "cardinality": "one-to-many"
    },
    {
      "entity": "co-proposer-mandate",
      "verb": "grants",
      "cardinality": "one-to-many"
    },
    {
      "entity": "governance-action",
      "verb": "submitted",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/proposers.md"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "config/proposers.ts"
    }
  ]
}
---

# Proposer

A person signed in with the reward address that submitted at least one governance action. A proposer writes in threads and authorizes co-proposers to write on its behalf.

## Information kept

- **Reward address** — the stake address that receives the action deposits back
- **Curated name** — the organization name DRepTalk curates for well-known proposers
