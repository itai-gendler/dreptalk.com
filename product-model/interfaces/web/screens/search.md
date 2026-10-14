---
{
  "entities": [
    {
      "entity": "thread",
      "shows": [
        "Title",
        "Category"
      ]
    },
    {
      "entity": "post",
      "shows": [
        "Body"
      ]
    },
    {
      "entity": "governance-action",
      "shows": [
        "Title",
        "Action ID"
      ]
    },
    {
      "entity": "drep",
      "shows": [
        "Name",
        "DRep ID"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/search.astro"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/search/handler.ts"
    }
  ]
}
---

# Search

Search across threads, posts, governance actions and DReps; an on-chain id goes straight to its page.
