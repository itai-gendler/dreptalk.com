---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "post",
      "effect": "reads",
      "facts": [
        "Body"
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "visitor",
        "drep",
        "spo",
        "cc-member",
        "proposer",
        "co-proposer",
        "delegator",
        "moderator"
      ],
      "when": [
        {
          "state": "Visible"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "writes",
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
          "verb": "writes",
          "entity": "spo"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "writes",
          "entity": "cc-member"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "writes",
          "entity": "proposer"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "writes",
          "entity": "co-proposer"
        }
      ]
    },
    {
      "actors": [
        "moderator"
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
      "target": "src/lib/forum/postVisibility.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/posts/[id]/history.astro"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "README.md",
      "title": "README"
    }
  ]
}
---

# Only its author and moderators read a hidden post

Anyone reads a visible post. Once hidden, its text and its history are shown only to its author and to moderators.
