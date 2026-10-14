---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep gives eleven actions in one batch eleven different rationales",
      "kind": "actor",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::voting-dashboard"
        }
      }
    },
    {
      "text": "The Product disables submitting and explains the limit",
      "kind": "product",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::voting-dashboard"
        }
      }
    }
  ]
}
---

# More than ten different rationale texts

## Trigger

A batch carries more than ten distinct rationale texts or more than 50 votes.

## Outcome

Submit stays disabled with a notice; nothing is signed.
