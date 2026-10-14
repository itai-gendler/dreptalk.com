---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "delegation",
      "effect": "reads",
      "facts": [
        "Stake address"
      ]
    },
    {
      "type": "entity",
      "id": "account",
      "effect": "reads",
      "facts": [
        "Linked stake address"
      ]
    }
  ],
  "permits": [],
  "references": [
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/my-drep.md"
    }
  ]
}
---

# Nobody reads a followed stake address on a page

The stake address behind a followed delegation stays on the server: it is in no link, no URL and no page.
