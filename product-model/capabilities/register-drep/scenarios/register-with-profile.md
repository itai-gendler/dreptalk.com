---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor connects a CIP-95 wallet and fills in the profile with an optional image",
      "kind": "actor",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::register-drep"
        }
      }
    },
    {
      "text": "The Product hosts the profile document at an address named by its hash",
      "kind": "product",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::register-drep"
        }
      }
    },
    {
      "text": "The Visitor signs and submits the registration in the wallet, paying the deposit and fee",
      "kind": "actor",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::register-drep"
        }
      }
    }
  ]
}
---

# Register with a profile

## Trigger

A holder wants to represent delegators.

## Outcome

The registration is submitted; the DRep appears on DRepTalk after the next DRep sync.

## Edge cases

- Motivations, qualifications, a payment address and the do-not-list flag sit behind Show advanced fields.
