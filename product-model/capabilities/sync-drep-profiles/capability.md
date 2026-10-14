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
      "target": "src/lib/dreps/sync.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/sync/phases/dreps.ts"
    }
  ]
}
---

# Sync DRep profiles

Every six hours the Product reads every registered DRep from the chain: new DReps, their CIP-119 profiles, voting power and status, and tells delegators who follow a DRep when its status changes.
