---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A new Governance action names a live Proposal Drafts Thread among its first 20 references",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "thread",
          "as": "draft",
          "effect": "reads",
          "facts": [
            "Address"
          ]
        },
        {
          "entity": "governance-action",
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
      "text": "The Product opens the action's Thread and connects the draft to the Governance action",
      "kind": "product",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "creates",
          "to": "Syncing",
          "facts": [
            "Action ID",
            "Type",
            "Title",
            "References"
          ]
        },
        {
          "entity": "thread",
          "as": "governance-thread",
          "effect": "creates",
          "to": "Open",
          "facts": [
            "Title",
            "Category",
            "Opened by",
            "Address"
          ],
          "with": "governance-action"
        },
        {
          "entity": "thread",
          "as": "draft",
          "effect": "changes",
          "from": "Open",
          "to": "Closed",
          "facts": []
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

# Connect the Proposal Draft the action names

## Trigger

The new action's references name a Proposal Drafts thread on this network.

## Outcome

The draft shows Now on-chain and closes; the action shows Discussed as a draft.

## Edge cases

- A draft named by several actions shows all of them; it reopens only when none remains connected.
- An action its draft's author detached is never connected to that draft again.
