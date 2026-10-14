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
      "target": "src/lib/cip100/reconcile.ts#reconcilePostDocs"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/sync/phases/governance.ts#governancePhases"
    }
  ]
}
---

# Publish post versions

Once a public post's grace window has closed, the Product publishes its current text as a citable version, and catches up on any edit not yet published.
