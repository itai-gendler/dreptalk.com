---
{
  "availability": [
    {
      "place": "web::public"
    }
  ],
  "domain": "governance-actions",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/sync.ts#syncGovernanceActions"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/sync.ts#createDeferredGovTopics"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/draftLinks.ts#buildDraftLinkStatements"
    }
  ]
}
---

# Open a governance action thread

Every few minutes the Product discovers new governance actions on chain, reads and verifies each proposal document and opens one thread per action, connecting it to the Proposal Draft its references name.
