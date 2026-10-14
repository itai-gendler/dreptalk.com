---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "thread",
      "effect": "changes",
      "facts": [
        "Title"
      ]
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "opens",
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
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/forum.ts#editTitle"
    }
  ]
}
---

# Only its author retitles a thread

The person who opened a thread in a discussion category changes its title.
