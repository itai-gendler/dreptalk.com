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
      "entity": "vote",
      "verb": "casts",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/voting-as-an-spo.md"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/resolveRole.ts#resolveSpo"
    }
  ]
}
---

# SPO

A stake pool operator signed in with the Calidus key registered to its pool. An SPO writes in threads; its pool votes on chain with the pool cold key outside DRepTalk and appear here once synced.

## Information kept

- **Pool ID** — the pool the Calidus key is registered to
- **Pool name** — the pool ticker and name from its metadata
