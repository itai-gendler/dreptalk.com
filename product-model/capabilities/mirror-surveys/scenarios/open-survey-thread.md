---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "An eligible Survey is linked by an imported Governance action",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "survey",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::thread"
        }
      }
    },
    {
      "text": "The Product stores the Survey and opens its Thread with an opening Post written by the Product",
      "kind": "product",
      "entities": [
        {
          "entity": "survey",
          "effect": "creates",
          "to": "Open",
          "facts": [
            "Questions",
            "Eligible roles",
            "Closing epoch",
            "Sealed",
            "Text loaded"
          ]
        },
        {
          "entity": "thread",
          "effect": "creates",
          "to": "Open",
          "facts": [
            "Title",
            "Category",
            "Opened by",
            "Address"
          ],
          "with": "survey"
        },
        {
          "entity": "post",
          "effect": "creates",
          "to": "Visible",
          "facts": [
            "Body",
            "Kind",
            "Posted at"
          ],
          "with": "thread"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::thread"
        }
      }
    }
  ]
}
---

# Open the thread of a linked survey

## Trigger

An eligible survey is linked by a governance action DRepTalk mirrors.

## Outcome

The survey has its thread in Surveys with the survey card at the top.
