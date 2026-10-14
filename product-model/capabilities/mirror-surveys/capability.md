---
{
  "availability": [
    {
      "place": "web::public"
    }
  ],
  "domain": "surveys",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/surveys/sync.ts#syncSurveys"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/surveys/admission.ts#eligibleSurvey"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/cip-179-surveys.md"
    }
  ]
}
---

# Mirror surveys

Every few minutes the Product reads the Tessera index and mirrors each CIP-179 survey that DReps may answer, that has a valid definition, whose encryption it can read and that an imported governance action links: it opens the survey's thread and keeps its responses and tally current. Runs only on a deployment with a survey index configured.
