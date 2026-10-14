---
{
  "kind": "person",
  "acts": "external",
  "relations": [
    {
      "entity": "account",
      "verb": "uses",
      "cardinality": "one-to-one"
    }
  ],
  "references": [
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/for-delegators.md"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/delegatorLogin.ts"
    }
  ]
}
---

# Delegator

A person signed in read-only with the stake wallet that holds their delegated ada, and the role every signed-in account holds whatever its writer roles. A delegator follows their DRep, receives notifications and manages their own devices and notification settings, but never posts, reacts, flags or votes.
