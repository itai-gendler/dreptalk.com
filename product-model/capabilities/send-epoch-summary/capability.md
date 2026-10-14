---
{
  "availability": [
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "notifications",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/delegationDigest.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/notifications/delegationDigest.ts#isReportable"
    }
  ]
}
---

# Send epoch summaries

After an epoch in which a followed DRep voted, the Product writes each follower an epoch summary: how many actions it voted on, up to three titles, and how many votes carry a rationale.
