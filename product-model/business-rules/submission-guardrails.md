---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "submit-governance-action"
    },
    {
      "type": "entity",
      "id": "governance-action",
      "facts": [
        "On-chain changes"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/guardrailEvaluator.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/submit-a-governance-action.md"
    }
  ]
}
---

# A treasury withdrawal or parameter change is signed only after the guardrails script accepts it

Every treasury withdrawal recipient must be a registered stake address, and parameter values must stay within the constitution's range.
