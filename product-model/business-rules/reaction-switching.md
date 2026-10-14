---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "reaction",
      "effect": "changes"
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
      "target": "src/lib/db/postReactions.ts#setReaction"
    }
  ]
}
---

# Only its writer switches a reaction

A writer switches only their own reaction to the other side.
