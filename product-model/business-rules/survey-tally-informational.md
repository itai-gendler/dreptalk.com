---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "mirror-surveys"
    },
    {
      "type": "entity",
      "id": "survey",
      "facts": [
        "Tally"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/surveys/tallyCompute.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/cip-179-surveys.md"
    }
  ]
}
---

# A survey tally is a reading, never a result

Only DRep responses count, under the generic CIP-179 validity rules with the denominator stated; the power behind each option is shown next to the number of DReps who picked it.
