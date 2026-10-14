---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "post",
      "effect": "changes",
      "facts": [
        "Body"
      ]
    }
  ],
  "permits": [
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
        },
        {
          "fact": "Kind",
          "is-not": "Vote rationale"
        },
        {
          "state": "Visible"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "writes",
          "entity": "spo"
        }
      ],
      "when": [
        {
          "fact": "Kind",
          "is-not": "Vote rationale"
        },
        {
          "state": "Visible"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "writes",
          "entity": "cc-member"
        }
      ],
      "when": [
        {
          "fact": "Kind",
          "is-not": "Vote rationale"
        },
        {
          "state": "Visible"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "writes",
          "entity": "proposer"
        }
      ],
      "when": [
        {
          "fact": "Kind",
          "is-not": "Vote rationale"
        },
        {
          "state": "Visible"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "writes",
          "entity": "co-proposer"
        }
      ],
      "when": [
        {
          "fact": "Kind",
          "is-not": "Vote rationale"
        },
        {
          "state": "Visible"
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
      "target": "src/lib/db/forum.ts#editPost"
    }
  ]
}
---

# Only its author edits a visible post that is not a vote rationale

A writer edits only their own post, while it is visible and unless it is a cross-posted vote rationale. The Product changes a post's text only when it erases a deleted post.
