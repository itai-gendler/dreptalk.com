---
{
  "entities": [
    {
      "entity": "drep",
      "shows": [
        "DRep ID",
        "Name",
        "Objectives",
        "Motivations",
        "Qualifications",
        "Links",
        "Image",
        "Status",
        "Voting power",
        "Delegators",
        "Report card",
        "Profile as of"
      ]
    },
    {
      "entity": "vote",
      "shows": [
        "Choice",
        "Cast at",
        "Earlier votes"
      ]
    },
    {
      "entity": "drep-link",
      "shows": [
        "Short name"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/dreps/[drepId].astro"
    }
  ]
}
---

# DRep profile

One DRep: its metadata, voting power, votes with rationales, report card and drep.link.
