---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Proposer starts a thread in Proposal Drafts and fills in the outline: summary, action type, amount, motivation and planned submission",
      "kind": "actor",
      "actor": "proposer",
      "entities": [
        {
          "entity": "thread",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::category"
        }
      }
    },
    {
      "text": "The Product opens the Thread with an opening Post of up to 150,000 characters",
      "kind": "product",
      "actor": "proposer",
      "entities": [
        {
          "entity": "thread",
          "effect": "creates",
          "to": "Open",
          "facts": [
            "Title",
            "Category",
            "Opened by",
            "Address",
            "Replies",
            "Last activity",
            "Written under mandate"
          ]
        },
        {
          "entity": "post",
          "effect": "creates",
          "to": "Visible",
          "facts": [
            "Body",
            "Kind",
            "Posted at",
            "Written under mandate"
          ],
          "with": "thread"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::category"
        }
      }
    },
    {
      "text": "The Product takes the Proposer to the draft with its link and a copy button",
      "kind": "product",
      "actor": "proposer",
      "entities": [
        {
          "entity": "thread",
          "effect": "reads",
          "facts": [
            "Address"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::thread"
        }
      }
    }
  ]
}
---

# Share a proposal draft

## Trigger

A proposer wants feedback before submitting a governance action.

## Outcome

The draft is open in Proposal Drafts; its author sees the exact link to put into the action's references.
