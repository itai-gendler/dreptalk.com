---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "start-topic"
    },
    {
      "type": "entity",
      "id": "thread",
      "facts": [
        "Category"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "config/categories.ts#isDiscussion"
    }
  ]
}
---

# People open threads only in the discussion categories

Proposal Drafts, Constitution and Guardrails, Budget and Treasury and General take threads from writers; Governance Actions and Surveys hold only threads the Product opens.
