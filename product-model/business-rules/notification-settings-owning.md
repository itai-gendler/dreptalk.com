---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "changes",
      "facts": [
        "Push preferences",
        "Telegram preferences"
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
      "target": "src/pages/api/notifications/prefs.ts"
    }
  ]
}
---

# A person changes only their own notification settings

Notification settings belong to the person's own account.
