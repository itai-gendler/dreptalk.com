---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "changes",
      "facts": [
        "Inbox last opened"
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
    },
    {
      "related": [
        {
          "verb": "uses",
          "entity": "delegator"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "uses",
          "entity": "moderator"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/notifications.ts"
    }
  ]
}
---

# A person marks only their own inbox as opened

Opening notifications records the visit on the person's own account.
