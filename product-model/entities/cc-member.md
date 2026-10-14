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
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/resolveRole.ts#resolveCc"
    }
  ]
}
---

# CC member

A Constitutional Committee member signed in with its authorized committee hot key. A CC member writes in threads; committee votes are cast on chain outside DRepTalk and appear here once synced.

## Information kept

- **Committee credential** — the cold credential, or the hot credential it signed with
- **Name** — the committee member name DRepTalk knows for the credential
