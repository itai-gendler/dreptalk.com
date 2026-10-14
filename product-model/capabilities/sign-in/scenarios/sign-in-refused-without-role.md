---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor signs the challenge for a role their key does not hold",
      "kind": "actor",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::sign-in"
        }
      }
    },
    {
      "text": "The key holds no active on-chain role of that kind",
      "kind": "condition",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::sign-in"
        }
      }
    },
    {
      "text": "The Product refuses the sign-in",
      "kind": "product",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::sign-in"
        }
      }
    }
  ]
}
---

# Sign-in refused without an on-chain role

## Trigger

Someone signs with a key that holds no governance role.

## Outcome

No device is signed in; the sign-in screen says the key is not an active DRep, SPO, CC member or proposer.

## Edge cases

- An inactive DRep, a retired DRep and a Plutus-script DRep are refused the DRep role.
- A challenge is single-use and expires; signing an old one is refused.
- A wallet on the other network is refused with a network mismatch.
