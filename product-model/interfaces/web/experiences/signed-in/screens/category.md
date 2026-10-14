---
{
  "entities": [
    {
      "entity": "thread",
      "shows": [
        "Title",
        "Category",
        "Opened by",
        "Replies",
        "Last activity"
      ],
      "collects": [
        "Title"
      ]
    },
    {
      "entity": "post",
      "collects": [
        "Body"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/c/[slug].astro"
    }
  ]
}
---

# Category

The threads of one discussion category, or of the Surveys category, newest activity first.
