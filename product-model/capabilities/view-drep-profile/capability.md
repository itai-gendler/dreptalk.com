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
  "domain": "dreps",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/dreps/[drepId].astro"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/drep-report-card.md"
    }
  ]
}
---

# View a DRep profile

Anyone reads a DRep's profile: its metadata, voting power, every vote with its rationale, and its report card. A link built from the DRep ID redirects to the named profile.
