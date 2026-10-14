---
{
  "availability": [
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "surveys",
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

# Answer a survey

A DRep answers a survey from its thread with the wallet holding the same DRep key it signed in with; the wallet signs and submits the answer, which is survey metadata and not a vote.
