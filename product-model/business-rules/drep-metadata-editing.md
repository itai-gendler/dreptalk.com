---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "drep",
      "effect": "changes",
      "facts": [
        "Name",
        "Objectives",
        "Motivations",
        "Qualifications",
        "Links",
        "Image",
        "Payment address",
        "Do not list"
      ]
    }
  ],
  "permits": [
    {
      "self": true
    },
    {
      "unattended": true
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/drepProfileApply.ts#applyDrepProfile"
    }
  ]
}
---

# Only the DRep itself changes its profile

A DRep changes only its own profile, by signing an update certificate; the DRep sync applies what the chain holds.
