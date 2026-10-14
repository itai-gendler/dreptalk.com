---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "flag",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "raises",
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
          "verb": "raises",
          "entity": "spo"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "raises",
          "entity": "cc-member"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "raises",
          "entity": "proposer"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "raises",
          "entity": "co-proposer"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/postFlags.ts#unflagPost"
    }
  ]
}
---

# Only its writer withdraws a flag

A writer withdraws only their own flag.
