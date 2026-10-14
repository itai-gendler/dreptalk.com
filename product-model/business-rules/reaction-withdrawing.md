---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "reaction",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "gives",
          "entity": "drep"
        }
      ],
      "when": [
        {
          "entity": "drep",
          "fact": "Status",
          "is": "Active"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "gives",
          "entity": "spo"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "gives",
          "entity": "cc-member"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "gives",
          "entity": "proposer"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "gives",
          "entity": "co-proposer"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/postReactions.ts#clearReaction"
    }
  ]
}
---

# Only its writer withdraws a reaction

A writer withdraws only their own reaction.
