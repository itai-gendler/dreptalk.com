---
{
  "entities": [
    {
      "entity": "post-version",
      "shows": [
        "Text",
        "Replaced at"
      ]
    },
    {
      "entity": "post",
      "shows": [
        "Body",
        "Edited"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/posts/[id]/history.astro"
    }
  ]
}
---

# Post history

Every earlier version of an edited post, with the changes between them.
