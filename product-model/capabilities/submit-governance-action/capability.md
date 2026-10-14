---
{
  "availability": [
    {
      "place": "web::signed-in"
    }
  ],
  "references": [
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/submit-a-governance-action.md"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/govActionGate.ts#gateGovActionRequest"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/guardrailEvaluator.ts"
    }
  ]
}
---

# Submit a governance action

A signed-in person builds a governance action in a form, reviews it as its page will show, and signs and submits it with their own wallet, which pays the deposit. Available on the preprod network only.
