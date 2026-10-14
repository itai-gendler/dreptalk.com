---
{
  "domain": "discussions",
  "references": [
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/citing-a-post.md"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/cip100.ts"
    }
  ]
}
---

# Post version

A permanent, content-addressed version of a public post that can be cited: its address is derived from its text, so the text behind it never changes.

## Information kept

- **Text** — the post text of that version
- **Address** — the content-derived address the version is served at
- **Published at** — when the version was published
- **Replaced at** — when a later edit replaced it
