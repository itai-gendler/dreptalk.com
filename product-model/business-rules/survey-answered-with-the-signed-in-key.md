---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "answer-survey"
    },
    {
      "type": "entity",
      "id": "survey-response",
      "facts": [
        "Counted"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/components/survey/RespondPanel.astro"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/cip-179-surveys.md"
    }
  ]
}
---

# A survey is answered with the DRep key the person signed in with

The answer is signed in the DRep's own wallet with the same key credential; it is survey metadata, not a vote, and counts through the closing epoch, a later answer replacing an earlier one.
