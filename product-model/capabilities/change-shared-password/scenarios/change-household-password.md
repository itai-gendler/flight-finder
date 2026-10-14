---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin verifies with the current password and enters a new password of at least 12 characters",
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
      "text": "The Product replaces the shared password, signs out every browser and removes every passkey",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "app-access",
          "effect": "changes",
          "facts": [
            "Shared password"
          ]
        },
        {
          "entity": "browser-session",
          "effect": "removes"
        },
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

# Change the shared password

## Trigger

Admin wants a new shared password.

## Outcome

Only the new password opens the app; every browser enters again and passkeys must be saved again.
