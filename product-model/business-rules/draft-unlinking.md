---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "governance-action",
      "effect": "changes",
      "facts": [
        "Draft link refused"
      ]
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "drafts",
          "entity": "thread"
        },
        {
          "verb": "opens",
          "entity": "drep"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "drafts",
          "entity": "thread"
        },
        {
          "verb": "opens",
          "entity": "spo"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "drafts",
          "entity": "thread"
        },
        {
          "verb": "opens",
          "entity": "cc-member"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "drafts",
          "entity": "thread"
        },
        {
          "verb": "opens",
          "entity": "proposer"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "drafts",
          "entity": "thread"
        },
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
      "target": "src/lib/db/draftLinks.ts#isDraftAuthor"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/forum/handlers.ts#handleDraftUnlink"
    }
  ]
}
---

# Only the draft's author or a moderator detaches an action

The author of the Proposal Draft, under the same mandate it was opened with, or a moderator detaches a governance action from the draft; a lapsed writer role does not stop the author.
