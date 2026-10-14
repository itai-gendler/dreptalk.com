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
      "target": "src/pages/cite/[postId].astro"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/citing-a-post.md"
    }
  ]
}
---

# Cite a post

Anyone opens Cite on a public post to get the permanent, content-addressed address of each version, so a quote cannot silently change later.
