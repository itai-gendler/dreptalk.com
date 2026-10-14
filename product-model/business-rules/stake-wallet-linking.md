---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "changes",
      "facts": [
        "Linked stake address"
      ]
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "uses",
          "entity": "drep"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "uses",
          "entity": "spo"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "uses",
          "entity": "cc-member"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "uses",
          "entity": "proposer"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "uses",
          "entity": "co-proposer"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/api/auth/link-stake.ts"
    }
  ]
}
---

# Only writers link a stake wallet in settings

Writers link a stake wallet to their account to follow its delegation; a delegator's account is its stake wallet.
