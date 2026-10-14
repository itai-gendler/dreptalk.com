---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "notification-channel",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "connects",
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
          "verb": "connects",
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
          "verb": "connects",
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
          "verb": "connects",
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
          "verb": "connects",
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
          "verb": "connects",
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
          "verb": "connects",
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
      "target": "src/lib/db/notificationChannels.ts"
    }
  ]
}
---

# A person removes only their own channels

A person disconnects only their own channels; the Product removes a channel that no longer accepts delivery.
