---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "notification",
      "effect": "changes",
      "to": "Read"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "receives",
          "entity": "account"
        },
        {
          "verb": "uses",
          "entity": "drep"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "receives",
          "entity": "account"
        },
        {
          "verb": "uses",
          "entity": "spo"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "receives",
          "entity": "account"
        },
        {
          "verb": "uses",
          "entity": "cc-member"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "receives",
          "entity": "account"
        },
        {
          "verb": "uses",
          "entity": "proposer"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "receives",
          "entity": "account"
        },
        {
          "verb": "uses",
          "entity": "co-proposer"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "receives",
          "entity": "account"
        },
        {
          "verb": "uses",
          "entity": "delegator"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "receives",
          "entity": "account"
        },
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
      "target": "src/lib/db/notifications.ts#markAllRead"
    }
  ]
}
---

# Opening the inbox marks only the person's own notifications read

Only the person's own notifications are marked read.
