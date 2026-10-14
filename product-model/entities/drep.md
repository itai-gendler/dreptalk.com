---
{
  "kind": "person",
  "acts": "external",
  "relations": [
    {
      "entity": "account",
      "verb": "uses",
      "cardinality": "one-to-one"
    },
    {
      "entity": "thread",
      "verb": "opens",
      "cardinality": "one-to-many"
    },
    {
      "entity": "post",
      "verb": "writes",
      "cardinality": "one-to-many"
    },
    {
      "entity": "reaction",
      "verb": "gives",
      "cardinality": "one-to-many"
    },
    {
      "entity": "flag",
      "verb": "raises",
      "cardinality": "one-to-many"
    },
    {
      "entity": "vote",
      "verb": "casts",
      "cardinality": "one-to-many"
    },
    {
      "entity": "drep-link",
      "verb": "owns",
      "cardinality": "one-to-one"
    },
    {
      "entity": "multisig-vote",
      "verb": "collects",
      "cardinality": "one-to-many"
    },
    {
      "entity": "survey-response",
      "verb": "sends",
      "cardinality": "one-to-many"
    },
    {
      "entity": "delegation",
      "verb": "represents",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/dreps.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/dreps/sync.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/managing-your-drep.md"
    }
  ]
}
---

# DRep

A delegated representative registered on chain. Every registered DRep has a profile here whether or not it ever signed in; one that signs in with its DRep key writes in threads, votes on open governance actions and manages its own on-chain registration and metadata. A DRep controlled by a native multisig script signs in through any of its member keys and acts as that one DRep.

## Information kept

- **DRep ID** — the on-chain credential id, key-based or script-based
- **Name** — the display name from its CIP-119 metadata
- **Objectives** — the objectives text from its metadata
- **Motivations** — the motivations text from its metadata
- **Qualifications** — the qualifications text from its metadata
- **Links** — the links from its metadata
- **Image** — the profile image its metadata points to, kept as a self-hosted copy
- **Payment address** — the payment address from its metadata
- **Do not list** — the CIP-119 do-not-list flag; DRepTalk still shows the DRep
- **Status** — Active, Inactive or Retired, as of the last DRep sync
- **Voting power** — the stake delegated to it, as of the last sync, with its history per epoch
- **Delegators** — how many stake addresses delegate to it
- **Script DRep** — whether a native multisig script controls it
- **Report card** — its participation, rationale coverage, vote changes and timing against other DReps
- **Profile as of** — when its profile and voting power were last synced
