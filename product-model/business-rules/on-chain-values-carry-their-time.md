---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "governance-action",
      "facts": [
        "Data as of"
      ]
    },
    {
      "type": "entity",
      "id": "drep",
      "facts": [
        "Profile as of"
      ]
    }
  ],
  "references": [
    {
      "kind": "doc",
      "role": "intent",
      "target": "README.md",
      "title": "README"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/freshness.ts"
    }
  ]
}
---

# Every on-chain value is shown with the time of its data

The chain is never read live on a page; scheduled syncs fill what pages show.
