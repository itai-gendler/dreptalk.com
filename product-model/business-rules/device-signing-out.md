---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "device",
      "effect": "changes",
      "to": "Signed out"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "has",
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
          "verb": "has",
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
          "verb": "has",
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
          "verb": "has",
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
          "verb": "has",
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
          "verb": "has",
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
          "verb": "has",
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
      "target": "src/lib/auth/session.ts#revokeSessionForUser"
    }
  ]
}
---

# A person signs out only their own devices

Signing out one device, or every device, acts only on the devices of the person's own account.
