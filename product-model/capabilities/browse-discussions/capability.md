---
{
  "availability": [
    {
      "place": "web::public"
    },
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "discussions",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/discussions.astro"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/c/[slug].astro"
    }
  ]
}
---

# Browse discussions

Anyone follows the forum: recent activity across categories, and the threads of one category.
