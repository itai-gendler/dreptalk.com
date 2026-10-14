---
{
  "references": [
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/managing-your-drep.md"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/drepLink/claim.ts"
    }
  ]
}
---

# drep.link

A DRep's short link, drep.link/name, that redirects to its profile.

## Information kept

- **Short name** — the current name after drep.link/
- **Previous name** — the name it replaced, still redirecting
- **Previous name redirects until** — 180 days after the change
- **Next change from** — 90 days after the DRep's own last change
- **Followers gained** — accounts that arrived through the link and started following a delegation
