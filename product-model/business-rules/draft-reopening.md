---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "thread",
      "effect": "changes",
      "to": "Open"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "opens",
          "entity": "drep"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "opens",
          "entity": "spo"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "opens",
          "entity": "cc-member"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "opens",
          "entity": "proposer"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "opens",
          "entity": "co-proposer"
        }
      ]
    },
    {
      "actors": [
        "moderator"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/draftLinks.ts#unlinkDraftAction"
    }
  ]
}
---

# Only the draft's author or a moderator reopens a connected draft

A connected draft reopens when its author or a moderator detaches the last action connected to it.
