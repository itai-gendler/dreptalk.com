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
      "verb": "holds",
      "cardinality": "one-to-one"
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
      "target": "src/lib/forum/mandate.ts"
    }
  ]
}
---

# Co-proposer

A person a proposer has authorized to write on its behalf with their own wallet. The role exists only while the mandate is active; a co-proposer signs in through the proposer sign-in, and every post shows their own name together with the proposer they write for.
