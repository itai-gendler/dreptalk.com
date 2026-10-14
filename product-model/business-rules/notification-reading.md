---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "notification",
      "effect": "reads"
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
    },
    {
      "unattended": true
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/notifications.astro"
    }
  ]
}
---

# A person reads only their own notifications

The inbox shows only the person's own notifications.
