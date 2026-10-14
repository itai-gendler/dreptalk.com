---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "co-proposer-mandate",
      "effect": "changes",
      "to": "Active"
    }
  ],
  "permits": [
    {
      "actors": [
        "visitor"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/coProposerRedeem.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/proposers.md"
    }
  ]
}
---

# Whoever holds the invite link accepts it

The invite link is the credential: the person who opens it accepts with their own wallet, without an on-chain role.
