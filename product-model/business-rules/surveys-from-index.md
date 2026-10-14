---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "survey",
      "effect": "creates"
    },
    {
      "type": "entity",
      "id": "survey-response",
      "effect": "creates"
    }
  ],
  "permits": [
    {
      "unattended": true
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/surveys/sync.ts#syncSurveys"
    }
  ]
}
---

# Surveys and their responses come only from the survey index

The Product mirrors surveys and responses from the Tessera index; answering happens on chain from the DRep's wallet.
