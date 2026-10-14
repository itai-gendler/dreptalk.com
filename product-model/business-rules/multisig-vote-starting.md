---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "multisig-vote",
      "effect": "creates"
    }
  ],
  "permits": [
    {
      "actors": [
        "drep"
      ],
      "when": [
        {
          "entity": "drep",
          "fact": "Script DRep",
          "is": "Yes"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/api/drep/multisig/index.ts"
    }
  ]
}
---

# Only a multisig DRep starts a multisig vote

A member signed in as a native-script DRep starts the vote that collects signatures.
