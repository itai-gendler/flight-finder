---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin verifies with the shared password, names the new credential and confirms with the device",
      "kind": "actor",
      "actor": "admin",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::administration::account-security"
        }
      }
    },
    {
      "text": "The Product saves the passkey",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "passkey",
          "effect": "creates",
          "facts": [
            "Name",
            "Saved at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::account-security"
        }
      }
    }
  ]
}
---

# Add a passkey from Account security

## Trigger

Admin opens Account security.

## Outcome

A new passkey is saved.
