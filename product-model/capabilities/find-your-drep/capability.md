---
{
  "availability": [
    {
      "place": "web::public"
    },
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "dreps",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/match.astro"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/match/logic.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/drep-matching.md"
    }
  ]
}
---

# Find your DRep

Anyone answers real governance questions and gets the DReps whose past votes line up with the answers; the answers never leave the browser.
