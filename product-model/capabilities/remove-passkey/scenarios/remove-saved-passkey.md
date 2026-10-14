---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin verifies their identity and chooses Remove beside the passkey",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "passkey",
          "effect": "reads",
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
    },
    {
      "text": "The Product removes the passkey",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "passkey",
          "effect": "removes"
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

# Remove a passkey

## Trigger

Admin no longer wants a saved passkey to open the app.

## Outcome

The passkey no longer opens the app.
